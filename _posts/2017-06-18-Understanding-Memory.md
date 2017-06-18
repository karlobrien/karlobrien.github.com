---
layout: post
title:  "Understanding Memory"
tags:
- Memory JIT Assembly Web
---

# Memory
As part of trying to understand how computer memory works, I am putting together some links on the best sources of information

In source code, incrementing a variable looks like a single operation but at cpu level it takes three instructions.
1. Load from memory (RAM) into short term memory (registers)
2. Perform the operation.
3. Store the result in memory.

Atomic operations make the computer see the above as single operations also.

## Three Common problems in memory

* (Crash Course In Memory Management)[https://hacks.mozilla.org/2017/06/a-crash-course-in-memory-management/]



# JIT Compilers
Overview of JIT here

* (Crash Course in JIT Compilers)[https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers/]

#Assembly
Overview here

(Assembly)[https://hacks.mozilla.org/2017/02/a-crash-course-in-assembly/]

# Web Assembly
* (Web Assembly)[https://hacks.mozilla.org/2017/02/a-cartoon-intro-to-webassembly/]