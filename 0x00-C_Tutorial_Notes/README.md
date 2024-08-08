
# 0x00. C - Hello, World Tutorial Notes

Welcome to the "Hello, World" of C programming! In this tutorial, we will embark on a journey through the basics of C, one of the most powerful and enduring programming languages. Whether you're a novice or brushing up on your skills, this guide will help you understand why C is the backbone of modern software engineering.

## Table of Contents
1. [Why C Programming is Awesome](#why-c-programming-is-awesome)
2. [The Origins of C](#the-origins-of-c)
   - [Dennis Ritchie and Brian Kernighan](#dennis-ritchie-and-brian-kernighan)
   - [Linus Torvalds](#linus-torvalds)
3. [What Happens When You Type `gcc main.c`](#what-happens-when-you-type-gcc-mainc)
4. [Understanding the Entry Point](#understanding-the-entry-point)
   - [What is `main`](#what-is-main)
5. [Printing Text in C](#printing-text-in-c)
   - [`printf`](#printf)
   - [`puts`](#puts)
   - [`putchar`](#putchar)
6. [Using the `sizeof` Operator](#using-the-sizeof-operator)
7. [Compiling with `gcc`](#compiling-with-gcc)
   - [Default Program Name](#default-program-name)
8. [C Coding Style and `betty-style`](#c-coding-style-and-betty-style)
9. [Including the Right Headers](#including-the-right-headers)
10. [The `main` Function and Return Values](#the-main-function-and-return-values)
11. [Writing Bash Scripts to Run C Programs](#writing-bash-scripts-to-run-c-programs)
12. [Basic Concepts in C](#basic-concepts-in-c)
    - [Variables](#variables)
    - [Assignments](#assignments)
    - [Data Types](#data-types)

---

## Why C Programming is Awesome

C is like the Latin of programming languages—many modern languages borrow from its syntax and structure. It's fast, efficient, and gives you direct control over your computer’s memory. If you want to understand how computers think and operate, learning C is essential.

## The Origins of C

### Dennis Ritchie and Brian Kernighan

Dennis Ritchie, the creator of C, and Brian Kernighan, who co-authored the classic book *The C Programming Language*, are the architects behind this powerful language. Ritchie developed C in the early 1970s at Bell Labs, and it quickly became the foundation for UNIX, influencing countless other operating systems and languages.

### Linus Torvalds

Linus Torvalds, the creator of Linux, built his famous kernel using C. This choice cemented C's reputation as a language of choice for systems programming.

### What is GNU?

GNU stands for "GNU's Not Unix." It is a recursive acronym, a type of wordplay where the first letter of the acronym stands for the acronym itself. The GNU project was initiated by Richard Stallman in 1983 with the goal of creating a free and open-source operating system that is Unix-compatible but entirely free of any proprietary software.

The GNU operating system, combined with the Linux kernel, forms what is commonly referred to as "GNU/Linux," which is the foundation for many popular distributions, such as Ubuntu, Fedora, and Debian. The GNU project emphasizes the importance of software freedom, advocating that users should have the freedom to run, modify, and share software.

## What Happens When You Type `gcc main.c`

When you type `gcc main.c`, you're invoking the GNU Compiler Collection to transform your human-readable C code into machine code that your computer can execute. This process involves several stages: preprocessing, compiling, assembling, and linking. Each stage converts your code closer to something the machine can understand, culminating in an executable file.

## Understanding the Entry Point

### What is `main`

The `main` function is the entry point of every C program. Think of it as the front door to your house—when you run a program, the operating system knocks on `main` to get things started. Without `main`, your program has no entry point and won't run.

## Printing Text in C

### `printf`

`printf` is like a versatile megaphone for your program. It can print formatted text, numbers, characters, and more. It's highly flexible but requires you to manage the format specifiers correctly (e.g., `%d` for integers, `%s` for strings).

### `puts`

`puts` is a simpler alternative to `printf`. It's like a loudspeaker that only knows how to say one line at a time. It automatically adds a newline at the end of the string it prints.

### `putchar`

`putchar` is even more focused—it only prints a single character. Imagine a typewriter that only types one letter at a time. It's efficient when you only need to output individual characters.

#### Best Use Cases
- Use `printf` when you need to format strings or include variables in your output.
- Use `puts` when you want to quickly print a string with a newline.
- Use `putchar` when you need to print characters one at a time.

## Using the `sizeof` Operator

The `sizeof` operator is like a measuring tape for your data. It tells you how much memory a particular type or variable occupies. This is crucial when managing memory, especially in systems programming.

Example:
```c
int a;
printf("Size of int: %lu bytes\n", sizeof(a));
```

## Compiling with `gcc`

Compiling is the act of turning your source code into an executable program. With `gcc`, this is as simple as:
```bash
gcc main.c -o myprogram
```
Here, `-o` specifies the output file name. If you omit `-o`, the default program name is `a.out`.

### Default Program Name

When you compile a C program without specifying an output name, `gcc` defaults to naming the executable `a.out`. It stands for "assembler output" and harks back to the early days of Unix.

## C Coding Style and `betty-style`

C has a standard coding style that makes your code easier to read and maintain. The `betty-style` tool helps you adhere to these conventions by checking your code for formatting issues.

To check your code:
```bash
betty filename.c
```

## Including the Right Headers

Headers in C are like a toolbox. They contain definitions for functions and macros that you can use in your code. To avoid "undefined reference" errors, always include the correct header.

For example, to use `printf`, include:
```c
#include <stdio.h>
```

## The `main` Function and Return Values

The `main` function’s return value is the program’s exit status, which signals success or failure to the operating system. Returning `0` usually means success:
```c
int main(void)
{
    return 0;
}
```

## Writing Bash Scripts to Run C Programs

Sometimes, you'll want to automate the compilation and execution of your C programs. A simple Bash script can help with this.

Example `run.sh` script:
```bash
#!/bin/bash
gcc main.c -o myprogram
./myprogram
```
Make it executable:
```bash
chmod +x run.sh
```
Now you can run your program with a single command:
```bash
./run.sh
```

## Basic Concepts in C

### Variables

Variables are like containers that store data. You need to declare a variable before you can use it:
```c
int age = 25;
```

### Assignments

Assignment is the process of giving a value to a variable:
```c
age = 30;
```

### Data Types

C is a statically-typed language, which means every variable has a type that dictates what kind of data it can hold (e.g., `int` for integers, `char` for characters).

---

By following this tutorial, you'll gain a solid foundation in C programming. Remember, practice is key to mastering any language, so don't hesitate to experiment with the examples provided!

Happy coding!

---

This README.md file will serve as a comprehensive guide for students to refer to as they learn the basics of C programming.