---
layout: post
title: IBM - OMR Tree Interpreter
permalink: /projects/ibm-omr-tree/
type: current
---

The [Eclipse OMR project](https://github.com/eclipse/omr) is an open-source and reusable toolkit implemented in C/C++ for building runtimes. It includes code for important language-agnostic runtime components, such as a JIT compiler and garbage collector as well as diagnostic tooling and platform abstraction technologies. There have been successful proof-of-concept projects leveraging OMR to enable JIT compilation for languages such as Lua, WebAssembly, and Python and it is also used to build the [Eclipse OpenJ9 JVM](https://github.com/eclipse/openj9). The Eclipse OMR compiler has an internal language-independent intermediate representation (IR) called OMR trees. Source programs are translated into OMR trees before being processed by the rest of the OMR compiler. OMR trees are a really useful tool, but we currently do not have an interpreter to evaluate OMR trees without first translating them to binary machine instructions.

<!--more-->

### Outline
The goal of this project is to build an interpreter for OMR trees to sever two goals: 1) create an abstract interpreter which generates constraint information for program values (this is used to drive program optimizations and 2) create an interactive terminal to let people write OMR trees and understand how they work.
A three year research project between IBM and the University of Alberta has produced an innovative new inliner which allowing the OMR compiler to produce smaller programs that run faster than the current inliner. This new inliner uses an abstract interpreter to gather information about the program which it uses to make good decisions about what to do. The abstract tree interpreter produced by this project will allow this new inliner to be used with more OMR-based runtimes like WebAssembly - currently this inliner only works with Java bytecode!

### Required Skills
Comfortable programming with C++ and Java, compiler background is desirable, interest in program analysis is a plus.

### Minimum Software/Hardware Requirements
Linux OS is preferable, but any supported platform/OS listed [here](https://github.com/eclipse/omr#eclipse-omr) will work. Instructions on how to build OMR can be found [here](https://github.com/eclipse/omr/blob/master/doc/BuildingWithCMake.md#requirements). Before the code sprint students should fork, clone, and build Eclipse OMR and Eclipse OpenJ9.