# C Compiler
A C compiler is a software tool that translates the human-readable C programming code into machine-readable code, which is typically in the form of machine code or assembly language. The machine-readable code is specific to the target computer's architecture and can be directly executed by the computer's processor.

The compilation process involves several stages:

<img src="https://github.com/kmitsolution/CLanguage/blob/main/Core/images/CCompiler.jpg" width=900 height=500 />

### Preprocessing:
The preprocessor stage processes the C source code before actual compilation. It handles directives that start with the "#" symbol, such as #include (for including header files) and #define (for macros). The preprocessor replaces these directives with the appropriate code, preparing the source code for the next stage.

For example: If you include <b> #include <stdio.h> </b> then preprocessor add the code of stdio.h in to your program.

With below command in gcc compiler to execute the preprocessor step. (let's consider main.c is a source C lanaguage code) 
```
gcc -E main.c
```
### Compilation: 
The compiler takes the preprocessed C source code and translates it into assembly code or intermediate code specific to the target architecture. The generated code represents the program's instructions in a human-readable format.

Below command is compiling the code ( it is performing 2 steps, Preporocessing and Converting the code into assembly language)
```
gcc -S main.c
```
It will produce a file <b> main.s </b> which includes the assembly code.

### Assembly:
If the compiler generates assembly code, the assembler converts the assembly code into machine code, which is a low-level representation of the program instructions, understood by the computer's hardware.

Below command is converting main.c file code into binary code and you can produce a binary file
```
gcc main.c -o main.o
```
### Linking:
The linker combines the machine code generated from different source files and library files to produce an executable binary file. It resolves external references and ensures all the required functions and libraries are present.

```
gcc main.c 
```
It will perform all the steps like preprocessing,compiling,assembly and produce a.exe in windows a.out in linux.

Once the compilation process is complete, the resulting executable file can be executed directly on the target computer.

## Popular C compilers include:

### GCC (GNU Compiler Collection):
GCC is a widely used open-source compiler that supports various programming languages, including C. It is available for multiple platforms and architectures and is known for its efficiency and optimization capabilities.
### Clang: 
Clang is another open-source C compiler that is part of the LLVM (Low-Level Virtual Machine) project. It aims to be highly compatible with GCC while providing better error messages and faster compilation times.
### Microsoft Visual C++: 
This compiler is part of Microsoft's Visual Studio IDE and is commonly used for Windows-based C/C++ development.
### Intel C Compiler (ICC):
ICC is a proprietary C compiler developed by Intel and is known for its advanced optimization features, particularly for Intel processors.
### Tiny C Compiler (TCC): 
TCC is a small and fast C compiler that focuses on simplicity and quick compilation.
### Digital Mars C/C++ Compiler (DMC):
DMC is a compiler for C and C++ developed by Digital Mars and is available for Windows.

It's important to choose a C compiler that matches your development needs, platform, and performance requirements. GCC is often the default choice for many developers due to its widespread usage and strong community support.
