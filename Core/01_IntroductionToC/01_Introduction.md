# C Programming Language
C programming language is a powerful and widely used general-purpose programming language. It was originally developed at <b>Bell Labs by Dennis Ritchie </b> between 1969 and 1973 to design the UNIX operating system. Since then, C has become one of the most popular and influential programming languages in the world.

Key features of the C programming language include:
### Procedural Language: 
C is a procedural programming language, which means it follows a step-by-step procedure for solving problems. It uses functions to structure the code and divide the program into smaller, manageable tasks.

Below is the example for procedural code in c. I have created 2 functions/procedures called calc1() and calc2() and invoked in main()
```c
#include <stdio.h>
//Procedure1
void calc1(){
    printf("This is calc1");
}
//Procedure2
void calc2(){
    printf("\nThis is calc2");
}
void main(){
   calc1();//call the calc1()
   calc2();//call the calc2()
}
```
### Portability: 
C programs can be easily ported or moved across different platforms and operating systems with minimal changes. This portability is one of the reasons for C's popularity in system-level programming.
### Efficiency:
C is known for its efficiency and high performance. It provides low-level access to memory and system resources, allowing programmers to write efficient code.
### Modularity:
C allows breaking down complex problems into smaller modules (functions), making the code easier to understand, maintain, and reuse.
### Rich Library Support:
C comes with a standard library that provides various functions for common tasks, such as input/output operations, string manipulation, memory allocation, and mathematical functions.
### Pointer Support:
Pointers in C allow direct memory manipulation, which provides more control over memory and efficient data handling.
### Wide Application: 
C is used in various domains, including system programming, embedded systems, game development, scientific applications, and more.

A simple "Hello, World!" program in C looks like this:

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

### Explanation:

#### #include <stdio.h>:
This line includes the standard input-output library, which provides the printf function.
#### int main(): 
The main function is the entry point of a C program.
#### printf("Hello, World!\n"):
The printf function is used to print the text "Hello, World!" to the console.
#### return 0;:
The main function returns an integer value, typically 0 to indicate successful execution.

To compile and run a C program, you need a C compiler installed on your computer, such as <b>GCC (GNU Compiler Collection)</b>. Once you have the compiler set up, you can use the command line to compile the code and generate an executable file.

C serves as a foundation for many other programming languages and has greatly influenced the development of modern programming languages. Learning C is an excellent starting point for anyone interested in programming, as it helps build a strong foundation in programming concepts and techniques.
