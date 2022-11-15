# Programming

## Compiler

- What is compiler?
  In computing, a compiler is a computer program that translates computer code written in one programming language (the source language) into another language (the target language). The name "compiler" is primarily used for programs that translate source code from a high-level programming language to a lower level language (e.g. assembly language, object code, or machine code) to create an executable program

- Why is compiler needed?
  Because computer can't understand the source code directly. It will understand only object level code. Source codes are human readable format but the system cannot understand it. So, the compiler is intermediate between human readable format and machine-readable format

## What is thread?

In computer science, a thread of execution is the smallest sequence of programmed instructions that can be managed independently by a scheduler, which is typically a part of the operating system.

## What is the difference between Single-thread and Multi-thread?

- **Single threaded** processes contain the execution of instructions in a single sequence. In other words, one command is processes at a time.
- **Multi threaded** allow the execution of multiple parts of a program at the same time. These are lightweight processes available within the process. Share code, data, file.
- Advantages of Multithreaded:
  - Share its resources such as memory, data, files etc
  - Economical to use threads as they share the process resources
  - Program responsiveness allows a program to run even if part of it is blocked using multithreading. This can also be done if the process is performing a lengthy operation
- Disadvantages of Multithreaded:
  - Difficulty of writing code
  - Difficulty of debugging
  - Difficulty of managing concurrency
  - Difficulty of testing
  - Difficulty of porting existing code

## Languages

- C/C++ (**compiled**)
  Preprocessing: get source, delete notes or comments
  Compilation: source -> assembly code
  Assembling: assembly code -> object code files (Ex: 010011010101)
  Linker: object code files -> shared library, executable file - Advantages: - a low-level language that easily communicates with hardware - Disadvantages: - Object-orientated programming languages have several security issues which means that programs written in C++ aren't as safe as others - Cannot support built-in code threads - The pointers that are used in C++ take up a lot of memory which is not always suitable for some devices

- Java (**compiled**)
  Need JVM
  //Biên dịch và thông dịch - Advantages: - JVM makes java can run on many different platforms - easy to understand high language - security because pointers are not used - Disadvantages: - low performance - long and complex code

- Javascript (**interpreted** - V8 compiled)
  - Advantages:
    - interpreted
    - simple syntax
    - Limited server interaction
  - Disadvantages:
    - security
- Why Javascript?
  - UI interface
  - Server-side code: Node.js
  - Mobile: ReactNative
  - API

## Software design pattern

- Backend
- Frontend
