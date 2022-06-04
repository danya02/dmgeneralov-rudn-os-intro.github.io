---
title: Программирование на Intel 8080
subtitle: Пост на тему по выбору на неделю 22

# Summary for listings and search engines
summary: Пост на тему по выбору на неделю 22

# Link this post with a project
projects: []

# Date published
date: '2022-06-04T09:30:00Z'

# Date updated
lastmod: '2022-06-04T09:30:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.

authors:
  - admin

tags:
  - Topical
  - Week 18

categories:
  - Topical
  - Week 18
---

The Intel 8080 was one of the most popular 16-bit microprocessors during the 1980s. It was used in a wide variety of devices, including personal computers, calculators, and even video games.
Its popularity meant that competing processors, like the Zilog Z80, had to be binary-compatible with it in order to succeed on the market.
As such, knowing how to write code for it can help you write code for many different devices.

The easiest way to get started is by using an assembler. An assembler is a program that translates assembly language -- a language that describes the instructions that a computer can execute -- into machine code.
Assembly language is a very simple language that is easy to learn and easy to write. It directly describes the instructions that the processor executes.

The instruction set of the Intel 8080 has somewhere around 200 one-byte instructions, with some taking one or two byte arguments.
These can be seen in an [opcode table](https://www.pastraiser.com/cpu/i8080/i8080_opcodes.html).

Like every processor, it has a program counter, which is a 16-bit register that keeps track of the current location in the program.
It also has a stack pointer, which is a 16-bit register that keeps track of the location of the top of the stack.
These two registers cannot be accessed directly.

There are also the registers B, C, D, E, H and L. These are 8-bit, but they can be accessed as 16-bit registers, called B, D and H, respectively.
The A register is the accumulator, and it is where arithmetic operations work on.
There is also a flags register, F, and together with A they form the PSW (Program Status Word). That can be pushed onto the stack, and popped off of it, which is the main purpose for such a grouping.

Speaking of the stack, it is only possible to push and pop the 16-bit combined registers onto it -- not the individual registers. Together with the fact that the PSW can be pushed and popped, this means that those values can also be manipulated, so one can consider the A and F registers as general-purpose.

The H and L registers are used to store the high and low bytes of a 16-bit address. This address is the memory location that a move instruction will access.
This means that in practical terms, to load or store a value from memory, one must first load an immediate into HL:

```asm
LXI H, 0x8000  ; Load immediate address 0x8000 into HL
MOV A, M       ; Load the value from 0x8000 into A
```

There are no 16-bit arithmetic instructions apart from incrementing and decrementing, which makes it clear that their intended purpose is to store addresses.

Other notable things include a suite of jump commands, which can be used to manipulate the program counter.
These jump commands are:

```asm
JMP  ; jump unconditionally
JZ   ; jump if zero
JNZ  ; jump if not zero
JC   ; jump if carry
JNC  ; jump if not carry
JPE  ; jump if parity even
JPO  ; jump if parity odd
JM   ; jump if negative
JP   ; jump if positive
```

These commands, except for JMP, can be used to branch to a different location in the program. Whether the branch is taken or not depends on the value of the flags register.

All jump instructions have corresponding call and return instructions.
A call instruction pushes the program counter onto the stack, and then sets the program counter to the address specified by the argument, moving into a subroutine.
A return instruction pops the program counter off the stack, and then continues execution from the address that was on top of the stack, returning to the calling routine.
These two types of instructions are used to allow repeating code in a program.

And that's all there is to it.
With these instructions, it is possible to write any program on the Intel 8080.
That program can then be run on a real computer, or on an emulator.