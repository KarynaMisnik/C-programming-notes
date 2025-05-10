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
  - [errno, malloc, -Wall](#errno-malloc--wall)
  - [Division by zero](#division-by-zero)
  - [Signals](#signals)
  - [setjmp](#setjmp)
* [Input and Output](#input-and-output)
  - [Format specifiers](#format-specifiers)
  - [Escape characters](#escape-characters)
  - [puts function](#puts-function)
  - [scanf function](#scanf-function)
* [Math](#math)
  - [Arithmetic Operators](#arithmetic-operators)
  - [Assignment Operators](#assignment-operators)
  - [Logical Operators](#logical-operators)
  - [Relational and Equality Operators](#relational-and-equality-operators)
  - [Type Casting](#type-casting)
  - [Shift Operators](#shift-operators)
  - [Bitwise Operators](#bitwise-operators)
  - [Comma Operator](#comma-operator)
  - [Math libraries](#math-libraries)
  - [Trigonometric functions](#trigonometric-functions)
  - [Hyperbolic functions](#hyperbolic-functions)
  - [Exponential and logarithmic functions](#exponential-and-logarithmic-functions)
  - [Power functions](#power-functions)
  - [Nearest integer, absolute value, and remainder functions](#nearest-integer-absolute-value-and-remainder-functions)
  - [Error and gamma functions](#error-and-gamma-functions)
* [Control](#control)
  - [Conditionals](#conditionals)
  - [Logical Expressions](#logical-expressions)
  - [if else](#if-else)
  - [switch case](#switch-case)
  - [Loops](#loops)
  - [goto](#goto)
 * [My Examples](#my-examples)
   - [while-loop](#while-loop)
   - [for-loop](#for-loop)
   - [switch case](#switch-case)
   - [Pointers](#pointers)
   - [Pointers and Arrays](#pointers-and-arrays)
   - [Bad example of pointers use](#bad-example-of-pointers-use)
   - [Pointers and Functions](#Pointers-and-Functions)
   - [Signal generator](#signal-generator)
   
   
# Introduction

### Why C ⁉️

C is mostly used for writting OS. The first OS written in C was Unix(Linux is also written in C). Most high-level programming languages are written in C (PHP, Perl, Python, Ruby).

C language combines universality and portability across various computer architectures while retaining most of the control of the hardware provided by assembly language.

C is compiled language, it is small: a C statement usually translates to a few assembly instructions, while most additional functionality comes from library functions.

C is designed for portability, performance, and minimal resource usage, making it ideal for systems like operating systems and embedded systems. Its explicit coding style helps programmers understand what each line does. Known for its efficiency and low-level capabilities, C is the native language of UNIX, highly portable, stable, and widely used. It allows direct memory manipulation through constructs like pointers and arrays, giving programmers control over memory layout and dynamic allocation, though deallocation must be managed manually.

### History ⌛

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

# First Program 👾

### "Hello world!"

File extension for programs written in C: eg.: **hello.c**<br>
```C
#include <stdio.h>
int main(void)
{
printf("Hello, World!\n");
return 0;
}
```

What does each line mean?<br>
<code>#include <stdio.h></code>


This is a preprocessor directive. Preprocessor directives gives instructions to a part of the compiler to modify the code before it is compiled. 
**#include** directive retrieves C code from the standard **stdio.h** file(header files, which have **.h** extension). It works like library. From that library we need only function **printf**. <br>

<code>int main(void)</code>

It could be only one **main()** function because it acts as the starting point of all C programs.<br>

<code>printf("Hello World!\n");</code>

This line produces the actual output on the console(terminal in UNIX environment).<br>

<code>return 0;</code>

When ending a program, we use an exit status to inform the operating system whether the program ran successfully. An exit status of <code>0</code> signals success, while other integers can represent different types of errors. This practice of using exit codes is a long-standing convention.

### Compiling </> 

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

# Basic Program Structure 🏗️

### Block, Statement, Whitespace and Scope


C does not have complete block structure but it's still important to understand what block is. A **block** consists of executable statements. **Statements** are the pieces of text that the compiler translates into executable instructions, along with the surrounding **whitespace**:<br>

<code>int num = 5;</code>

This declares a variable of type *integer*, initializes it to the *value* 5, which can be later
accessed with the *identiﬁer* 'num'.

A block of code has opening brace <code>{</code> and closing <code>}</code> Blocks can contain other blocks and they can contain their blocks. Example:<br>

```C
int main(void)
{
/* this is a 'block' */
int num = 5;
{
/* this is also a 'block', nested inside the outer block */
int numTwo = 6;
}
return 0;
}
```

The compiler ignores whitespace (except when it separates e.g. return from <code>0</code>). To orginize code in more readable form it is common to use spaces (or tabs) to organize source code.

**Scopes** define the visibility of data or functions within a program. In C, there are two types of scopes: **local** and **global**. A global entity is accessible from anywhere in the program, while a local entity is limited to the block in which it is declared. Example: <br>

```C
int num = 5; /* 'global' variable,can be accessed from anywhere in the program */
/* function, all variables inside of it
are "local" to the function. */
int main(void)
{
int num = 6; /* 'num' now equals 6 */
printf("%d\n", num); /* prints a '6' instead of the global variable of 'num',5 */
return 0;
}
```

### Basic Functions 🌠

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

### Standard Library 📚

In **1983**, as C was being standardized, the **American National Standards Institute (ANSI)** created a committee to define a standard version of C, known as **ANSI C**. This standard included a basic set of common functions, called the **Standard Library**, which provides tools for tasks like input/output, string manipulation, math, file handling, and memory management. However, it excludes hardware- or OS-specific functions, such as those for graphics, sound, or networking. 

# C Compilation 🧙‍♂️

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


# Variables ⚡

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

```C
#include <stdio.h>
int main() {
    int number;       // Step 1: Declare
    number = 10;      // Step 2: Initialize
    number = 20;      // Step 3: Assign a new value
    printf("The value of number is: %d\n", number); // Output: 20
    return 0;}
```

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

```C
sizeof(type);
sizeof(variable);
```

Example:<br>

```C
int a = 10;
printf("%zu\n", sizeof(int));
// Size of int type
printf("%zu\n", sizeof(a));      
// Size of variable a
```

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
   
```C
#include <stdio.h>
int main() {
    const double pi = 3.14159;  // Declare and initialize a constant variable
    printf("The value of pi is: %f\n", pi);
    // Attempting to modify the value will cause a warning or error
    // pi = 3.14;  // Uncommenting this line will cause a compilation error or warning
    return 0;
}
``` 
    
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

```C
#include <stdio.h>
#define PI 3.14159
int main() {
    double area, radius = 5.0;
    area = PI * radius * radius;  // PI is replaced with 3.14159
    printf("Area of the circle: %.2f\n", area);
    return 0;
}
```

Creating Macros: Use **#define** to create macros, which are code snippets or expressions.

Example:<br>

```C
#include <stdio.h>
#define SQUARE(x) ((x) * (x))  // Macro to calculate the square
int main() {
    int num = 4;
    printf("Square of %d is %d\n", num, SQUARE(num));
    return 0;
}
```

Key Points:
<ul>
  <li>No memory usage: #define values are replaced at compile time, so they do not use memory.</li>
  <li>No type checking: Unlike const, #define does not have a data type, and it doesn't follow scope rules.</li>
  <li>Parentheses are important for macros: Always wrap macro parameters and expressions in parentheses to avoid precedence issues.</li>
</ul>
    
➕ **Pros:** 
<ul>
  <li>Makes the code more readable.</li>
  <li>Easy to change values in one place without searching throughout the code.</li>
</ul>

➖ **Cons:**
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

```C
#include <stdio.h>
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
```

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

 ```C
#include <stdio.h>
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
```
    
### auto

The <code>auto</code> (redundant)keyword is used to declare automatic (local) variables. These variables are created when the program enters their scope and destroyed when it exits. However, since all variables declared inside a block are automatically treated as auto, the keyword is rarely used and is considered unnecessary.

Example:<br>

```C
#include <stdio.h>
int main() {
    auto int x = 10;  // Same as int x = 10;
    printf("Value of x: %d\n", x);
    return 0;
}
```

### register

The <code>register</code> (redundant)keyword suggests to the compiler that a variable should be stored in the CPU's register instead of RAM for faster access. However, modern compilers optimize this automatically, making the use of register unnecessary in most cases.

Example:<br>

```C
#include <stdio.h>
int main() {
    register int counter;  // Suggest storing in a CPU register
    for (counter = 0; counter < 5; counter++) {
        printf("Counter: %d\n", counter);
    }
    return 0;
}
```


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

C does not have built-in support for error handling (like exceptions). Instead, programmers are responsible for preventing errors and checking function return values. For instance, <code>-1</code> or <code>NULL</code> are returned by functions like <code>socket()</code> or <code>malloc()</code> to indicate errors. If an error cannot be avoided or recovered, the programmer typically logs the error and terminates the program.

C provides an external variable, <code>errno</code>, which is available after including **<errno.h>**. This variable stores error codes defined by the operating system (e.g., Linux) when resources cannot be allocated. These error codes can be converted to readable messages using the strerror(errno) function.

### errno, malloc, -Wall

 <code>errno</code> Runtime Error Handling
<ul>
  <li><b>What it does:</b> Tracks errors from system calls or library functions during program execution.</li>
  <li><b>How it works:</b> Functions like malloc or socket set errno to an error code if they fail. You can use strerror(errno) to get a human-readable error message.</li>
  <li><b>Use case:</b> Diagnosing runtime errors (e.g., memory allocation failure, file not found).</li>
</ul>

<code>malloc</code> Dynamic Memory Allocation
<ul>
  <li><b>What it does:</b> Allocates memory dynamically from the heap during runtime. Returns a pointer to the allocated memory or NULL if it fails.</li>
  <li><b>How it interacts with errno:</b> If malloc fails, it sets errno to indicate the reason (e.g., ENOMEM for "out of memory").</li>
  <li><b>Use case:</b> Allocating memory when the size isn’t known at compile time or for large data structures.</li>
</ul>

<code>-Wall:</code> Compiler Warnings

<ul>
  <li><b>What it does:</b> A GCC compiler flag that enables warnings about potential issues in your code.</li>
  <li><b>Purpose:</b> Helps catch errors early (before runtime) by identifying problems like uninitialized variables, unused functions, or missing return statements.</li>
  <li><b>Use case:</b> Ensuring code quality and preventing bugs during the compilation stage.</li>
</ul>

Example:<br>

```C
#include <stdio.h>
#include <stdlib.h>
#include <errno.h>
#include <string.h>

int main() {
    // Request a huge amount of memory to simulate a failure

    size_t size = 1024L * 1024L * 1024L * 1024L; // 1 TB
    void *ptr = malloc(size);

    if (ptr == NULL) {
        // malloc failed, errno is set to ENOMEM (Out of memory)
        printf("Memory allocation failed: %s\n", strerror(errno));
        return 1; // Exit the program with an error code
    }

    printf("Memory allocation successful!\n");

    // Use the allocated memory...
    // Free the memory when done
    free(ptr);

    return 0;
}
```

>Note:
>Use <code>malloc</code> for dynamic memory allocation.
>Check <code>errno</code> if <code>malloc</code> (or other functions) fail to diagnose and handle runtime errors.
>Use <code>-Wall</code> to detect and fix issues during <ins>compilation</ins>, improving code quality and reducing runtime errors.  
    
### Division by zero

You must ensure that a divisor is never zero to avoid errors like division by zero, which can crash your program. Alternatively, in Unix-like systems, you can prevent the operating system from terminating your process by blocking the SIGFPE signal, which is triggered by floating-point exceptions like division by zero.

Instead of letting your program crash when dividing by zero, you can check the divisor before performing the operation:<br>

```C
  #include <stdio.h>
#include <signal.h>
#include <unistd.h>
void signal_handler(int signum) {
    printf("Caught SIGFPE: Division by zero!\n");
}
int main() {
    // Set up a signal handler for SIGFPE
    signal(SIGFPE, signal_handler);
    int numerator = 10;
    int divisor = 0;
    // This will trigger SIGFPE, but the handler will manage it
    int result = numerator / divisor;
    printf("Result: %d\n", result);
    return 0;
}
```

Check if a divisor is not zero using <code>if-statement</code>:<br>

```C
  #include <stdio.h>

int main() {
    int numerator = 10;
    int divisor = 0; // Example of a zero divisor

    if (divisor == 0) {
        printf("Error: Division by zero is not allowed.\n");
    } else {
        printf("Result: %d\n", numerator / divisor);
    }
    return 0;
}
```

### Signals

In C, when certain critical errors or events occur (like division by zero or an interrupt), the operating system can raise a signal to notify the program. Signals are system-level alerts that indicate something serious has happened and may disrupt normal program execution.

Signals are not meant to catch errors like exceptions in other languages. Instead, they’re used to handle critical events, such as cleaning up resources before a program exits.

To handle signals, include the **<signal.h>** header, define a signal handler function, and use the <code>signal()</code> function to specify how the program should respond to specific signals.

Example:<br>

```C
#include <stdio.h>
#include <signal.h>
#include <stdlib.h>

// Signal handler function
void handle_signal(int signal) {

    if (signal == SIGFPE) {
        printf("Caught signal: Division by zero occurred!\n");
        exit(EXIT_FAILURE); // Cleanly terminate the program
    }
}

int main() {
    // Set up the signal handler for SIGFPE (Floating Point Exception)
    signal(SIGFPE, handle_signal);

    int numerator = 10;
    int divisor = 0;

    // This will trigger the SIGFPE signal
    int result = numerator / divisor;
    printf("Result: %d\n", result); // This line will not be reached

    return 0;
}
```

### setjmp

The <code>setjmp</code> and <code>longjmp</code> functions in C are used to perform <ins>non-local</ins> jumps—jumping from one part of a program to another, bypassing the normal function call and return mechanism. These functions are typically used for implementing custom error handling mechanisms.

**setjmp:** Saves the current environment (program state) in a jmp_buf structure for later use by longjmp.

**longjmp:** Restores the saved environment, effectively jumping back to the point where setjmp was called.


They are commonly used for:

1. **Error recovery:** Jumping out of deeply nested function calls when an error occurs.

2.Implementing exception-like mechanisms in C.

⚠️ Caution: These functions can make code harder to read and debug. Use them sparingly and only when necessary.

Example:<br>

```C
#include <stdio.h>
#include <setjmp.h>

jmp_buf env; // Declare a buffer to hold the environment

void risky_function(int value) {
    if (value == 0) {
        printf("Error: Division by zero detected!\n");
        longjmp(env, 1); // Jump back to the point where setjmp was called
    }
    printf("Result: %d\n", 10 / value);
}
int main() {
    int val = 0;
    if (setjmp(env) == 0) {
        // First time setjmp is called, it returns 0
        printf("Enter a non-zero value: ");
        scanf("%d", &val);
        // Call a function that might fail
        risky_function(val);
    } else {
        // After longjmp, setjmp returns the second argument of longjmp
        printf("Recovered from an error. Please fix your input.\n");
    }
    printf("Program continues...\n");
    return 0;
}
```

**How It Works**

1. setjmp(env) saves the current program state (like a checkpoint).

2. If no error occurs, the program runs normally.

3. If an error is detected, longjmp(env, 1) jumps back to the setjmp call, skipping the rest of the execution in the risky function.

4. The second call to setjmp returns 1, allowing the program to handle the error and continue.

Output Example: 

Input <code>0</code><br>

```C
Enter a non-zero value: 0
Error: Division by zero detected!
Recovered from an error. Please fix your input.
Program continues...
```


Input <code>2</code><br>

<code>Enter a non-zero value: 2
Result: 5
Program continues...
</code>

# Input and Output

### Format specifiers

<ins>Format specifiers</ins> in C are used to define the type of data being input or output when working with formatted input/output functions like <code>printf()</code> and <code>scanf()</code>. They act as **placeholders** within strings and indicate the type of variable that should be inserted or interpreted at that point.
Commonly Used Format Specifiers

Here are the most commonly used format specifiers in C:
<ins>Integer Types</ins>

| Modifier          | Description                                   |                       
|-------------------|-----------------------------------------------|
|%d or %i           |Signed decimal integer                         |                              
|%u                 |Unsigned decimal integer                       |                              
|%o                 |Unsigned octal integer                         |                             
|%x or %X           |Unsigned hexadecimal integer                   |                            


<ins>Floating-point Types</ins>


| Modifier          | Description                                   | Example                      |
|-------------------|-----------------------------------------------|------------------------------|
| %f                |Floating-point number                          | 3.14159                      |
| %e or %E          |Scientific notation                            |3.14e+00 or 3.14E+00          |
| %g or %G          |Uses %f or %e/%E based on precision            |                              |
|%a or %A           |Hexadecimal floating-point number              |                              |


<ins>Character and String Types</ins>

| Modifier          | Description                                   | 
|-------------------|-----------------------------------------------|
| %c                |Single character                               |                             
| %s                |String of characters                                               


<ins>Pointer</ins>

| Modifier          | Description                                   | 
|-------------------|-----------------------------------------------|
| %p                | Memory address (pointer)                      |                              


<ins>Modifiers for Size</ins>

To handle specific sizes, you can use modifiers before the format specifier:

| Modifier          | Description                                   | Example                      |
|-------------------|-----------------------------------------------|------------------------------|
|%h                 |Short                                          |%hd for short integers        |
|%l                 |Long                                           |%ld for long integers, %lf for double|
|%ll                |Long long                                      |%lld for long long integers   |
|%z                 |Size type (used for size_t)                    |                              |

 
<ins>Special Formats</ins>

| Modifier          | Description                                   | 
|-------------------|-----------------------------------------------|
|%%                 |Prints a literal % character                   |                                             
  
### Escape characters

<ins>Escape characters</ins> in C are special sequences of characters used within strings or character literals to represent characters that cannot be typed directly or have special meaning in a program. They start with a backslash (\) followed by a specific character.

| Escape Character | Description                                   | Example                      |
|-------------------|-----------------------------------------------|------------------------------|
| `\n`             | Newline (line break)                         | `printf("Hello\nWorld");`   |
| `\t`             | Horizontal tab                               | `printf("Hello\tWorld");`   |
| `\\`             | Backslash                                    | `printf("C:\\Path\\File");` |
| `\'`             | Single quote                                 | `printf("It\'s fine.");`    |
| `\"`             | Double quote                                 | `printf("He said, \"Hi!\"");` |
| `\?`             | Question mark                                | `printf("What\?");`         |
| `\a`             | Alert (produces a beep sound)                | `printf("\a");`             |
| `\b`             | Backspace                                    | `printf("ABC\b");`          |
| `\r`             | Carriage return (moves to the beginning of the current line) | `printf("Hello\rWorld");`   |
| `\f`             | Form feed                                    | Rarely used in modern code. |
| `\v`             | Vertical tab                                 | Rarely used in modern code. |
| `\0`             | Null character (indicates end of a string)   | Used in C strings.          |

### puts function

The <code>uts()</code> function in C is used to output a string to the standard output (usually the console) followed by a newline character <code>(\n)</code>.

1. **Input:** Takes a <ins>single</ins> argument, a pointer to a null-terminated string (char *str).
2. **Output:** Prints the string followed by a newline.
3. **Return Value:** Returns a <ins>non-negative</ins> value on success or **EOF** on <ins>failure.</ins>

Example: <br>

```C
#include <stdio.h>
int main() {
    puts("Hello, World!");  // Outputs: Hello, World!
    return 0;
}
```

### scanf function

The <code>scanf()</code> function in C is used for formatted input. It reads data from the standard input (usually the keyboard) and stores it in the variables specified by the arguments.

Example:<br>

<code>int scanf(const char *format, ...);</code>

<ins>Key Limitations</ins>

**Input Validation:**
Does not handle invalid input well (e.g., entering letters instead of numbers).
    
**Whitespace Sensitivity:**
<code>%s</code> stops reading at whitespace. Use <code>gets()</code> or <code>fgets()</code> for multi-word strings.
    
**Buffer Overflow:**
Can lead to undefined behavior if the input exceeds the buffer size.

>Notes: Use **fgets()** for strings to handle spaces and prevent overflow.
>Always validate the return value of **scanf()** to ensure input was correctly read.

# Math 👨‍🏫

### Arithmetic Operators

Arithmetic operators perform basic mathematical operations. Here are the key operators:

| Operator | Description               | Example (`a = 10, b = 3`) |
|----------|---------------------------|---------------------------|
| `+`      | Addition                  | `a + b = 13`              |
| `-`      | Subtraction               | `a - b = 7`               |
| `*`      | Multiplication            | `a * b = 30`              |
| `/`      | Division                  | `a / b = 3` (integer division) |
| `%`      | Modulus (remainder)       | `a % b = 1`               |


<ins>Modulus Operator (%)</ins>

The modulus operator returns the remainder of a division. It's not the equivalent of the ~~mathematical
modulus~~ and works only with integer operands. Division of integers will return an integer, and the division
of a negative integer by a positive integer((-5) / 3 = -1 [not -2]) will round towards zero instead of rounding down

>Note: Modulus is not deﬁned for ﬂoating-point numbers, but the **math.h** library has an **fmod** function.

 Example:<br>

```C
int a = 10, b = 3;
printf("%d", a % b); // Output: 1 (10 divided by 3 leaves a remainder of 1)
```

>Note: For negative numbers, the sign of the result depends on the implementation (often follows the dividend).

### Assignment Operators

Assignment operators in C are used to assign values to variables. They can also combine assignment with other operations.

| Operator | Description                        | Example         | Equivalent To   |
|----------|------------------------------------|-----------------|-----------------|
| `=`      | Assigns a value to a variable      | `a = 10`        | N/A             |
| `+=`     | Adds and assigns                   | `a += 5`        | `a = a + 5`     |
| `-=`     | Subtracts and assigns              | `a -= 3`        | `a = a - 3`     |
| `*=`     | Multiplies and assigns             | `a *= 2`        | `a = a * 2`     |
| `/=`     | Divides and assigns                | `a /= 4`        | `a = a / 4`     |
| `%=`     | Calculates modulus and assigns     | `a %= 3`        | `a = a % 3`     |

### Logical Operators

Logical operators are used to perform logical operations, often in decision-making and conditional expressions.

| Operator | Description                       | Example (`a = 1, b = 0`) | Result  |
|----------|-----------------------------------|--------------------------|---------|
| `&&`   | Logical AND (true if both are true) | `a && b`                 | `0` (false) |
| `ll`    | Logical OR (true if at least one is true) | `a ll b`          | `1` (true)  |
| `!`      | Logical NOT (negates a condition)  | `!a`                     | `0` (false) |


Example:<br>

```C
int a = 1, b = 0;
if (a && b) printf("Both true\n");  // Doesn't print
if (a || b) printf("At least one true\n");  // Prints
if (!a) printf("Not true\n");  // Doesn't print
```

>Logical operators return 1 (true) or 0 (false) based on the evaluation of conditions.

The **conditional operator**, also known as the **ternary operator**, is a shorthand for an **if-else** statement in C. It evaluates a condition and returns one of two values based on the result.

<code>condition ? value_if_true : value_if_false;</code>

condition: An expression that evaluates to <code>true</code> (non-zero) or <code>false</code> (zero).
<code>value_if_true</code>: The value returned if the condition is <ins>true</ins>.
<code>value_if_false</code>: The value returned if the condition is <ins>false</ins>.

Example:<br>

```C
#include <stdio.h>
int main() {
    int a = 10, b = 20;
    int max = (a > b) ? a : b; // Checks which value is greater
    printf("The maximum is: %d\n", max); // Outputs: The maximum is: 20
    return 0;
}
```

>Note: It's called "ternary" because it involves three operands: condition, true value, false value.

It is shorter way to write <code>if-statement</code>. Compare:

|if-statement|ternary|
|------------|-------|
|if (a > b)<br> max = a;<br> else<br>max = b; |max = (a > b) ? a : b;|
  
### Relational and Equality Operators

Relational operators in C are used to compare two values. They return a boolean result: <code>1 (true)</code> if the condition is <ins>satisfied</ins>, and <code>0 (false)</code> otherwise.

| Operator | Description                  | Example (`a = 10, b = 20`) | Result     |
|----------|------------------------------|---------------------------|-------------|
| `==`     | Equal to                     | `a == b`                  | `0` (false) |
| `!=`     | Not equal to                 | `a != b`                  | `1` (true)  |
| `>`      | Greater than                 | `a > b`                   | `0` (false) |
| `<`      | Less than                    | `a < b`                   | `1` (true)  |
| `>=`     | Greater than or equal to     | `a >= b`                  | `0` (false) |
| `<=`     | Less than or equal to        | `a <= b`                  | `1` (true)  |

>Note: **==** checks for equality, while **=** is used for assignment.
>Avoid using **==** for floating-point values due to precision issues.

Example:<br>

```C
#include <stdio.h>
int main() {
    int a = 10, b = 20;
    if (a == b) 
        printf("a is equal to b\n");
    else 
        printf("a is not equal to b\n");
    return 0;
}
```

>a is not equal to b

### Type Casting

Type casting in C is the process of converting a variable from one data type to another. It can be done explicitly by the programmer or implicitly by the compiler.

**Types of Type Casting**

**1.** Implicit Type Casting (Type Promotion)

Automatically performed by the compiler when assigning values of smaller data types to larger ones:

<code>int</code> → <code>float</code><br>
<code>char</code> → <code>t</code><br>

Example:<br>

<code>int num = 10;
float fnum = num;  // Implicit conversion from int to float
printf("%f", fnum);  // Output: 10.000000
</code>

**2.** Explicit Type Casting (Manual Conversion)

Done manually using the cast operator (type).

Useful when precise control over data conversion is needed.

Example:<br>

<code>float num = 5.7;
int intNum = (int) num;  // Explicit conversion from float to int
printf("%d", intNum);  // Output: 5 (decimal part is truncated)
</code>

Example of Type Casting:<br>

```C
#include <stdio.h>
  
int main() {
    int a = 5, b = 2;
    float result;
    result = (float)a / b;  // Explicit casting to float
    printf("Result: %.2f\n", result);  // Output: 2.50
    return 0;
}
```

>Implicit Casting is automatic and safe, but may lead to unintended results if not careful.
>Explicit Casting allows precision but may result in loss of data (e.g., truncating decimal points).
>Type Promotion happens <ins>automatically</ins> in expressions (e.g., integer division converts to float if one >operand is float).
>Casting <ins>does not change</ins> the original data type, only how the value is interpreted in the expression.

### Shift Operators

<ins>Shift operators</ins> in C are used to shift the bits of a variable to the left or right. They are primarily used for efficient mathematical operations, bit manipulation, and low-level programming.

Types of Shift Operators:

| Operator  | Description                 | Example (if `a = 8`) | Result in Binary | Decimal Result |
|-----------|-----------------------------|----------------------|-----------------|----------------|
| `<<`      | Left shift                    | `a << 2`              | `00100000`       | `32`            |
| `>>`      | Right shift                    | `a >> 2`              | `00000010`       | `2`             |


**Left Shift Operator (<<)**

Shifts bits to the **left**, filling with **zeros** on the **right**.
Each shift left **multiplies** the number by 2^n (where n is the shift count).
    
Example:<br>

<code>int a = 8;       // Binary: 00001000
int result = a << 2;  // Shift left by 2 (00001000 -> 00100000)
printf("%d", result); // Output: 32
</code>


**Right Shift Operator (>>)**

Shifts bits to the right, discarding bits on the right.
The behavior depends on the <ins>type of the number:</ins>
For <ins>unsigned</ins> numbers, zeroes are shifted in.
For <ins>signed numbers</ins>, it depends on the compiler (could fill with zeros or sign bits).
Each shift right divides the number by **2^n**.

Example:<br>

<code>int a = 8;       // Binary: 00001000
int result = a >> 2;  // Shift right by 2 (00001000 -> 00000010)
printf("%d", result); // Output: 2
</code>

Example Program:<br>

<code>#include <stdio.h>
int main() {
    int num = 16; // Binary: 00010000
    printf("Left Shift by 1: %d\n", num << 1);  // Output: 32
    printf("Right Shift by 1: %d\n", num >> 1); // Output: 8
    return 0;
}</code>

‼️Important Notes:

1. Shifting Beyond Limits:

Shifting by more than the number of bits in the type (e.g., int has 32 bits) leads to undefined behavior.

2. Arithmetic vs Logical Right Shift:

Arithmetic shift (signed int): Preserves sign bit in **negative** numbers.
Logical shift (unsigned int): Fills with **zeros**.

3. Efficiency:

Bitwise shifts are faster than multiplication and division by powers of 2.

### Bitwise Operators

Bitwise operators in C are used to manipulate individual bits of data at the binary level. These operators are useful in low-level programming, such as working with hardware, encryption, and optimization.

Types of Bitwise Operators:

| Operator | Name         | Description                                      | Example (`a = 5`, `b = 3`) |
|----------|--------------|--------------------------------------------------|---------------------------|
| `&`      | Bitwise AND  | Sets bits to 1 if both bits are 1                | `a & b` (0101 & 0011 = 0001) → `1` |
| `l`      | Bitwise OR   | Sets bits to 1 if either bit is 1                | `a l b` (0101 | 0011 = 0111) → `7` |
| `^`      | Bitwise XOR  | Sets bits to 1 if bits are different             | `a ^ b` (0101 ^ 0011 = 0110) → `6` |
| `~`      | Bitwise NOT  | Inverts all bits (1 to 0, 0 to 1)        | `~a` (~0101 = 1010) → `-6` (2's complement)|
| `<<`     | Left Shift   | Shifts bits to the left, filling with zeros       | `a << 1` (0101 → 1010) → `10` |
| `>>`     | Right Shift  | Shifts bits to the right, discarding right bits   | `a >> 1` (0101 → 0010) → `2` |


1. Bitwise **AND (&)**

Compares each bit of two numbers; result is 1 if both bits are 1.

Example:<br>

<code>int a = 5, b = 3;  // 5 = 0101, 3 = 0011
int result = a & b; // 0001 (decimal 1)
printf("%d", result);  // Output: 1
</code>

2. Bitwise **OR (|)**

Compares each bit; result is 1 if either bit is 1.

Example:<br>

<code>int a = 5, b = 3;
int result = a | b; // 0111 (decimal 7)
printf("%d", result);  // Output: 7
</code>

3. Bitwise **XOR (^)**

Compares each bit; result is 1 if the bits are different.

Example:<br>

<code>int a = 5, b = 3;
int result = a ^ b; // 0110 (decimal 6)
printf("%d", result);  // Output: 6
</code>

4. Bitwise **NOT (~)**

Inverts all bits (1 → 0, 0 → 1). Uses two's complement, meaning the value becomes negative.

Example:<br>

<code>int a = 5;
int result = ~a; // 1010 (decimal -6)
printf("%d", result);  // Output: -6
</code>

5. Left Shift **(<<)**

Moves bits to the left, filling right positions with zeros. Equivalent to multiplying by 2^n.

Example:<br>

<code>int a = 5;
int result = a << 1; // 1010 (decimal 10)
printf("%d", result);  // Output: 10
</code>

6. Right Shift **(>>)**

Moves bits to the right, discarding the rightmost bits. Equivalent to dividing by 2^n.

Example:<br>

<code>int a = 5;
int result = a >> 1; // 0010 (decimal 2)
printf("%d", result);  // Output: 2
</code>

**Example Program Using Bitwise Operators**

```C
#include <stdio.h>
  
int main() {
    int a = 5, b = 3;
    printf("a & b = %d\n", a & b);  // Output: 1
    printf("a | b = %d\n", a | b);  // Output: 7
    printf("a ^ b = %d\n", a ^ b);  // Output: 6
    printf("~a = %d\n", ~a);        // Output: -6
    printf("a << 1 = %d\n", a << 1); // Output: 10
    printf("a >> 1 = %d\n", a >> 1); // Output: 2
    return 0;
}
```

🗝️ **Key Points**

**Efficiency:**

Bitwise operations are **faster** than arithmetic operations for multiplication/division by powers of 2.

**Use Cases:**

Bit masking, setting/clearing specific bits, <ins>optimizing</ins> performance.

⚠️ Caution:

When working with signed numbers, right shifts may behave differently depending on the compiler (logical vs arithmetic shift).

### Comma Operator

The comma operator in C is used to separate multiple expressions where only the rightmost expression's value is returned. It is often used to write concise code, especially in loop constructs and complex expressions.

1. Multiple Expressions in a Single Statement:<br>

<code>#include <stdio.h>
int main() {
    int a, b;
    a = (b = 10, b + 5);  // Assign b = 10, then a = b + 5
    printf("a = %d, b = %d\n", a, b);  // Output: a = 15, b = 10
    return 0;
}
</code>

2. For loop:<br>

<code>#include <stdio.h>
int main() {
    int i, j;
    for (i = 0, j = 10; i < 5; i++, j--) {
        printf("i = %d, j = %d\n", i, j);
    }
    return 0;
}
</code>

3. Function Arguments

The comma operator should not be confused with the comma used to separate function arguments, which serves a different purpose:<br>

<code>void func(int x, int y);  // Comma here separates arguments, not the operator</code>

Example of Misuse:<br>

<code>int x = (5, 10, 15);  // Only 15 is assigned to x
printf("%d", x);  // Output: 15</code>


### Math libraries

The **math.h** header file in C contains declarations for various mathematical functions (like **sqrt**, **sin**, **cos**, **pow**, etc.).

<ins>Historical Evolution:</ins>

**1990 ISO Standard:** Only supported <code>double</code> precision for these functions.
**1999 ISO Standard:** Added support for <code>float</float> and <code>long double</code> precision.

<ins>Linking:</ins> To use these functions in your program, you must link it with the math library (usually by including a flag like 
**-lm** during compilation).

<ins>Error Handling:</ins>

**Domain Errors:** Occur when the input values to a function are invalid (e.g., negative argument for <code>sqrt</code>).
**Range Errors:** Occur when the result of the function cannot be accurately represented within the given floating-point type (e.g., <code>pow(1000.0, 1000.0)</code> might exceed the maximum representable value for a double).


### Trigonometric functions

#### The acos and asin functions

The **acos** functions return the <ins>arccosine</ins> of their arguments in radians, and the **asin** functions return the <ins>arcsine</ins> of their arguments in radians. All functions expect the argument in the range <code>[-1,+1]</code>. The arccosine returns a value in the range <code>[0,π]</code> the arcsine returns a value in the range <code>[-π/2,+π/2]</code>.

|#include <math.h>|
|-----------------|
|float asinf(float x); /* C99 */|
|float acosf(float x); /* C99 */|
|double asin(double x);|
|double acos(double x);|
|long double asinl(long double x); /* C99 */|
|long double acosl(long double x); /* C99 */|

#### The atan and atan2 functions

The **atan** functions return the <ins>arctangent</ins> of their arguments in radians, and the **atan2** function return the <ins>arctangent</ins> of y/x in radians. The **atan** functions return a value in the range <code>[-π/2,+π/2]</code> (the reason why ±π/2 are included in the range is because the ﬂoating-point value may represent inﬁnity, and atan(±∞) = ±π/2); the **atan2** functions
return a value in the range <code>[-π,+π]</code>. For **atan2**, a domain error may occur if both arguments
are zero.

|#include <math.h>|
|-----------------|
|float atanf(float x); /* C99 */|
|float atan2f(float y, float x); /* C99 */|
|double atan(double x);|
|double atan2(double y, double x);|
|long double atanl(long double x); /* C99 */|
|long double atan2l(long double y, long double x); /* C99 */|

#### The cos, sin, and tan functions

The **cos**, **sin**, and **tan** functions return the <ins>cosine</ins>, <ins>sine</ins>, and <ins>tangent</ins> of the argument, expressed in *radians*.

|#include <math.h>|
|-----------------|
|float cosf(float x); /* C99 */|
|float sinf(float x); /* C99 */|
|float tanf(float x); /* C99 */|
|double cos(double x);|
|double sin(double x);|
|double tan(double x);|
|long double cosl(long double x); /* C99 */|
|long double sinl(long double x); /* C99 */|
|long double tanl(long double x); /* C99 */|

### Hyperbolic functions

The **cosh**, **sinh** and **tanh** functions compute the hyperbolic cosine, the hyperbolic sine, and the hyperbolic tangent of the argument respectively. For the hyperbolic sine and cosine functions, a range error occurs if the magnitude of the argument is too large.
The acosh functions compute the inverse hyperbolic cosine of the argument. A domain
error occurs for arguments less than 1.

The asinh functions compute the inverse hyperbolic sine of the argument.
The atanh functions compute the inverse hyperbolic tangent of the argument. 

A domain error occurs if the argument is not in the interval <code>[-1, +1]</code>. A range error may occur if the argument equals <code>-1</code> or <code>+1</code>.

|#include <math.h>|
|-----------------|
|float coshf(float x); /* C99 */|
|float sinhf(float x); /* C99 */|
|float tanhf(float x); /* C99 */|
|double cosh(double x);|
|double sinh(double x);|
|double tanh(double x);|
|long double coshl(long double x); /* C99 */|
|long double sinhl(long double x); /* C99 */|
|long double tanhl(long double x); /* C99 */|
|float acoshf(float x); /* C99 */|
|float asinhf(float x); /* C99 */|
|float atanhf(float x); /* C99 */|
|double acosh(double x); /* C99 */|


### Exponential and logarithmic functions

An exponential function is a mathematical function of the form <code>f(x) = a * e^(bx)</code>, where e is Euler's number (approximately 2.71828), and a and b are constants. In C, you can use the **exp()** function to compute e raised to the power of a number.

```C
#include <stdio.h>
#include <math.h>  // Include math.h for exp() function
int main() {
    double x = 2.0;
    double result = exp(x);  // exp(x) returns e raised to the power of x
    printf("e^%.2f = %.5f\n", x, result);
    return 0;
}
``

>Note: Here, exp(x) returns e raised to the power of x, which is e^2 in this example.

Logarithmic functions are the inverse of exponential functions. In C, you can use **log()** and **log10()** to compute natural and base-10 logarithms, respectively.


<code>
#include <stdio.h>
#include <math.h>  // Include math.h for log() function
int main() {
    double x = 20.0;
    double result = log(x);  // log(x) returns the natural log (base e) of x
    printf("ln(%.2f) = %.5f\n", x, result);
    return 0;
}
</code>

**Exponential Growth (Population Growth)**

In real-life applications, exponential growth can model things like population growth or compound interest. This example shows how you might calculate population growth over time.

<code>
#include <stdio.h>
#include <math.h>
int main() {
    double initial_population = 1000.0;  // Initial population
    double growth_rate = 0.05;           // Growth rate (5%)
    double time = 10.0;                  // Time in years
    double population = initial_population * exp(growth_rate * time);  // e^(growth_rate * time)
    printf("Population after %.2f years: %.2f\n", time, population);
    return 0;
}
</code>


### Power functions

The **pow** functions compute x raised to the power y and return the result. A domain <ins>error</ins> occurs if <code>x</code> is negative and <code>y</code> is not an integral value. A domain error occurs if the result cannot be represented when **x** is zero and y is less than or equal to zero. A range error may
occur.

<code>
#include <stdio.h>
#include <math.h>
int main() {
    double base = 3.0;
    double exponent = 4.0;
    double result = pow(base, exponent);  // base^exponent
    printf("%.2f^%.2f = %.2f\n", base, exponent, result);
    return 0;
}
</code>

>Note: Here, pow(base, exponent) computes the value of base raised to the power of exponent.


The **sqrt** functions compute the positive square root of <code>x</code> and return the result. A domain error occurs if the argument is <ins>negative</ins>.


```C
#include <stdio.h>
#include <math.h>  // For sqrt() function

int main() {
    double number, result;
    // Ask the user for input
    printf("Enter a number: ");
    scanf("%lf", &number);
    // Check if the number is non-negative, as sqrt() only works with non-negative values
    if (number < 0) {
        printf("Error! Square root of a negative number is not defined.\n");
    } else {
        // Calculate the square root
        result = sqrt(number);
        // Output the result
        printf("The square root of %.2lf is %.2lf\n", number, result);
    }
    return 0;
}
```

The **cbrt** functions compute the <ins>cube</ins> root of <code>x</code> and return the result.

<code>
#include <stdio.h>
#include <math.h>  // For cbrt() function
int main() {
    double number, result;
    // Ask the user for input
    printf("Enter a number: ");
    scanf("%lf", &number);
    // Calculate the cube root
    result = cbrt(number);
    // Output the result
    printf("The cube root of %.2lf is %.2lf\n", number, result);
    return 0;
}
</code>


The **hypot** functions compute the <ins>square</ins> root of the sums of the squares of <code>x</code> and <code>y</code>, without
overﬂow or underﬂow, and return the result.

<code>
#include <stdio.h>
#include <math.h>  // For hypot() function
int main() {
    double side1, side2, result;
    // Ask the user for the lengths of the two sides
    printf("Enter the length of the first side: ");
    scanf("%lf", &side1);
    printf("Enter the length of the second side: ");
    scanf("%lf", &side2);
    // Calculate the hypotenuse using the hypot() function
    result = hypot(side1, side2);
    // Output the result
    printf("The length of the hypotenuse is %.2lf\n", result);
    return 0;
}
</code>


### Nearest integer, absolute value, and remainder functions

The **ceil** functions compute the smallest integral value not less than <code>x</code> and return the result; the floor functions compute the largest integral value not greater than <code>x</code> and return the result.

<code>
#include <stdio.h>
#include <math.h>  // For ceil() function
int main() {
    double number, result;
    // Ask the user for input
    printf("Enter a number: ");
    scanf("%lf", &number);
    // Calculate the ceiling value
    result = ceil(number);
    // Output the result
    printf("The ceiling of %.2lf is %.0lf\n", number, result);
    return 0;
}
</code>

>Note: Enter a number: 3.14
>The ceiling of 3.14 is 4


The **fabs** functions compute the absolute value of a ﬂoating-point number x and return the result.

#include <stdio.h>
#include <math.h>  // For fabs() function
int main() {
    double number, result;
    // Ask the user for input
    printf("Enter a number: ");
    scanf("%lf", &number);
    // Calculate the absolute value
    result = fabs(number);
    // Output the result
    printf("The absolute value of %.2lf is %.2lf\n", number, result);
    return 0;
}

>Note: Enter a number: -7.25
>The absolute value of -7.25 is 7.25



### Error and gamma functions

The **erf** functions compute the <ins>error function</ins>, while **erfc** computes its complement <code>(1 - erf(x))</code>, with possible range errors for large arguments. The **lgamma** functions return the natural logarithm of the absolute gamma function value, with range errors for negative integers or zero. The tgamma functions compute the gamma function, with domain errors for negative integers and potential range errors.

# Control

Programs rarely follow a single control path; they use conditionals and loops to respond to input, repeat steps efficiently, and simulate logic. In C, a block is a grouped set of statements enclosed in **{}** and executed as a unit. Blocks can be empty, nested, and do not require a semicolon after the closing brace.

### Conditionals

Decision-making is fundamental to both human activities and programming. In C, conditionals allow programs to make decisions based on specific conditions. The **If-Else** statement is the most common conditional, with **Switch-Case** providing a shorthand alternative. In C, logic is treated as arithmetic: <code>0</code> represents <ins>false</ins>, and any <code>nonzero</code> value represents <ins>true</ins>. Using predefined values for "TRUE" can lead to errors. Logical and arithmetic operations are closely related, with specific operators commonly used for logic.

| Expression | Result |
|------------|--------|
| a < b      | 1 if a is less than b, 0 otherwise. |
| a > b      | 1 if a is greater than b, 0 otherwise. |
| a <= b     | 1 if a is less than or equal to b, 0 otherwise. |
| a >= b     | 1 if a is greater than or equal to b, 0 otherwise. |
| a == b     | 1 if a is equal to b, 0 otherwise. |
| a != b     | 1 if a is not equal to b, 0 otherwise. |

>Note: remember that the equality operator is <code>==</code>, not <code>=</code>. Mistaking <code>=</code> for <code>==</code> can >lead to hard-to-find bugs since <code>=</code> <ins>assigns</ins> a value instead of checking equality. The compiler may not catch >this mistake, as expressions like
><code>if (c = 20) {
>} </code>
>are valid but always evaluate as **true**.
>A helpful trick to avoid this error is to place the constant first (e.g., <code>if (20 == c))</code> so that a mistaken **=** >would cause a compilation error.

>Note: C does not have a dedicated boolean type as many other languages do. <code>0</code> means **false** and anything else
>**true**.

### Logical Expressions

| Operator | Description |
|----------|------------|
| `a || b` | When EITHER `a` or `b` is true (or both), the result is `1`, otherwise the result is `0`. |
| `a && b` | When BOTH `a` and `b` are true, the result is `1`, otherwise the result is `0`. |
| `!a` | When `a` is true, the result is `0`. When `a` is `0`, the result is `1`. |


<code>e = ((a && b) || (c > d));</code>

>e is set equal to 1 if a and b are non-zero, or if c is greater than d. In all other cases, e is set to 0.

Bitwise operators operate on operands at the bit level and require integral types. The six operators are **& (AND)**, **| (OR)**, **^ (XOR)**, **~ (NOT)**, **<< (left shift)**, and **>> (right shift)**. The **NOT** operator is unary, while the others are binary. These operators have lower precedence than relational and equivalence operators, often requiring parentheses.

Numbers starting with **0x** are hexadecimal (base 16), using digits 0-9 and a-f. Hex is commonly used in C because it easily converts to binary, which C does not natively support.

| Operator  | Description | Example |
|-----------|------------|---------|
| `a & b`  | Bitwise AND of `a` and `b` | `0xc & 0xa` → `0x8` (Binary: `1100 & 1010` → `1000`) |
| `a | b`  | Bitwise OR of `a` and `b`  | `0xc | 0xa` → `0xe` (Binary: `1100 | 1010` → `1110`) |
| `a ^ b`  | Bitwise XOR of `a` and `b` | `0xc ^ 0xa` → `0x6` (Binary: `1100 ^ 1010` → `0110`) |
| `~a`     | Bitwise complement of `a` | `~0xc` → `-1 - 0xc` (Binary: `~1100` → `...11110011`, where `...` are additional `1` bits) |
| `a << b` | Shift `a` left by `b` (Multiply `a` by `2^b`) | `0xc << 1` → `0x18` (Binary: `1100 << 1` → `11000`) |
| `a >> b` | Shift `a` right by `b` (Divide `a` by `2^b`) | `0xc >> 1` → `0x6` (Binary: `1100 >> 1` → `110`) |


### if else

The if-else statement in C is used for decision-making, allowing a program to execute different blocks of code based on conditions.<br>

<code>
if (condition) {
    // Code executes if condition is true
} else {
    // Code executes if condition is false
}</code>

Example:<br>

```C
  #include <stdio.h>
int main() {
    int num = 10;
    if (num > 0) {
        printf("Number is positive.\n");
    } else {
        printf("Number is non-positive.\n");
    }
    return 0;
}
```

>Number is positive.

**if-else if-else Ladder**
Used when there are multiple conditions to check.<br>

<code>
  if (condition1) {
    // Executes if condition1 is true
} else if (condition2) {
    // Executes if condition2 is true
} else {
    // Executes if none of the conditions are true
}</code>

Example:<br>

<code>
  int score = 85;
if (score >= 90) {
    printf("Grade: A\n");
} else if (score >= 80) {
    printf("Grade: B\n");
} else if (score >= 70) {
    printf("Grade: C\n");
} else {
    printf("Grade: F\n");
}</code>

**Nested if-else**
An if-else statement inside another if-else.

Example:<br>

<code>
  int num = 5;
if (num > 0) {
    if (num % 2 == 0)
        printf("Positive even number\n");
    else
        printf("Positive odd number\n");
} else {
    printf("Non-positive number\n");
}</code>

**Ternary Operator (?:) - Shorter Alternative**

<code>(condition) ? expression1 : expression2;</code>

Example:<br>

<code>int num = -5;
printf("%s", (num > 0) ? "Positive" : "Non-positive");
</code>

>**if** evaluates a condition; if true, it executes the corresponding block.
>**else** runs when the if condition is <ins>false</ins>.
>**else if** allows checking multiple conditions.
>Always use braces **{}** for multiple statements in if blocks to avoid logic errors.
>The <ins>ternary operator</ins> **(?:)** is a shorthand for simple if-else statements.
 
### switch case

The **switch-case** statement in C is a multi-way branching control structure used when a variable is compared against multiple possible values. It is often used as an alternative to long if-else if chains for better readability and efficiency.

Syntax:<br>

```C
switch (expression) {
    case value1:
        // Code to execute if expression == value1
        break;
    case value2:
        // Code to execute if expression == value2
        break;
    ...
    default:
        // Code to execute if no case matches
}
```

>**expression:** Must evaluate to an integer or character type.
>**case value:**: Defines a block of code for a specific value.
>**break;**: Prevents fall-through to the next case (optional but recommended).
>**default:**: Executes if none of the cases match (optional).

<code>#include <stdio.h>
int main() {
    int day = 3;
    switch (day) {
        case 1:
            printf("Monday\n");
            break;
        case 2:
            printf("Tuesday\n");
            break;
        case 3:
            printf("Wednesday\n");
            break;
        case 4:
            printf("Thursday\n");
            break;
        default:
            printf("Invalid day\n");
    }
    return 0;
}</code>

Output: <code>Wednesday</code>

⚠️ If **break;** is omitted, execution continues into the next case.

<code>#include <stdio.h>
int main() {
    int num = 2;
    switch (num) {
        case 1:
            printf("One\n");
        case 2:
            printf("Two\n");
        case 3:
            printf("Three\n");
    }
    return 0;
}</code>

Output: <code>Two
Three</code>

>Here, since case 2 doesn’t have a break;, execution falls through to case 3.

**Using default Case**

The default case executes if no other case matches.

<code>int grade = 85;
switch (grade / 10) {  // Checking the tens digit
    case 10:
    case 9:
        printf("Grade: A\n");
        break;
    case 8:
        printf("Grade: B\n");
        break;
    case 7:
        printf("Grade: C\n");
        break;
    default:
        printf("Grade: F\n");
}</code>

>The switch expression must be an **integer** or **character**.
>Use **break;** to prevent fall-through behavior.
>**default** is optional but recommended.
>Cannot ~~use~~ floating-point numbers (float, double) as case values.
>case values must be constant expressions (no variables).

The switch-case is best suited when checking fixed values and improves code readability compared to long if-else if chains.

### Loops


### goto


# My Examples

## Control Statements

#### IF-statements

```C
#include <stdio.h>
  int main(){
  int value1, value2;
  printf("Type fisrt value:\n");
  scanf("%d", &value1);
  printf("Type second value:\n");
  scanf("%d", &value2);
  if(value1 > value2){
  printf("%d is bigger than %d\n", value1, value2);
  }if(value1 < value2){
  printf("%d is bigger than %d\n", value2, value1);
  }if(value1 == value2){
      printf("%d is equal to %d\n", value1, value2);
  }
  }
```

#### IF-ELSE-IF statements

```C
#include <stdio.h>
#define PI 3.14

int main(){
int radius, base, height;
float circleArea, triangleArea;
int choice;

    while(1){
        printf("Choose what area you want to find:\n");
        printf("0 - to find area of a circle\n");
        printf("1 - to find area of a triangle\n");
        printf("-1 - Exit program\n");
        scanf("%d", &choice);

        if(choice == 0){
            printf("You chose to find area of a circle. Type radius value:\n");
            scanf("%d", &radius);
            circleArea = PI * radius * radius;
            printf("The radius of a circle is %d, and its area is: %f\n", radius, circleArea);

        } else if(choice == 1){

            printf("You chose to find area of a triangle. Type base value:\n");
            scanf("%d", &base);

            printf("Type height value:\n");
            scanf("%d", &height);
            triangleArea = 0.5 * base * height;
            printf("The base of the triangle is %d, the height of the triangle is %d, and its area is: %f\n", base, height, triangleArea);
        } else if(choice == -1){
            printf("Exiting the program. Goodbye!\n");
            break;
        } else {
            printf("Invalid choice. Please try again.\n");
        }
    }
    return 0;
}</code>

#### SWITCH-case

<code>#include <stdio.h>
#define PI 3.14
int main() {
    int radius, base, height;
    float circleArea, triangleArea;
    int choice;
    while(1) {
        printf("Choose what area you want to find:\n");
        printf("0 - to find area of a circle\n");
        printf("1 - to find area of a triangle\n");
        printf("-1 - Exit program\n");
        scanf("%d", &choice);
         switch(choice) {
            case 0:
                printf("You chose to find area of a circle. Type radius value:\n");
                scanf("%d", &radius);
                circleArea = PI * radius * radius;
                printf("The radius of a circle is %d, and its area is: %f\n", radius, circleArea);
                break;
            case 1:
                printf("You chose to find area of a triangle. Type base value:\n");
                scanf("%d", &base);
                printf("Type height value:\n");
                scanf("%d", &height);
                triangleArea = 0.5 * base * height;
                printf("The base of the triangle is %d, the height of the triangle is %d, and its area is: %f\n", base, height, triangleArea);
                break;
            case -1:
                printf("Exiting the program. Goodbye!\n");
                return 0;  // Exits the program
            default:
                printf("Invalid choice. Please try again.\n");
                }
}
}
```

## Loops

#### while-loop: exampleone

<code>#include <stdio.h>
#define SIZE 100
int main() {
    int count = 0, input;
    int all_inputs[SIZE];
    int index = 0;
    printf("0 (zero) input will stop the program\n");
    printf("Type your values:\n");
    while (1) {
        scanf("%d", &input);  
        if (input == 50) {
            count++;
        }
        if (input == 0) {
            printf("All your inputs: ");
            for (int i = 0; i < index; i++) {
                printf("%d ", all_inputs[i]);
            }
            printf("\n50 was typed %d times\n", count);
            printf("Good bye!\n");
            break;
        }
        if (index < SIZE) {
            all_inputs[index] = input;
            index++;
        } else {
            printf("Input limit reached.\n");
            break;
        }
    }
    return 0;
}
</code>

#### while-loop: example two

<code>#include <stdio.h>
int main() {
    int goal, savings, months = 0;
    int total_savings = 0;
    printf("What is your savings goal?\n");
    scanf("%d", &goal);  // Added & to get the address of goal
    printf("How much do you save every month? \n");
    scanf("%d", &savings);  // Added & to get the address of savings
    while (total_savings < goal) {
        months++;
        total_savings += savings;
        printf("Months: %d \t Savings: %d\n", months, total_savings);  // Added \n for better output format
    }
    printf("Congratulations! You reached your savings goal in %d months!\n", months);
    return 0;
}
</code>

#### for-loop

<code>#include <stdio.h>
int main(){
int count;
for(count=0; count<=10; count++){
printf("%d\t", count);
}
return 0;
}
</code>

<code>#include <stdio.h>
int main() {
    int first_value, second_value, result;
    // Print the header row
    printf("\t");
    for (first_value = 1; first_value <= 10; first_value++) {
        printf("%d\t", first_value);
    }
    printf("\n");
    // Print the multiplication table
    for (first_value = 1; first_value <= 10; first_value++) {
        printf("%d\t", first_value);  // Print the first column
        for (second_value = 1; second_value <= 10; second_value++) {
            result = first_value * second_value;
            printf("%d\t", result);
        }
        printf("\n");  // Move to the next line after each row
    }
    return 0;
}
</code>

## Arrays

#### One-dimensional array

<code>#include <stdio.h>
#define SIZE 5
int main() {
    int nums[SIZE];  // Array to store values
    int input, count;
    printf("Enter your values:\n");
    // Loop to read values into the array
    for (count = 0; count < SIZE; count++) {
        scanf("%d", &nums[count]);  // Store input in the array
    }
    printf("The array is printed:\n");
    // Loop to print the values from the array
    for (count = 0; count < SIZE; count++) {
        printf("The value of element %d is %d\n", count, nums[count]);
    }
    return 0;
}
</code>

#### Groups of arrays

<code>#include <stdio.h>
int main() {
    int size;  
    printf("Enter the size of the array: ");
    scanf("%d", &size);
    if (size <= 0) {  
        printf("Invalid size. Exiting program.\n");
        return 1;  
    }
    int nums[size];  // Dynamically create an array of user-defined size
    int input, count = 0;
    printf("Enter your values (0 to stop):\n");
    while (count < size) {
        scanf("%d", &input);
        if (input == 0) {
            printf("The program stops.\n");
            break;
        }
        nums[count] = input;
        count++;
    }
    printf("\nStored values: ");
    for (int i = 0; i < count; i++) {
        printf("%d ", nums[i]);
    }
    printf("\n");
    // Grouping values in sets of 3 and calculating sums
    printf("\nSum of groups of 3:\n");
    for (int i = 0; i < count; i += 3) {
        int sum = 0;
        for (int j = 0; j < 3 && (i + j) < count; j++) {
            sum += nums[i + j];
        }
        printf("Group starting at index %d: Sum = %d\n", i, sum);
    }
    return 0;
}
</code>

#### Print array after each input

<code>#include <stdio.h>
int main(){
int size, input;
int count = 0;  
    printf("Enter the size of the array: ");
    scanf("%d", &size);
    if (size <= 0) {  
        printf("Invalid size. Exiting program.\n");
        return 1;  
    }
     int nums[size];  // Dynamically create an array of user-defined size
    int input, count = 0;
    printf("Enter your values (0 to stop):\n");
    while (count < size) {
        scanf("%d", &input);
        if (input == 0) {
            printf("The program stops.\n");
            break;
        }
        nums[count] = input;
        count++;
    }
    printf("\nStored values: ");
    for (int i = 0; i < count; i++) {
        printf("%d ", nums[i]);
    }
    return 0;
}
</code>

#### two-dimensional matrix

<code>#include <stdio.h>
#define ROWS 2
#define COLS 3
int main() {
    int matrix1[ROWS][COLS], matrix2[ROWS][COLS];
    // Input for first matrix
    printf("Enter values for the first 2x3 matrix:\n");
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            printf("Element [%d][%d]: ", i, j);
            scanf("%d", &matrix1[i][j]);
        }
    }
    // Input for second matrix
    printf("Enter values for the second 2x3 matrix:\n");
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            printf("Element [%d][%d]: ", i, j);
            scanf("%d", &matrix2[i][j]);
        }
    }
    // Adding matrices and storing result in matrix1
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            matrix1[i][j] += matrix2[i][j];
        }
    }
    // Printing the resulting matrix
    printf("\nResulting matrix after addition:\n");
    for (int i = 0; i < ROWS; i++) {
        for (int j = 0; j < COLS; j++) {
            printf("%d ", matrix1[i][j]);
        }
        printf("\n");
    }
    return 0;
}
</code>

## Functions

#### Addition

<code>#include <stdio.h>
int limit, result = 0;  // Initialize result to 0
void addition() {  
    printf("What is the limit: ");
    scanf("%d", &limit);
    printf("Sum calculation: ");
    for (int count = 0; count <= limit; count++) {  
        result += count;
        if (count == limit) {
            printf("%d = %d\n", count, result);  // No + after last number
        } else {
            printf("%d + ", count);  // Print + after every number except last
        }
    }
}
int main() {
    addition();
    return 0;
}
</code>

#### Different Operations 

<code>#include <stdio.h>
// Function declarations
void Intro();
int Choice();
void Addition();
void Multiplication();
int main() {
    char continue_program = 'y';  // Variable to control whether to continue asking for operations
    Intro();  // Print out what the program does
    while (continue_program != 'q') {  // Keep looping until 'q' is pressed
        int choice = Choice();  // Get user choice (0 for addition, 1 for multiplication)
        // Based on choice, call the appropriate function
        if (choice == 0) {
            Addition();  // Perform addition
        } else if (choice == 1) {
            Multiplication();  // Perform multiplication
        } else {
            printf("Invalid choice. Please enter 0 for addition or 1 for multiplication.\n");
        }
        // Ask the user what to do next
        printf("\nDo you want to perform a new operation?\n");
        printf("Enter 0 for addition, 1 for multiplication, or 'q' to quit: ");
        scanf(" %c", &continue_program);  // ' ' before %c is used to consume any leftover newline characters
    }
    printf("Exiting the program. Goodbye!\n");
    return 0;
}
// Function to introduce the program
void Intro() {
    printf("Welcome to the calculator program!\n");
    printf("You can either add or multiply numbers.\n");
    printf("After each operation, you can choose the next operation.\n");
}
// Function to ask the user for their choice (0 for addition, 1 for multiplication)
int Choice() {
    int choice;
    printf("\nWhat would you like to do? (0 for addition, 1 for multiplication): ");
    scanf("%d", &choice);
    return choice;
}
// Function for performing addition
void Addition() {
    int num1, num2;
    printf("Enter two numbers to add: ");
    scanf("%d %d", &num1, &num2);
    printf("The sum is: %d\n", num1 + num2);
}
// Function for performing multiplication
void Multiplication() {
    int num1, num2;
    printf("Enter two numbers to multiply: ");
    scanf("%d %d", &num1, &num2);
    printf("The result is: %d\n", num1 * num2);
}
</code>

#### Functions & global parameters

<code>#include <stdio.h>
// Global variables to store the values
int num1, num2;
// Function to read values into the global variables
void Read() {
    printf("Enter the first integer: ");
    scanf("%d", &num1);
    printf("Enter the second integer: ");
    scanf("%d", &num2);
}
// Function to swap the values of num1 and num2
void Switch() {
    int temp;
    temp = num1;
    num1 = num2;
    num2 = temp;
}
// Function to print the values of num1 and num2
void Print() {
    printf("After switching:\n");
    printf("First integer: %d\n", num1);
    printf("Second integer: %d\n", num2);
}
int main() {
    // Calling the Read function to input values
    Read();
    // Calling the Switch function to swap the values
    Switch();
    // Calling the Print function to display the results
    Print();
    return 0;
}
</code>

#### Functions & global parameters

<code>#include <stdio.h>
#define SIZE 10 // Maximum number of grades
// Global variable to count the number of zeroes
int zeroCount = 0;
// Function to read grades into the array
void Read(int grades[], int *numGrades) {
    int grade;
    *numGrades = 0; // Initialize the number of grades
    printf("Enter grades (0-5). Enter 99 to stop:\n");
    while (*numGrades < SIZE) {
        scanf("%d", &grade);
        // If a non-valid grade is entered, stop the input
        if (grade == 99) {
            break;
        }
        // Check if the grade is between 0 and 5
        if (grade >= 0 && grade <= 5) {
            grades[*numGrades] = grade;
            // Count zero grades
            if (grade == 0) {
                zeroCount++;
            }
            (*numGrades)++; // Increment the number of grades entered
        } else {
            printf("Invalid grade. Please enter a grade between 0 and 5, or 99 to stop.\n");
        }
    }
}
// Function to calculate the average grade
float Calculate(int grades[], int numGrades) {
    int sum = 0;
    // Calculate the sum of all grades
    for (int i = 0; i < numGrades; i++) {
        sum += grades[i];
    }
    // Return the average
    return (numGrades > 0) ? (float)sum / numGrades : 0.0;
}
// Function to print the results
void Print(float average) {
    printf("\nThe average grade is: %.2f\n", average);
    printf("The number of zeroes entered: %d\n", zeroCount);
}
int main() {
    int grades[SIZE]; // Array to store grades
    int numGrades;    // To store the actual number of grades entered
    // Call the Read function to input the grades
    Read(grades, &numGrades);
    // Call the Calculate function to compute the average
    float average = Calculate(grades, numGrades);
    // Call the Print function to display the results
    Print(average);
    return 0;
}
</code>

## Pointers

#### Basic pointer operations

```C
#include <stdio.h>
int main() {
    int var = 10;  // Declare an integer variable and assign it a value
    int *ptr;      // Declare an integer pointer
    ptr = &var;    // Assign the address of the variable to the pointer

    // Print the value of the variable
    printf("1. The value of the variable: %d\n", var);
    // Print the address of the variable
    printf("2. The address of the variable: %p\n", (void*)&var);
    // Print the memory address the pointer is pointing to
    printf("3. The memory address the pointer is pointing to: %p\n", (void*)ptr);
    // Print the contents of the memory location the pointer points to
    printf("4. The contents of the memory location the pointer points to: %d\n", *ptr);
    return 0;
}
```

#### Pointers and Arrays

<code>#include <stdio.h>
int main() {
    int arr[5];      // Declare an array of 5 integers
    int *ptr = arr;  // Declare a pointer and assign it to the array
    // Writing values to the array using the pointer
    printf("Enter 5 integer values:\n");
    for (int i = 0; i < 5; i++) {
        printf("Enter value for element %d: ", i+1);
        scanf("%d", ptr);  // Use pointer to assign values to the array
        ptr++;  // Move the pointer to the next element
    }
    // Reading and printing values starting from the last element using the pointer
    printf("\nValues in reverse order:\n");
    ptr--;  // Move the pointer to the last element in the array
    for (int i = 4; i >= 0; i--) {
        printf("Element %d: %d\n", i+1, *ptr);  // Dereference pointer to access value
        ptr--;  // Move the pointer to the previous element
    }
    return 0;
}
</code>

#### Bad example of pointers use

```C
int main(){
char *p_one;
char abc;
*p_one = 'A';
*p_one = &abc;
*p_one = 'b';
return 0;
}
```

🚨 Problem 1: char *p_one; is uninitialized
```C
char *p_one;
```
>[!Warning]
> A pointer is declared, but it points to nowhere — it contains garbage.

🚨 Problem 2: <code>*p_one = 'A';</code>

 'A' has  an unknown memory location:

 ```C
*p_one = 'A';
```

>[!Warning]
>This is undefined behavior and usually causes a segmentation fault or crash, because you're dereferencing a pointer that was never initialized or assigned a valid address.

🚨 Problem 3: <code>*p_one = &abc;</code>

```C
*p_one = &abc;
```

<code>*p_one</code> is a char (a single byte), and you're trying to store a char * (a memory address) in that single byte. This:
Makes no sense in terms of types
Is almost guaranteed to corrupt memory
Might trigger a compiler warning like:

<code>warning: assignment makes integer from pointer without a cast</code>

>[!Warning]
>It doesn’t change where p_one points — it only writes garbage (the address of abc) into a single byte of memory that’s already invalid.

Problem 4: <code>*p_one = 'b';</code>

>[!Warning]
>Random garbage location, undefined behavior.

**How to fix**

```C
int main() {
    char *p_one;
    char abc;

    p_one = &abc;   // ✅ Make p_one point to abc
    *p_one = 'A';   // ✅ Now abc = 'A'
    *p_one = 'b';   // ✅ abc = 'b'

    printf("abc = %c\n", abc);  // Outputs: abc = b
    return 0;
}
```

#### String length

<code>#include <stdio.h>
#include <string.h>  // Include for strlen function
int main() {
    char data[] = "Hello World";  // The string we are working with
    int length = 0;  // To store length of string
    // 1. Using a simple loop (without pointers)
    for (int i = 0; data[i] != '\0'; i++) {
        length++;
    }
    printf("Length using loop: %d\n", length);
    // 2. Using a char pointer to loop through the array
    char *ptr = data;  // Pointer to the first element of the string
    int length_with_pointer = 0;
    while (*ptr != '\0') {
        length_with_pointer++;
        ptr++;  // Move pointer to the next character
    }
    printf("Length using pointer: %d\n", length_with_pointer);
    // 3. Using strlen function to find the length of the string
    int length_with_strlen = strlen(data);
    printf("Length using strlen: %d\n", length_with_strlen);
    return 0;
}
</code>

#### Char Arrays

<code>#include <stdio.h>
int main() {
    char array1[50], array2[50], combined[100];  // Arrays for the two inputs and the combined result
    char *ptr1, *ptr2, *ptr_combined;
    // Get input from the user
    printf("Enter the first string: ");
    gets(array1);  // unsafe, used for this task per instruction
    printf("Enter the second string: ");
    gets(array2);  // unsafe, used for this task per instruction
    // Pointers to the start of each array
    ptr1 = array1;
    ptr2 = array2;
    ptr_combined = combined;
    // Copy contents of array1 to combined array using pointer
    while (*ptr1 != '\0') {
        *ptr_combined = *ptr1;  // Copy character from array1 to combined
        ptr_combined++;  // Move pointer in combined array
        ptr1++;  // Move pointer in array1
    }
    // Copy contents of array2 to combined array using pointer
    while (*ptr2 != '\0') {
        *ptr_combined = *ptr2;  // Copy character from array2 to combined
        ptr_combined++;  // Move pointer in combined array
        ptr2++;  // Move pointer in array2
    }
    // Null-terminate the combined array
    *ptr_combined = '\0';
    // Print the combined string
    printf("Combined string: ");
    puts(combined);
    return 0;
}
</code>

#### Pointers and Functions

```C
#include <stdio.h>
#define SIZE 5  // Define the size of the arrays
// Global array declaration
int global_array[SIZE];

// Function to read data into an array
void Read_data(int *arr) {
    printf("Enter %d integer values:\n", SIZE);
    for (int i = 0; i < SIZE; i++) {
        scanf("%d", &arr[i]);  // Read values into the local array
    }
}
// Function to move data from the local array to the global array
// Adding 20 to each element in the process
void Move(int *arr) {
    for (int i = 0; i < SIZE; i++) {
        global_array[i] = arr[i] + 20;  // Copy and add 20 to each element
    }
}
// Function to print an array passed by pointer
void Print(int *arr) {
    for (int i = 0; i < SIZE; i++) {
        printf("%d ", arr[i]);  // Print the array element
    }
    printf("\n");
}

int main() {
    int local_array[SIZE];  // Local array declared in main
    // Read data into the local array
    Read_data(local_array);
    // Print the original local array
    printf("\nOriginal array:\n");
    Print(local_array);
    // Move data from the local array to the global array with addition
    Move(local_array);
    // Print the modified global array
    printf("\nModified global array (after adding 20 to each element):\n");
    Print(global_array);
    return 0;
}
```

#### Stack

```C
#include <stdio.h>
#include <stdlib.h>
#define SIZE 10  // Define the size of the stack

// Function to push an element onto the stack
int* Push(int* stack_ptr, int* stack_end) {

    int value;
    // Check if the stack is full
    if (stack_ptr >= stack_end) {
        printf("Stack is full! Cannot push more elements.\n");
        return NULL;  // Stack is full, return NULL
    }
    // Ask user for an integer value to add to the stack
    printf("Enter a number to push onto the stack: ");
    scanf("%d", &value);
    // Push the value and move the pointer to the next position
    *stack_ptr = value;
    stack_ptr++;
    return stack_ptr;  // Return the new stack pointer
}
// Function to pop an element from the stack
int* Pop(int* stack_ptr, int* stack_start) {
    // Check if the stack is empty
    if (stack_ptr == stack_start) {
        printf("Stack is empty! Cannot pop any elements.\n");
        return NULL;  // Stack is empty, return NULL
    }
    // Move the stack pointer one step back to remove the last element
    stack_ptr--;
    printf("Popped value: %d\n", *stack_ptr);  // Show the popped value
    return stack_ptr;  // Return the new stack pointer
}
// Function to show the contents of the stack
void Show(int* stack_ptr, int* stack_start) {
    if (stack_ptr == stack_start) {
        printf("Stack is empty!\n");
        return;
    }
    // Print elements in the stack starting from the last added item
    printf("Stack contents (top to bottom):\n");
    for (int* ptr = stack_ptr - 1; ptr >= stack_start; ptr--) {
        printf("%d\n", *ptr);
    }
}

int main() {
    int stack[SIZE];  // Define a stack array with a fixed size
    int* stack_ptr = stack;  // Pointer to the top of the stack
    int* stack_start = stack;  // Pointer to the bottom (start) of the stack
    int* stack_end = stack + SIZE;  // Pointer to the end of the stack
    int choice;
    
    while (1) {
    
        // Ask the user for an action
        printf("\nStack Operations Menu:\n");
        printf("1. Push an element onto the stack\n");
        printf("2. Pop an element from the stack\n");
        printf("3. Show the contents of the stack\n");
        printf("4. Quit\n");
        printf("Choose an option (1-4): ");
        scanf("%d", &choice);
        
        switch (choice) {
            case 1:
                stack_ptr = Push(stack_ptr, stack_end);  // Push operation
                break;
            case 2:
                stack_ptr = Pop(stack_ptr, stack_start);  // Pop operation
                break;
            case 3:
                Show(stack_ptr, stack_start);  // Show stack contents
                break;
            case 4:
                printf("Exiting program.\n");
                return 0;  // Exit the program
            default:
                printf("Invalid choice! Please choose a valid option.\n");
        }
    }
    return 0;
}
```

## Signal Generator

#### Square wave

```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>
#include <sndfile.h>
#ifndef M_PI
#define M_PI 3.14159265358979323846264338
#endif
#define SAMPLE_RATE 44100
#define SAMPLE_COUNT (SAMPLE_RATE * 4) /* 4 seconds */
#define AMPLITUDE (1.0 * 0x7F000000)    /* Max amplitude */

int main(void)
{
    SNDFILE *file;
    SF_INFO sfinfo;
    int k;
    int buffer[SAMPLE_COUNT]; // FIXED THE ARRAY ALLOCATION
    memset(&sfinfo, 0, sizeof(sfinfo));
    sfinfo.samplerate = SAMPLE_RATE;
    sfinfo.frames = SAMPLE_COUNT;
    sfinfo.channels = 1;
    sfinfo.format = (SF_FORMAT_WAV | SF_FORMAT_PCM_24);
    file = sf_open("square_wave.wav", SFM_WRITE, &sfinfo);
    
    if (file == NULL)
    {
        printf("Error: Not able to open output file.\n");
        return 1;
    }
    // GENERATE SQUARE WAVE: TWO SAMPLES HIGH, TWO SAMPLES LOW
    for (k = 0; k < SAMPLE_COUNT; k++)
    {
        if ((k / 2) % 2 == 0) // Every two samples, toggle between high and low
            buffer[k] = AMPLITUDE;
        else
            buffer[k] = 0;
    }
    if (sf_write_int(file, buffer, sfinfo.channels * SAMPLE_COUNT) != sfinfo.channels * SAMPLE_COUNT)
    {
        puts(sf_strerror(file));
    }
    sf_close(file);
    return 0;
}
```

####  Square Wave Using a Sum of Sine Waves

```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>
#include <sndfile.h>

#ifndef M_PI
#define M_PI 3.14159265358979323846264338
#endif
#define SAMPLE_RATE 44100
#define SAMPLE_COUNT (SAMPLE_RATE * 4) /* 4 seconds */
#define AMPLITUDE (0.7 * 0x7F000000)    /* Adjusted amplitude to prevent clipping */
#define BASE_FREQ 344.0                 /* Base frequency of the square wave */

int main(void)
{
    SNDFILE *file;
    SF_INFO sfinfo;
    int k;
    double t;
    int buffer[SAMPLE_COUNT]; 
    memset(&sfinfo, 0, sizeof(sfinfo));
    sfinfo.samplerate = SAMPLE_RATE;
    sfinfo.frames = SAMPLE_COUNT;
    sfinfo.channels = 1;
    sfinfo.format = (SF_FORMAT_WAV | SF_FORMAT_PCM_24);
    file = sf_open("square_wave_fourier.wav", SFM_WRITE, &sfinfo);

    if (file == NULL)
    {
        printf("Error: Not able to open output file.\n");
        return 1;
    }
    // Generate square wave using Fourier series
    for (k = 0; k < SAMPLE_COUNT; k++)
    {
        t = (double)k / SAMPLE_RATE;
        // Fourier series: sin(ωt) + (1/3)sin(3ωt) + (1/5)sin(5ωt) + (1/7)sin(7ωt)
        double sample = sin(2 * M_PI * BASE_FREQ * t)
                        + (1.0 / 3.0) * sin(2 * M_PI * 3 * BASE_FREQ * t)
                        + (1.0 / 5.0) * sin(2 * M_PI * 5 * BASE_FREQ * t)
                        + (1.0 / 7.0) * sin(2 * M_PI * 7 * BASE_FREQ * t);
        buffer[k] = (int)(AMPLITUDE * sample); // Scale and store in buffer
    }
    if (sf_write_int(file, buffer, sfinfo.channels * SAMPLE_COUNT) != sfinfo.channels * SAMPLE_COUNT)
    {
        puts(sf_strerror(file));
    }
    sf_close(file);
    return 0;
}
```

####  Splitting Sinal Generator program Up Into Functions

```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>
#include <sndfile.h>

#ifndef M_PI
#define M_PI 3.14159265358979323846264338
#endif
#define SAMPLE_RATE 44100
#define SAMPLE_COUNT (SAMPLE_RATE * 4) /* 4 seconds */
#define AMPLITUDE (0.7 * 0x7F000000)    /* Adjust amplitude to prevent clipping */
#define BASE_FREQ 344.0                 /* Base frequency of the square wave */

SNDFILE *file;     // Global file pointer
SF_INFO sfinfo;    // Global structure for file info
int buffer[SAMPLE_COUNT]; // Global buffer for audio samples

// Function to set up the WAV file
void setup(const char *filename)
{
    memset(&sfinfo, 0, sizeof(sfinfo));
    sfinfo.samplerate = SAMPLE_RATE;
    sfinfo.frames = SAMPLE_COUNT;
    sfinfo.channels = 1;
    sfinfo.format = (SF_FORMAT_WAV | SF_FORMAT_PCM_24);
    file = sf_open(filename, SFM_WRITE, &sfinfo);

    if (file == NULL)
    {
        printf("Error: Unable to open output file.\n");
        exit(1);
    }
}
// Function to generate the square wave using Fourier series
void generate()
{
    for (int k = 0; k < SAMPLE_COUNT; k++)
    {
        double t = (double)k / SAMPLE_RATE;
        // Square wave approximation using Fourier series
        double sample = sin(2 * M_PI * BASE_FREQ * t)
                        + (1.0 / 3.0) * sin(2 * M_PI * 3 * BASE_FREQ * t)
                        + (1.0 / 5.0) * sin(2 * M_PI * 5 * BASE_FREQ * t)
                        + (1.0 / 7.0) * sin(2 * M_PI * 7 * BASE_FREQ * t);
        buffer[k] = (int)(AMPLITUDE * sample); // Scale and store in buffer
    }
    if (sf_write_int(file, buffer, sfinfo.channels * SAMPLE_COUNT) != sfinfo.channels * SAMPLE_COUNT)
    {
        puts(sf_strerror(file));
    }
}
// Function to close the WAV file
void finish()
{
    sf_close(file);
}
// Main function
int main(void)
{
    setup("square_wave_fourier.wav");
    generate();
    finish();
    printf("WAV file successfully created!\n");
    return 0;
}
```

#### Signal Generator, User Input

```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>
#include <sndfile.h>
#ifndef M_PI

#define M_PI 3.14159265358979323846264338
#endif
#define SAMPLE_RATE 44100
#define SAMPLE_COUNT (SAMPLE_RATE * 4) /* 4 seconds */
#define AMPLITUDE (0.7 * 0x7F000000)    /* Prevent clipping */

SNDFILE *file;     // Global file pointer
SF_INFO sfinfo;    // Global structure for file info
int buffer[SAMPLE_COUNT]; // Global buffer for audio samples
int base_freq;     // User-defined frequency

// Function to get user input for filename and frequency
void get_user_input(char *filename)
{
    printf("Enter output filename (e.g., output.wav): ");
    fgets(filename, 100, stdin); // Read filename input
    filename[strcspn(filename, "\n")] = 0; // Remove newline character
    printf("Enter base frequency in Hz (e.g., 440): ");
    scanf("%d", &base_freq);
}
// Function to set up the WAV file
void setup(const char *filename)
{
    memset(&sfinfo, 0, sizeof(sfinfo));
    sfinfo.samplerate = SAMPLE_RATE;
    sfinfo.frames = SAMPLE_COUNT;
    sfinfo.channels = 1;
    sfinfo.format = (SF_FORMAT_WAV | SF_FORMAT_PCM_24);
    file = sf_open(filename, SFM_WRITE, &sfinfo);
    
    if (file == NULL)
    {
        printf("Error: Unable to open output file.\n");
        exit(1);
    }
}
// Function to generate the square wave using Fourier series
void generate()
{
    for (int k = 0; k < SAMPLE_COUNT; k++)
    {
        double t = (double)k / SAMPLE_RATE;
        // Square wave approximation using Fourier series
        double sample = sin(2 * M_PI * base_freq * t)
                        + (1.0 / 3.0) * sin(2 * M_PI * 3 * base_freq * t)
                        + (1.0 / 5.0) * sin(2 * M_PI * 5 * base_freq * t)
                        + (1.0 / 7.0) * sin(2 * M_PI * 7 * base_freq * t);
        buffer[k] = (int)(AMPLITUDE * sample); // Scale and store in buffer
    }
    if (sf_write_int(file, buffer, sfinfo.channels * SAMPLE_COUNT) != sfinfo.channels * SAMPLE_COUNT)
    {
        puts(sf_strerror(file));
    }
}
// Function to close the WAV file
void finish()
{
    sf_close(file);
}
// Main function
int main(void)

{
    char filename[100];
    get_user_input(filename);
    setup(filename);
    generate();
    finish();
    printf("WAV file '%s' successfully created with frequency %d Hz!\n", filename, base_freq);
    return 0;
}
```

> Provide a C source code file which has the following characteristics
> filename make_sine.c
> it can be  compiled with the command gcc -Wall make_sine.c -lsndfile -lm
> When the program is run, it produces a .wav file which contains a 1000Hz sine signal.

```C
#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <sndfile.h>

#ifndef M_PI
#define M_PI 3.14159265358979323846
#endif

#define SAMPLE_RATE     44100
#define DURATION        4
#define SAMPLE_COUNT    (SAMPLE_RATE * DURATION)
#define FREQUENCY       1000.0
#define AMPLITUDE       (0.8 * 0x7FFFFF)  // Scaled to avoid clipping for 24-bit

int main(void)
{
    SNDFILE *file;
    SF_INFO sfinfo;
    int buffer[SAMPLE_COUNT];
    int k;

    // Clear the SF_INFO struct
    memset(&sfinfo, 0, sizeof(sfinfo));

    // Set format details
    sfinfo.samplerate = SAMPLE_RATE;
    sfinfo.frames     = SAMPLE_COUNT;
    sfinfo.channels   = 1;
    sfinfo.format     = SF_FORMAT_WAV | SF_FORMAT_PCM_24;

    // Open file for writing
    file = sf_open("sine.wav", SFM_WRITE, &sfinfo);
    if (file == NULL)
    {
        puts("Error: Could not open file for writing.");
        puts(sf_strerror(NULL));
        return 1;
    }

    // Generate sine wave samples
    for (k = 0; k < SAMPLE_COUNT; k++)
    {
        double t = (double)k / SAMPLE_RATE;
        buffer[k] = (int)(AMPLITUDE * sin(2.0 * M_PI * FREQUENCY * t));
    }

    // Write to file
    if (sf_write_int(file, buffer, SAMPLE_COUNT) != SAMPLE_COUNT)
    {
        puts("Error writing to file.");
        puts(sf_strerror(file));
        sf_close(file);
        return 1;
    }

    // Close file
    sf_close(file);
    puts("WAV file 'sine.wav' created successfully.");
    return 0;
}

```





















