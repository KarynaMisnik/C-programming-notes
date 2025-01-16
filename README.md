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
  - [Block, Statement, Whitespace and Scope](#block-statement-whitespace-and-scope)
  - [Basic Functions](#basic-functions)
  - [Standard Library](#standard-library)
* [C Compilation](#c-compilation)
* [Variables](#variables)
  - [Declaring, Initializing and Assigning Variables](#declaring-initializing-and-assigning-variables)
  - [Data Types](#data-types)
  - [Data Type Modifiers](#data-type-modifiers)
  - [Const Qualiﬁer](#const-qualiﬁer)
  - [#define](#define)
  - [static](#static)
  - [extern](#extern)
  - [volatile](#volatile)
  - [auto](#auto)
  - [register](#register)
  - [Modifiers summary](#modifiers-summary)
* [Error handling](#error-handling)
  - [Division by zero](#division-by-zero)
  - [Signals](#signals)
  - [setjmp](#setjmp)


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

# C Compilation

Compilation in C programming is the process of converting your written code into a program that the computer can run. Here's how it works, step by step:

1. **Writing the Code:** You write your program in a text file with a **.c** extension (e.g., <code>program.c</code>).

2.  **Preprocessing:** The compiler processes your code to handle things like **#include** and **#define**. This step prepares the code for compilation by expanding macros and including header files.

3. **Compiling:** The compiler translates your C code into assembly code, which is a low-level language that the computer can understand.

4. **Assembling:** The assembler converts the assembly code into machine code (binary instructions), creating an object file (<code>.o</code> or <code>.obj</code>).

5. **Linking:** The linker combines your object file with necessary libraries (e.g., the Standard Library) to create the final executable program.

6. **Executable File:** The result is an executable file (e.g., <code>program.exe</code> or <code>./program</code>), which you can run on your computer.


|<img src='https://github.com/user-attachments/assets/4f75d0ca-59e9-4483-b71e-3c961016b048' alt="c compiler process scheme">|
|:--:|
| *C Compilation Scheme* |


# Variables

In C, variables are names that refer to memory locations where values are stored. We can think of a variable as a placeholder for a value. For example, if a variable i is set to *4*, then *i + 1* equals *5*.

Before using a variable in C, you must <ins>declare</ins> it. Declaring a variable tells the program how many variables you need, their names, and how much memory they require.

Each variable has a <ins>type</ins>, which defines what kind of data it can hold (e.g., integer, float, etc.) and how much memory it needs. The size of a type depends on the hardware and compiler being used, as C is a low-level language.

In C, all variables <ins>*must be assigned*<ins> a specific type when they are declared.

### Declaring, Initializing and Assigning Variables

<dl>
  <dt><h3>Step 1:</h3> Declare the variable</dt>
  Define the variable by specifying its type and name. 
</dl>
<code>int number;</code>
<br>

> At this point, memory is reserved for the variable, but no value is assigned to it.

<dl>
  <dt><h3>Step 2:</h3> Initialize the variable</dt>
  Assign an initial value to the variable when you declare it.
</dl>
<code>int number = 10;</code>
<br>

>This combines declaration and initialization, giving the variable a value of <code>10</code>.

<dl>
  <dt><h3>Step 3:</h3> Assign a new value to the variable</dt>
  If needed, you can change the value of the variable later in the program.
</dl>
<code>number = 20;</code>
<br>

>Now, the value of number is updated to 20.

**Summary:** <br>

<code>#include <stdio.h>
int main() {
    int number;       // Step 1: Declare
    number = 10;      // Step 2: Initialize
    number = 20;      // Step 3: Assign a new value
    printf("The value of number is: %d\n", number); // Output: 20
    return 0;}
</code>

### Data Types

They are four basic data types: **int**, **char**, **float**, and **double**.

**int (Integer):**
<ul>
  <li>Stores whole numbers (no decimal point).</li>
  <li>Size: Typically 4 bytes (varies by system).</li>
  <li>Range: Usually -2,147,483,648 to 2,147,483,647.</li>
</ul>
  Example:<br>

  <code>int age = 25;</code>

  **char (Character):**

  <ul>
    <li>Stores a single character or ASCII value.</li>
    <li>Size: 1 byte.</li>
    <li>Range: -128 to 127 or 0 to 255 (depending on system).</li>
  </ul>
Example:<br>

<code>char grade = 'A';</code>

>**Note:** For characters **' '** are used. 

**float (Floating Point):**

<ul>
    <li>Stores decimal numbers with single precision</li>
    <li>Size: Typically 4 bytes.</li>
    <li>Range: Approximately ±3.4e−38 to ±3.4e38.</li>
  </ul>

  Example<br>

  <code>float temperature = 36.5;</code>

**double (Double Precision Floating Point):**

<ul>
    <li>Stores decimal numbers with double precision (more accuracy than float).</li>
    <li>Size: Typically 8 bytes.</li>
    <li>Range: Approximately ±1.7e−308 to ±1.7e308.</li>
  </ul>
Example:<br>

<code>double pi = 3.141592653589;</code>


The **sizeof** ~~function~~ operator in C is used to determine the size (in bytes) of a data type or a variable in memory. It is a compile-time operator that returns an unsigned integer representing the size.

Syntax:<br>

<code>sizeof(type);
sizeof(variable);</code>

Example:<br>

<code>int a = 10;
printf("%zu\n", sizeof(int));     // Size of int type
printf("%zu\n", sizeof(a));       // Size of variable a</code>

>Note: In C, **%zu** is a format specifier used with printf to print values of type **size_t**, which is an unsigned integer type used to represent the size of objects in bytes.
>The sizeof operator returns a value of type **size_t**, so **%zu** is the correct way to print it.
**%zu** ensures portability and avoids warnings or errors when printing the result of sizeof on different platforms.

**Key Points:**

<ul>
  <li>Useful for portability across systems.</li>
  <li>Works with all data types, arrays, pointers, and structures.</li>
  <li>The result depends on the system architecture (e.g., 32-bit vs 64-bit).</li>
</ul>
   
### Data Type Modifiers

In C, long and short are modifiers that adjust the memory size of a data type:

<ul>
  <li><b>short:</b> Uses less memory than int (typically 2 bytes, range: -32,768 to 32,767).</li>
  <li><b>long:</b> Uses more memory than int (typically 4 or 8 bytes).</li>
  <li>Memory sizes are not fixed but follow the rule:
    <code>sizeof(short) <= sizeof(int) <= sizeof(long).</code></li>
</ul>
  
Modern compilers also support **long long**, which is typically 8 bytes.


**Unsigned and Signed Modifiers:**
<ul>
  <li><b>unsigned:</b> Makes a variable store only <i>positive</i> values, doubling its range.</li>
</ul>

Example: For unsigned short, the range is <code>0</code> to <code>65,535</code>.

<ul>
  <li><b>signed:</b> Allows both <i>positive</i> and <i>negative</i> values (default for most types except char).</li>
</ul>

Example: For signed int, the range is <code>-2,147,483,648</code> to <code>2,147,483,647</code>.

**Key Points:**

<ul>
  <li>unsigned and signed can be used with any integer type.</li>
  <li>If the type is omitted, <coe>int</coe> is assumed (e.g., unsigned means <code>unsigned int</code>).</li>
</ul>
    
### Const Qualiﬁer


The **const qualifier** in C is used to declare variables whose values <ins>cannot be changed</ins> after they are initialized. This ensures the variable remains constant throughout the program.

**Why use const?**

<ul>
  <li>Prevent accidental modification of important values.</li>
  <li>Enable small optimizations by the compiler, as it knows the value won't change.</li>
  <li>Improve code clarity and safety by clearly indicating which values are constant.</li>
</ul>

   Example:<br>
   
<code>#include <stdio.h>

int main() {
    const double pi = 3.14159;  // Declare and initialize a constant variable

    printf("The value of pi is: %f\n", pi);

    // Attempting to modify the value will cause a warning or error
    // pi = 3.14;  // Uncommenting this line will cause a compilation error or warning

    return 0;
}</code>
    
    
### #define

What is <code>#define</code> in C?

**#define** is a <ins>preprocessor directive</ins> in C used to define *constants* or *macros*. It allows you to assign a name to a value or code snippet, which the compiler replaces throughout the program during preprocessing (before compilation).

Syntax:<br>

<code>#define NAME value</code>

**NAME:** The identifier (constant or macro name).
**value:** The value or code snippet that NAME represents.

How to Use <code>#define</code>

Defining Constants: Use **#define** to create symbolic constants to make your code more readable and maintainable.

Example:<br>

<code>#include <stdio.h>

#define PI 3.14159

int main() {
    double area, radius = 5.0;
    area = PI * radius * radius;  // PI is replaced with 3.14159
    printf("Area of the circle: %.2f\n", area);
    return 0;
}</code>

Creating Macros: Use **#define** to create macros, which are code snippets or expressions.

Example:<br>

<code>#include <stdio.h>

#define SQUARE(x) ((x) * (x))  // Macro to calculate the square

int main() {
    int num = 4;
    printf("Square of %d is %d\n", num, SQUARE(num));
    return 0;
}</code>

Key Points:
<ul>
  <li>No memory usage: #define values are replaced at compile time, so they do not use memory.</li>
  <li>No type checking: Unlike const, #define does not have a data type, and it doesn't follow scope rules.</li>
  <li>Parentheses are important for macros: Always wrap macro parameters and expressions in parentheses to avoid precedence issues.</li>
</ul>
    
**Pros:**
<ul>
  <li>Makes the code more readable.</li>
  <li>Easy to change values in one place without searching throughout the code.</li>
</ul>

**Cons:**
<ul>
  <li>No type checking (prone to errors in complex macros).</li>
  <li>Harder to debug as they are replaced during preprocessing.</li>
</ul>

   ### static

The static keyword has two main purposes:

**Static Linkage** (for global variables and functions):
<ul>
  <li>When a global variable or function is declared as static, it can only be accessed within the file where it is defined.</li>
  <li>This means it is "hidden" from other files in the project, making it private to that file.</li>
</ul>
        
**Static Storage Duration** (for local variables):
<ul>
  <li>When a local variable is declared as static, it is created only once and retains its value even after the function or block ends.
  </li>
  <li>Unlike global variables, it can only be accessed within its defined scope.</li>
</ul>
        
Example:<br>

<code>#include <stdio.h>
void increment() {
    static int value = 0;  // Retains its value between calls
    value++;
    printf("Value: %d\n", value);
}
int main() {
    increment();  // Output: Value: 1
    increment();  // Output: Value: 2
    increment();  // Output: Value: 3
    return 0;
}
</code>

### extern

The <code>extern</code> keyword is used to declare a variable that is defined in another file. It does not allocate memory for the variable but tells the compiler that the variable exists somewhere else in the program.


Example:<br>

|file 1: <code>main.c</code>|file 2: <code>data.c</code>|
|----|----|
|#include <stdio.h><br> // Declare the external variable<br> extern int sharedVar;<br> int main() {<br> printf("Value of sharedVar: %d\n", sharedVar);<br> return 0;<br>}|// Define the variable<br> int sharedVar = 42;<br>  // Actual memory is allocated here|

|bash|yaml|
|----|----|
|gcc main.c data.c -o program<br>./program|Value of sharedVar: 42|

How It Works:
<ul>
  <li><b>data.c</b> defines sharedVar and allocates memory for it.</li>
   <li><b>main.c</b> uses extern to declare the same variable so the compiler knows it exists and can use it.</li>
   <li>The linker connects the declaration in <b>main.c</b> with the definition in <b>data.c</b>.</li>
</ul>
This approach allows variables to be shared across multiple files without duplication.


### volatile

The <code>volatile</code> keyword tells the compiler that a variable's value can change at any time, even outside the program's control (e.g., by hardware or another thread). Without volatile, the compiler might optimize code by assuming the variable doesn't change, leading to incorrect behavior.

When to Use volatile:
<ul>
  <li><b>Embedded Systems:</b> When a variable is updated by hardware (e.g., reading sensor data).</li>
  <li><b>Multi-threaded Programs:</b> When a variable is shared between threads.</li>
  <li><b>Interrupt Handlers:</b> When a variable is modified inside an interrupt routine.</li>
</ul>
    
 Example:<br>

 <code>#include <stdio.h>
#include <stdbool.h>
// Simulated hardware flag
volatile bool flag = false;
void hardwareInterrupt() {
    // Simulate hardware changing the flag
    flag = true;
}
int main() {
    printf("Waiting for flag...\n");
    // Simulate checking for a hardware flag
    while (!flag) {
        // Without volatile, this loop might be optimized into an infinite loop
    }
    printf("Flag is set! Exiting.\n");
    return 0;
}
</code>
    
### auto

The <code>auto</code> (redundant)keyword is used to declare automatic (local) variables. These variables are created when the program enters their scope and destroyed when it exits. However, since all variables declared inside a block are automatically treated as auto, the keyword is rarely used and is considered unnecessary.

Example:<br>

<code>#include <stdio.h>
int main() {
    auto int x = 10;  // Same as int x = 10;
    printf("Value of x: %d\n", x);
    return 0;
}
</code>

### register

The <code>register</code> (redundant)keyword suggests to the compiler that a variable should be stored in the CPU's register instead of RAM for faster access. However, modern compilers optimize this automatically, making the use of register unnecessary in most cases.

Example:<br>

<code>#include <stdio.h>
int main() {
    register int counter;  // Suggest storing in a CPU register
    for (counter = 0; counter < 5; counter++) {
        printf("Counter: %d\n", counter);
    }
    return 0;
}
</code>


### Modifiers summary

<table>

<th>
  <td><code>static</code></td>
  <td><code>extern</code></td>
  <td><code>auto</code></td>
  <td><code>register</code></td>
</th>
  
  <tr>
    <th>Storage</th>
    <td>Memory</td>
    <td>Memory</td>
    <td>Memory</td>
    <td>CPU registers</td>
  </tr>

  <tr>
    <th>Default value</th>
    <td>Zero</td>
     <td>Zero</td>
    <td>Garbage value (random value)</td>
     <td>Garbage value</td>
  </tr>

  <tr>
    <th>Scope</th>
    <td>Local to the block in which it is declared</td>
    <td>Global</td>
    <td>Local to the block in which it is declared</td>
    <td>Local to the block in which it is declared</td>
  </tr>

  <tr>
    <th>Lifetime</th>
    <td>Value persists between diﬀerent function calls</td>
    <td>Value persists between diﬀerent function calls</td>
    <td>Value persists between diﬀerent function calls</td>
    <td>Value persists between diﬀerent function calls</td>
  </tr>

  <tr>
    <th>Keyword optionality</th>
    <td>Mandatory</td>
    <td>Optional</td>
    <td>Optional</td>
    <td>Mandatory</td>
  </tr>
  
</table>

# Error handling

### Division by zero

### Signals

### setjmp


    








