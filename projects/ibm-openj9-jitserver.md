---
layout: page
title: IBM - OpenJ9 JITServer Log Management
---

The [Eclipse OpenJ9 project](https://github.com/eclipse/openj9) is an open source runtime for running Java applications. One of the newest innovations in the Eclipse OpenJ9 codebase is a project called JIT-as-a-Service. Traditionally, a JIT compiler runs inside the JVM compiling Java bytecode to binary machine instructions to improve performance. The downside of this process is that it takes CPU and memory resources away from the application which is running - these resources are used to run the compiler. The JIT-as-a-Service project decouples the JIT compiler from the rest of the JVM so that it can be run as a service in the cloud! This new compilation model is more challenging to debug, but opens a number of exciting new possibilities.

When debugging a problem in dynamically compiled (“jitted”) code developers typically resort to compilation logs which detail the decisions taken by the JIT compiler and show the intermediate language (IL) representation of the compiled method after each optimization pass. Unfortunately, due to the non-deterministic nature of the JIT compiler, a compilation log generated in a subsequent run may not faithfully describe the native code generated in a previous run. On the other hand, proactively logging all the methods is prohibitively expensive both in terms of CPU and memory footprint. However, since in a JIT-as-a-Service solution the compilations happen in a remote JITServer process, consuming more resources for the sake of producing the compilation logs becomes feasible.

### Outline
Because the compilation logs can be big, they cannot be kept in memory - they need to be stored out to disk. Rather than reinventing the wheel and creating a brand new implementation of a log repository it’s probably better to store the logs in an “off-the-shelf” database. The search key should be composed of the ID of the client that requested the compilation and the name of the compiled method. Since there could be several compilations for the same method, the system needs to be able to store several values for the same key. A key-value store like Cassandra seems very well suited to the job (other database systems may work as well). Other considerations for the project:
* To reduce storage needs the logs should be compressed (compression can happen at the JITServer or the database system could do it).
* Some customers may want the data to be encrypted.
* The users should have the option to select which methods to log (wildcards should be supported) and the amount of debugging information to generate.

A related but independent logging problem is the following: The JITServer process produces a “verbose log” (vlog) which includes details of every compilation request it receives from various JVM clients. This could be useful in tracking performance issues as well as troubleshooting the handshake between the clients and the server. Because the JITServer is a long running process that can serve many JVM clients, over time the vlog could grow very large. The proposed solution involves a scheme of rotating logs: once the vlog reaches a certain size, the file is closed and a new one is started. The JITServer will keep only the last N vlogs around and delete the rest. Again, configurability, compression and encryption concerns apply.

The end goal of this project is to implement efficient log management for the JIT-as-a-Service solution to facilitate debugging and analysis of the compiler when not run in the JVM.

### Required Skills

Comfortable programming with C++ and Java, familiarity with databases, application logging frameworks, and log rotation are a bonus.

### Minimum Software/Hardware Requirements
Linux OS (can be a VM) suitable to [build Eclipse OpenJ9](https://github.com/eclipse/openj9/blob/master/doc/build-instructions/Build_Instructions_V8.md). Before the code sprint, students should fork, clone, and build Eclipse OpenJ9. Note that native building of Java 8 on MacOS is not supported - you will need a true linux environment.
