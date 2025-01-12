<div id="user-content-toc"><ul><summary list-style-type: none;>

## C-programming-notes 📓

</ul></summary>
</div>

## Intro

Welcome to my GitHub repository dedicated to my journey of learning and mastering C programming! 🖥️🚀

Here, you'll find a collection of my notes, code snippets, and practice exercises as I explore the fundamentals and advanced concepts of C. This repository serves as both a study companion and a resource for anyone else diving into this powerful and timeless programming language.: 
Notes are based on following source material:

<div>
<img src='https://img.shields.io/badge/C Programming-%2300599C.svg?style=for-the-badge&logo=logoColor=white'/>
<img src='https://img.shields.io/badge/ChatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white' />
<img src='https://img.shields.io/static/v1?style=for-the-badge&message=Wikipedia&color=000000&logo=Wikipedia&logoColor=FFFFFF&label=' />
<img src='https://img.shields.io/static/v1?style=for-the-badge&message=W3Schools&color=04AA6D&logo=W3Schools&logoColor=FFFFFF&label=' />
<img src='https://img.shields.io/static/v1?style=for-the-badge&message=YouTube&color=FF0000&logo=YouTube&logoColor=FFFFFF&label=' />
</div>

## Menu

* [Introduction](#introduction)
  - [Why C?](#why-c)
  - [History](#history)
* [First program](#first-program)
  - ["Hello World!"](#hello-world)
  - [Compiling](#compiling)
* [Basic Program Structure](#basic-program-structure)
  - [Block, Statement, Whitespace and Scope](#block-statement-whitespace-scope)
  - [Basic Functions](#basic-functions)
  - [Standard Library](#standard-library)


# Introduction

### Why C

C is mostly used for writting OS. The first OS written in C was Unix(Linux is also written in C). Most high-level programming languages are written in C (PHP, Perl, Python, Ruby).

C language combines universality and portability across various computer architectures while retaining most of the control of the hardware provided by assembly language.

C is compiled language, it is small: a C statement usually translates to a few assembly instructions, while most additional functionality comes from library functions.

C is designed for portability, performance, and minimal resource usage, making it ideal for systems like operating systems and embedded systems. Its explicit coding style helps programmers understand what each line does. Known for its efficiency and low-level capabilities, C is the native language of UNIX, highly portable, stable, and widely used. It allows direct memory manipulation through constructs like pointers and arrays, giving programmers control over memory layout and dynamic allocation, though deallocation must be managed manually.

### History

Programming languages timeline:

<dl>
  
  <dt><h3>1950s</h3></dt>
  
   <dt>1957 - Fortran (Formula Translation):</dt>
<ul>
  <li>Developed by IBM and led by John Backus.</li>
  <li>The first high-level programming language designed for scientific and engineering computations.</li>
</ul>
   <dt>1958 - Algol (Algorithmic Language):</dt>
 <ul>
   <li>Created by an international committee.</li>
   <li>Introduced structured programming and was influential in the development of many future languages.</li>
 </ul>

   <dt><h3>1960s</h3></dt>
  <dt>1960 - COBOL (Common Business-Oriented Language):</dt>
<ul>
  <li>Developed for business, finance, and administrative systems.</li>
<li>Known for its readability and use in enterprise applications.</li>
</ul>

   <dt>1964 - BASIC (Beginner's All-purpose Symbolic Instruction Code):</dt>
  <ul>
    <li>Created by John G. Kemeny and Thomas E. Kurtz.</li>
    <li>Aimed to simplify programming for students and beginners.</li>
  </ul>
  
  <dt>1967 - BCPL (Basic Combined Programming Language):</dt>
  <ul>
    <li>Designed by Martin Richards.</li>
    <li>A precursor to the C language, focusing on simplicity and portability.</li>
  </ul>

   <dt>1968 - Algol 68:</dt>
  <ul>
    <li>A successor to Algol, introducing more advanced features but criticized for its complexity.</li>
    <li>Influenced languages like Pascal and C.</li>
  </ul>

  <dt><h3>1970s</h3></dt>
  
  <dt>1970 - Pascal:</dt>
  <ul>
    <li>Developed by Niklaus Wirth.</li>
    <li>Designed for teaching structured programming and data structuring.</li>
  </ul>

  <dt>1972 - C:</dt>
<ul>
  <li>Developed by Dennis Ritchie at Bell Labs.</li>
   <li>Evolved from B (a derivative of BCPL) and included features like structured programming, efficient low-level memory manipulation, and portability.</li>
   <li>Became the foundation for many modern programming languages and operating systems, including UNIX.</li>
</ul>

</dl>

# First Program

### "Hello world!"

File extension for programs written in C: eg.: **hello.c**<br>
<code>#include <stdio.h>
int main(void)
{
printf("Hello, World!\n");
return 0;
}
</code>

What does each line mean?<br>
<code>#include <stdio.h>
</code>

This is a preprocessor directive. Preprocessor directives gives instructions to a part of the compiler to modify the code before it is compiled. 
**#include** directive retrieves C code from the standard **stdio.h** file(header files, which have **.h** extension). It works like library. From that library we need only function **printf**. <br>

<code>int main(void)</code>

It could be only one **main()** function because it acts as the starting point of all C programs.<br>

<code>printf("Hello World!\n");</code>

This line produces the actual output on the console(terminal in UNIX environment).<br>

<code>return 0;</code>

When ending a program, we use an exit status to inform the operating system whether the program ran successfully. An exit status of <code>0</code> signals success, while other integers can represent different types of errors. This practice of using exit codes is a long-standing convention.

### Compiling

For compiling in UNIX environment(GCC must be installed) the command is: <br>

<code>gcc example.c</code>

To run the program:<br>

<code>./a.out</code>

The result will be **Hello, World!**. 
To show the exit status of the last program, run:<br>

<code>echo $</code>
This shows the value the main function has returned, which is 0 in the above example.

One more way to compile and run the program is:<br>

<code>gcc -o -Wall testing example.c</code>

<code>-o</code>

If you want the output to have a name other than **./a.out**. In this case it will get a new name **testing**. So, for runninng the program command will be: <br>

<code>./testing</code><br>

<code>-Wall</code>

It indicates that gcc should generate warnings about various types of suspicious code that are likely to be incorrect. These warnings help identify potential issues in your code, such as logical errors, bad practices, or possible bugs, even if the code compiles successfully.

# Basic Program Structure

### Block, Statement, Whitespace and Scope


C does not have complete block structure but it's still important to understand what block is. A **block** consists of executable statements. **Statements** are the pieces of text that the compiler translates into executable instructions, along with the surrounding **whitespace**:<br>

<code>int num = 5;</code>

This declares a variable of type *integer*, initializes it to the *value* 5, which can be later
accessed with the *identiﬁer* 'num'.

A block of code has opening brace <code>{</code> and closing <code>}</code> Blocks can contain other blocks and they can contain their blocks. Example:<br>

<code>int main(void)
{
/* this is a 'block' */
int num = 5;
{
/* this is also a 'block', nested inside the outer block */
int numTwo = 6;
}
return 0;
}</code>

The compiler ignores whitespace (except when it separates e.g. return from <code>0</code>). To orginize code in more readable form it is common to use spaces (or tabs) to organize source code.

**Scopes** define the visibility of data or functions within a program. In C, there are two types of scopes: **local** and **global**. A global entity is accessible from anywhere in the program, while a local entity is limited to the block in which it is declared. Example: <br>

<code>int num = 5; /* 'global' variable,can be accessed from anywhere in the program */

/* function, all variables inside of it
are "local" to the function. */
int main(void)
{
int num = 6; /* 'num' now equals 6 */
printf("%d\n", num); /* prints a '6' instead of the global variable of 'num',5 */
return 0;
}</code>

### Basic Functions

A **function** is a block of reusable code that performs a specific task. 

Advantages of Using Functions:
<ul>
  <li><ins>Code Reusability:</ins> Write once, reuse multiple times.</li>
   <li><ins>Modularity:</ins> Breaks down complex programs into smaller, manageable chunks.</li>
   <li><ins>Improved Debugging:</ins> Easier to test and debug individual parts.</li>
   <li><ins>Ease of Maintenance:</ins> Simplifies updating and maintaining the code.</li>
</ul>

Requesting a function to perform its task is called a **function call**. Functions often need data from the caller to work; these are called **arguments**. After completing its task, a function may send a result back to the caller, known as the return value.

**Before calling a function:**

<ul>
  <li>What the function does;</li>
  <li>The data type of the arguments and what they mean;</li>
  <li>The data type of the return value and what it means;</li>
</ul>

Return value could be a result of computatyion or indication whether a function successfuly completed its work. 

### Standard Library

In **1983**, as C was being standardized, the **American National Standards Institute (ANSI)** created a committee to define a standard version of C, known as **ANSI C**. This standard included a basic set of common functions, called the **Standard Library**, which provides tools for tasks like input/output, string manipulation, math, file handling, and memory management. However, it excludes hardware- or OS-specific functions, such as those for graphics, sound, or networking. 




















