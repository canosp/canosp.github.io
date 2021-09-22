---
layout: post
title:  Code Sprint - Fall 2021
date:   2021-09-22 12:05:55 -0700
image:  '/assets/photos/w20.jpg'
tags:   Codesprint
---

This semester, we have 4 exciting projects:
- [Automated JIT Compiler Debugging Agent](#automated-jit-compiler-debugging-agent)
- [Eclipse Adoptium and Eclipse AQAvit](#eclipse-adoptium-and-eclipse-aqavit)
- [Language Server for Eclipse Jakarta EE](#language-server-for-eclipse-jakarta-ee)
- [Review Board](#review-board)

<br /><br />

## Automated JIT Compiler Debugging Agent
The JIT compiler, and hence the JVM, is a non-deterministic program. While the output of a Java program is predictable each time the JVM executes it, the manner in which the JVM executes that program is not. There are a variety of reasons for this, including memory/CPU resource availability at execution time, timing of triggering JIT compilation, varying profiling metrics between runs, hardware support, and environmental settings.

Because the JVM is a non-deterministic program, it is often found that defects in the JVM are intermittent. Intermittent defects are software defects that do not occur 100% of the time that the program/test is run. The reasons for intermittency are the same reasons outline above, i.e. the JIT is a non-deterministic program and hence compilations can look different in different environment settings. This project aims to automate JIT compiler debugging by reducing the problem space using key insights into the JIT compilation process.

#### Participating Students
- Qasim Khawaja (University of Alberta)
- Shane Killoran (University of British Columbia)

#### Project Mentors
- Filip Jeremic
- Rahil Shah

#### Code Sprint Presentation
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/wydNpzsqTSY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br /><br />


## Eclipse Adoptium and Eclipse AQAvit
Adoptium is a community-driven, open-source project dedicated to building, testing and distributing high-quality, fully-testing OpenJDK binaries to the Java community. AQAvit (Adoptium Quality Assurance vitality project) is an ever-evolving program to “make quality certain to happen”. We create tools and innovate in the area of software verification, bringing research and prototypes to production grade solutions as part of our mission to provide high-quality OpenJDK binaries.

#### Participating Students
- Amanda Nguyen (University of Alberta)
- Paul Saunders (University of Alberta)
- Shiyu Xiu (University of Alberta)

#### Project Mentors
- Shelley Lambert
- Lan Xia
- Sophia Guo


#### Code Sprint Presentation
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/vL1Za4ULgtA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br /><br />


## Language Server for Eclipse Jakarta EE (IBM)
Develop a language server and the associated Eclipse client for the set of open cloud-native Java APIs in Eclipse Jakarta EE to boost developer productivity. Eclipse Jakarta EE is an open source community-driven collaboration on defining and innovating on the next generation of cloud-native Java APIs.

The Language Server Protocol (LSP) enables language-specific assistance for IDEs and editors such as validations, auto-complete etc to be built in a common reusable way.

This project looks to develop a common Language Server using the Language Server Protocol for Jakarta EE APIs and the associated client for the Eclipse IDE.

#### Participating Students
- Alvin Tan (McGill University)
- Ananya Rao (University of Alberta)
- Daniil Tiganov (University of Alberta)
- Himanshu Chotwani (University of British Columbia)
- Shaunak Tulshibagwale (University of British Columbia)
- Zijian Pei (McGill University)

#### Project Mentors
- Yee-Kang (YK) Chang
- Kevin Sutter
- Kathryn Kodama
- Eric Lau


#### Code Sprint Presentation
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/E-KGtkflO98" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br /><br />


## Review Board (Beanbag)
Review Board is a powerful web-based code review tool that helps developers do peer review as they write code. Code review is a standard industry practice used to find bugs, improve quality, and mentor junior engineers.

Review Board is used by thousands of software companies including Yelp, LinkedIn, and VMware, as well as many open-source projects like Apache.

Students working on Review Board will have the opportunity to learn about back-end web development using Python and Django, as well as front-end development using HTML, CSS, Javascript, jQuery, and Backbone.js. Source control is managed via Git on GitHub. All patches are reviewed using Review Board, and students will be participating in the code review process.

#### Participating Students
- Akim Ruslanov (University of British Columbia)
- Cynthia (Lanhui) Shi (McGill University)
- Jordan Van Den Bruel (University of Alberta)
- Matthew Goodman (McGill University)
- Michelle Aubin (University of Alberta)
- Michelle Wang (University of Alberta)
- Sandy Saji (University of Alberta)

#### Project Mentors
- Mike Conley
- David Trowbridge
- Christian Hammond

#### Code Sprint Presentation
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/jG5E4WdLTL0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<br /><br />