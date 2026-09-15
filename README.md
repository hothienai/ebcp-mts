# Embedded C Programming Mentorship Program

## Overview

🚀 The Embedded C Programming Mentorship Program is a practical introduction to C programming in the context of real microcontroller development. It combines core C language concepts with the daily workflow of an embedded engineer: configuring a toolchain, building and debugging firmware, using Git for collaboration, and validating code on STM32 hardware.

This is not a complete survey of the C language. The course focuses on the parts of C that students will use to read, write, debug, and maintain embedded firmware. Every chapter is paired with a hands-on exercise, and examples are intended to be built, flashed, and observed on a development board.

<img src="/ebcp-mts.png" alt="Embedded C Programming Mentorship Program"/>

## Learning Outcomes

🎯 By the end of the program, students will be able to:

- Explain how C source code is compiled, linked, loaded, and executed on a microcontroller.
- Write clear C programs using appropriate types, operators, control flow, functions, pointers, arrays, and structures.
- Apply embedded-C practices including `const`, `volatile`, fixed-width integer types, bitwise operations, memory awareness, and defensive use of pointers.
- Set up and use STM32CubeIDE, STM32CubeMX, the ARM GNU Toolchain, and ST-LINK debugging tools.
- Build, flash, pause, step through, inspect, and troubleshoot firmware on an STM32 board.
- Use Git and GitHub for version control and team collaboration, including branches, commits, pull requests, reviews, and merge-conflict resolution.

## Who This Course Is For

✅ This course is intended for students and early-career engineers who are new to embedded C, microcontroller development, or collaborative firmware projects. Basic programming experience is helpful but not required. A willingness to compile, debug, and investigate failed experiments is essential.

## Prerequisites

- A computer with permission to install development tools.
- A GitHub account for repository access and collaboration.
- An STM32 development board and a USB data cable.
- Recommended: an STM32 Nucleo-F401RE, which matches the STM32F401 projects in this repository.

Other STM32F4 Nucleo boards may be used, but their pin configuration, clock setup, and generated project files can differ.

## Required Tools

### STM32 Development Toolchain

Create an ST account before downloading ST software.

- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html): IDE, compiler integration, build tools, and debugger.
- [STM32CubeMX](https://www.st.com/en/development-tools/stm32cubemx.html): graphical configuration tool used to generate STM32 initialization code.
- [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html): utility for programming and inspecting STM32 devices.
- [ST-LINK tools and drivers](https://www.st.com/en/development-tools/st-link-v2.html): debugger/programmer support. Nucleo boards include an onboard ST-LINK debugger.
- [GNU Arm Embedded Toolchain](https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads): useful when building outside STM32CubeIDE or inspecting the toolchain directly.

### Version Control and Collaboration

- [Git](https://git-scm.com/downloads): distributed version-control system used for source history and collaboration.
- [GitHub](https://github.com/): repository hosting, pull requests, issues, and code review.
- [Visual Studio Code](https://code.visualstudio.com/): recommended editor for reviewing code and working with Git.
- [Git Graph for VS Code](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph): optional visual history and branch browser.
- [TortoiseGit](https://tortoisegit.org/download/): optional Windows Git client.

## Hardware

The recommended target is the [STM32 Nucleo-F401RE](https://www.st.com/en/evaluation-tools/nucleo-f401re.html). It provides an STM32F401RE microcontroller, onboard ST-LINK debugging, a USB connection, and accessible I/O headers for experiments.

You will also need a USB data cable compatible with the board's ST-LINK connector. Use a data-capable cable; some USB cables provide power only and cannot program or debug the board.

## Working Method

Each lesson follows the same engineering loop:

1. Read the focused C or embedded-systems concept.
2. Implement a small change in the matching project.
3. Build the firmware and address compiler warnings or errors.
4. Flash and debug the program on the STM32 board.
5. Observe the hardware result and explain the behavior.
6. Commit the completed work to a Git branch and share it through a pull request when working as a team.

Students should make small, descriptive commits. A useful commit explains the intent, for example: `Add GPIO output exercise` rather than `Update files`.

## Git Collaboration Expectations

The course uses Git as an engineering practice, not only as a backup mechanism. Students will learn to:

- Clone the course repository and keep a local branch synchronized with the remote.
- Create a focused branch for each exercise or feature.
- Review `git status` and `git diff` before committing.
- Write concise commit messages that describe the change.
- Push branches and open pull requests on GitHub.
- Respond to review feedback and resolve simple merge conflicts.

Do not commit generated build outputs, temporary IDE files, or credentials. Commit source files, configuration required to reproduce the project, and concise documentation.

## Course Roadmap

The schedule below is a guide. The mentorship can move more slowly where students need additional practice with the debugger, hardware, or a particular C concept.

### 🔑 Chapter 0 - Development Environment and Workflow

Estimated time: 2 hours

- Install STM32CubeIDE, ST-LINK support, Git, and Visual Studio Code.
- Create or configure an STM32 project with STM32CubeMX.
- Identify the source, header, linker-script, startup, and generated-code areas of a firmware project.
- Build, flash, and debug a baseline program on the board.
- Clone the repository, create a branch, make a commit, and push it to GitHub.

### 🔑 Chapter 1 - Getting Started with Embedded C

Estimated time: 3 hours

1. The first embedded C program
2. Variables and arithmetic expressions
3. `for` statements
4. Symbolic constants
5. Arrays
6. Functions
7. Arguments and pass by value
8. External variables and scope

### 🔑 Chapter 2 - Types, Operators, and Expressions

Estimated time: 5 hours

9. Variable names and naming conventions
10. Data types and sizes
11. Constants and literals
12. Declarations
13. Type qualifiers: `const` and `volatile`
14. Arithmetic operators
15. Relational and logical operators
16. Type Conversions 
17. Increment and decrement operators
18. Bitwise operators
19. Bit-shift operators
20. Assignment operators and expressions
21. Conditional expressions
22. Precedence and order of evaluation

### 🔑 Chapter 3 - Control Flow

Estimated time: 3 hours
    
23. Statements and blocks
24. `if`, `else if`, and `else`
25. `switch` statements
26. `while` and `for` loops
27. `do`-`while` loops
28. `break` and `continue`

### 🔑 Chapter 4 - Functions and Program Structure

Estimated time: 3 hours
    
29. Function fundamentals
30. External variables
31. Header files and interfaces
32. Static variables and functions
33. Initialization
34. Recursion and embedded constraints
35. The C preprocessor

### 🔑 Chapter 5 - Pointers and Arrays

Estimated time: 3 hours
    
36. Pointers and addresses
37. Pointers and function arguments
38. Pointers and arrays
39. Address arithmetic
40. Character pointers and functions
41. Pointer arrays and pointers to pointers
42. Multidimensional arrays
43. Initialization of pointer arrays
44. Pointers returned from functions
45. Function pointers
46. Complex declarations

### 🔑 Chapter 6 - Structures and Data Representation

Estimated time: 5 hours
    
47. Structure fundamentals
48. Structures and functions
49. Arrays of structures
50. Pointers to structures
51. `typedef`
52. Unions
53. Pointers to unions
54. Structure & Unions size
55. Bit-fields
56. Enumerations

### 🔑 Chapter 7 - Embedded C Review and Applied Practice

Estimated time: 3 hours
 
57. `volatile` and hardware registers
58. Type casting and conversion risks
59. The stack and call stack
60. Null pointers
61. Padding bytes and alignment
62. Divide by zero
63. Pass by reference
64. Function pointers: call to unknown functions
65. Callbacks
66. Void pointer 
67. Software Design and Code optimization

## Recommended References

- [The C Programming Language, Second Edition](): classic reference for C language fundamentals.
- [STM32F401xD/E Reference Manual (RM0368)](https://www.st.com/resource/en/reference_manual/rm0368-stm32f401xbc-and-stm32f401xde-advanced-armbased-32bit-mcus-stmicroelectronics.pdf): authoritative reference for the STM32F401 peripherals and registers.
- [STM32F401RE Product Page](https://www.st.com/en/microcontrollers-microprocessors/stm32f401re.html): datasheet, documentation, and device resources.
- [Pro Git](https://git-scm.com/book/en/v2): free reference for Git concepts and collaboration workflows.

## Evidence of Completion

Students complete the program by maintaining a GitHub repository containing their exercises, meaningful commits, and a final hardware demonstration. The final review should show that the student can explain the code path from C source to observed board behavior, use the debugger to inspect a fault or unexpected result, and collaborate through a pull request.