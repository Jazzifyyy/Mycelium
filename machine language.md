---
tags:
  - books
  - operating_systems
  - info
---
_Machine language_ is a collection of unique bit patterns that a device can identify and perform an action. 

A _machine instruction_ is a unique bit pattern that a device can identify.

In a computer system, a device with its language is called CPU (Central-Processing-Unit), which controls all activities going inside a computer. For example, in the x86 architecture, the pattern `10100000` means telling a CPU to add two numbers, or `000000101` to halt a computer.

Why does such a bit pattern cause a device to do something? The reason is that underlying each instruction is a small circuit that implements the instruction. Similar to how a function/subroutine in a computer program is called by its name, a bit pattern is a name of a little function inside a CPU that got executed when the CPU finds one.

A hardware device may not be a CPU but still has its language. A device with its own machine language is a _programmable device_, since a user can use the language to command the device to perform different actions.

For example, a printer has its set of commands for instructing it how to
print a page.

# Also See:
+ [[assembly language]]