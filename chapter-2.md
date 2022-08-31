# Introduction to Operating Systems
OS provides an easy to use interface for software to interact with hardware. OS do this through a process of __virtualization__: takes physical resource (processor, memory, disks, etc.) and transforms it into a more general, powerful, and easy-to-use virtual form of itself, thus the OS is often referred to as a __virtual machine__

This "easy-to-use interface" (OS's) provides a few hundred __system calls__ to applications (a.k.a standard library), allowing applications to interact with hardwares.

OS is also known as a __resource manager__, because it enables multiple programs to run and share the same hardware (CPUs, memory, disks, etc.)

## Virtualizing the CPU
With just one CPU, the OS can provide the __illusion__ of multiple virtual CPUs, executing multiple programs at once. There are policies of the OS to handle special situations (i.e if 2 programs want to run at a particular time, which _should_ run?)

## Virtualizing the Memory
With multiple programs running at once, the OS creates the __illusion__ that each program has its own private __virtual address space__. The OS does this by somehow maps these virtual addresses to the physical memory of the machine. A memory reference within one running program does not affect the address space of another program (or the OS itself). In reality, a computer's physical memory is a shared resource managed by the OS.

## Concurrency
The conceptual term refers to a group of problems when it comes to working with __many things at once__ in the same program. Some examples:
- The OS can have multiple program running at once, which leads to some deep and interesting problems
- The OS can manage multiple processors to run at once (as opposed to just have one processor), which also leads to some interesting problems

## Persistence
Most users want their data to be persistent and shared amongst programs. The OS provides a __file system__, responsible for storing any files the user creates in a reliable and efficient manner on the disks of the system.

## Design Goals
- Abstractions to make the system convenient and easy to user
- Performant while minimizing overheads