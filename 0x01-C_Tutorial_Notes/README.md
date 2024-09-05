---

# 0x01. C - Variables, if, else, while Tutorial Notes

Welcome to the "0x01. C - Variables, if, else, while Tutorial Notes." This tutorial is tailored for software engineering students, providing a comprehensive introduction to basic C programming concepts, with a focus on variables, operators, conditional statements, and loops. Let's dive into why C programming is powerful and explore its foundational elements!

## Table of Contents
- [Introduction](#introduction)
- [Basics of C Programming](#basics-of-c-programming)
  - [Variables](#variables)
  - [Assignments](#assignments)
  - [Data Types](#data-types)
- [Operators in C](#operators-in-c)
  - [Arithmetic Operators](#arithmetic-operators)
  - [Logical Operators](#logical-operators)
  - [Relational Operators](#relational-operators)
  - [Boolean Operators](#boolean-operators)
- [Conditional Statements](#conditional-statements)
  - [If and If...Else Statements](#if-and-ifelse-statements)
- [Loops](#loops)
  - [Using While Loops](#using-while-loops)
- [Printing Variables](#printing-variables)
- [The ASCII Character Set](#the-ascii-character-set)
- [GCC Flags: -m32 and -m64](#gcc-flags--m32-and--m64)
- [Bonus: Scripting C Programs with Bash](#bonus-scripting-c-programs-with-bash)
  - [Example Script](#example-script)
- [Conclusion](#conclusion)

---

## Introduction

C is often referred to as the "mother of all programming languages." It is foundational, close to the hardware, and has a profound influence on modern programming languages. Mastering C equips you with a deep understanding of how software interacts with hardware.

In this tutorial, we will:
- Explore C basics like variables, operators, and loops.
- Learn how to use conditional statements.
- Practice compiling and running C code using the GCC compiler.
- Understand how to automate code checking and compilation with a bash script.

## Basics of C Programming

### Variables

Variables are placeholders used to store data. Think of them as labeled boxes that hold different types of information in your program.

```c
/* Declaring variables of different types */
int age = 25; /* An integer variable */
char initial = 'A'; /* A character variable */
unsigned int count = 100; /* An unsigned integer variable */
```

### Assignments

Assignments are how you give values to variables.

```c
/* Assigning values to variables */
int score;
score = 85; /* Assigning 85 to the variable score */
```

### Data Types

C offers several data types to manage different kinds of information. Here are some common ones:

- `int`: For integers.
- `char`: For single characters.
- `unsigned int`: For non-negative integers.

## Operators in C

Operators are symbols that perform operations on variables and values.

### Arithmetic Operators

Arithmetic operators are used for mathematical calculations. They include:
- `+` (Addition)
- `-` (Subtraction)
- `*` (Multiplication)
- `/` (Division)
- `%` (Modulus)

Example:

```c
int a = 10, b = 5;
int sum = a + b; /* Adds a and b */
```

### Logical Operators

Logical operators help make decisions based on conditions:
- `&&` (Logical AND)
- `||` (Logical OR)
- `!` (Logical NOT)

Example:

```c
int x = 1, y = 0;
if (x && !y) {
    /* This block runs because x is TRUE and y is FALSE */
}
```

### Relational Operators

These operators compare values:
- `==` (Equal to)
- `!=` (Not equal to)
- `<` (Less than)
- `>` (Greater than)
- `<=` (Less than or equal to)
- `>=` (Greater than or equal to)

Example:

```c
if (a > b) {
    /* Executes if a is greater than b */
}
```

### Boolean Operators

In C, values `0` and `1` are used to represent `FALSE` and `TRUE`, respectively.

## Conditional Statements

Conditional statements allow your code to make decisions.

### If and If...Else Statements

- **`if` Statement**: Executes a block of code if a specified condition is true.
- **`if...else` Statement**: Provides an alternative block of code if the condition is false.

Example:

```c
int num = 10;
/* Checking if the number is positive */
if (num > 0) {
    /* Code runs if num is greater than 0 */
} else {
    /* Code runs if num is not greater than 0 */
}
```

## Loops

Loops allow you to execute a block of code multiple times.

### Using While Loops

`while` loops execute as long as a condition is true.

Example:

```c
int count = 0;
/* Loop will run as long as count is less than 5 */
while (count < 5) {
    count++; /* Increment count */
}
```

## Printing Variables

Use `printf` to print the values of variables.

```c
/* Printing integer and character variables */
int age = 20;
char grade = 'A';
printf("Age: %d, Grade: %c\n", age, grade);
```

## The ASCII Character Set

ASCII is a character encoding standard that assigns a number to each character.

- Characters range from 0 to 127.
- Example: `'A'` is 65, `'a'` is 97.

## GCC Flags: -m32 and -m64

These flags tell GCC which mode to compile the code in:
- `-m32`: Compiles in 32-bit mode.
- `-m64`: Compiles in 64-bit mode.

## Bonus: Scripting C Programs with Bash

### Example Script

Below is a script that prompts the user for filenames, checks code style with Betty, compiles with GCC, and runs the executable if everything passes.

```bash
#!/bin/bash

# Prompt the user for the input C filename
echo "Enter the name of the C file (e.g., main.c):"
read input_file

# Prompt the user for the output filename
echo "Enter the desired output filename (e.g., output):"
read output_file

# Check the C file with the Betty linter
betty "$input_file"
if [ $? -eq 0 ]; then
    # Compile the C file with gcc if Betty check passes
    gcc -Wall -pedantic -Werror -Wextra -std=gnu89 "$input_file" -o "$output_file"
    echo "Compilation successful!"
    # Run the compiled output file
    ./"$output_file"
else
    # Print an error message if Betty checks fail
    echo "Betty checks failed."
fi
```

### Explanation of the Script

1. **Shebang (`#!/bin/bash`)** tells the system to use the bash shell.
2. `echo` prints prompts to the user.
3. `read` takes user input for filenames.
4. `betty "$input_file"` checks the file style.
5. `gcc` compiles the file with strict flags.
6. The script runs the executable if the check passes or prints an error if it fails.

**Note**: Ensure [Betty linter](https://github.com/alx-tools/Betty.git) and [GCC](https://www.linkedin.com/pulse/how-install-gcc-complete-guide-macos-windows-linux-solomon-okomowho-fixbf) are installed on your machine.

## Conclusion

Understanding the basics of C, from operators to loops and conditionals, is a powerful skill. You can manipulate data, make decisions, and repeat actions efficiently. By leveraging bash scripts, you can automate repetitive tasks and streamline your coding process.

---

This tutorial aims to build a strong foundation in C programming and instill best practices early on. Happy coding!