# C Preprocessor
In C programming, the preprocessor is a stage of the compilation process that operates before the actual compilation of the source code begins. It processes the source code before it is passed to the compiler. The preprocessor directives are special instructions that tell the preprocessor how to manipulate the source code before it is compiled.

Preprocessor directives start with a `#` symbol and are not considered part of the C language itself. They are used to include header files, define constants, conditionally compile code, and perform other text manipulations. Here are some commonly used preprocessor directives:

1. **Include Directive (`#include`)**
   - The `#include` directive is used to include the contents of a header file into your source code. Header files typically contain function prototypes, macros, and declarations that you want to use in your program.

   ```c
   #include <stdio.h>
   ```

   You can also include user-defined header files using double-quotes:

   ```c
   #include "myheader.h"
   ```

2. **Macro Definition (`#define`)**
   - The `#define` directive is used to create macros, which are text substitutions. Macros are often used for constants or to create simple functions.

   ```c
   #define PI 3.14159265
   ```

   After this directive, every occurrence of `PI` in your code will be replaced with `3.14159265`.

3. **Conditional Compilation (`#ifdef`, `#ifndef`, `#else`, `#endif`)**
   - Conditional directives are used to include or exclude code from the compilation based on conditions.

   ```c
   #ifdef DEBUG
   // Debugging code here
   #else
   // Release code here
   #endif
   ```

   You can define the `DEBUG` symbol using `-D` compiler option or via a `#define` directive.

4. **File Inclusion (`#pragma once`)**
   - The `#pragma once` directive is used to ensure that a header file is included only once in a translation unit. It helps prevent multiple inclusions of the same header.

   ```c
   #pragma once
   ```

5. **Conditional Inclusion (`#if`, `#elif`, `#else`, `#endif`)**
   - These directives are used for more complex conditional compilation based on expressions.

   ```c
   #if defined(PLATFORM_LINUX)
   // Linux-specific code
   #elif defined(PLATFORM_WINDOWS)
   // Windows-specific code
   #else
   // Code for other platforms
   #endif
   ```

6. **Stringization (`#` Operator)**
   - The `#` operator is used for stringizing (converting a macro argument into a string).

   ```c
   #define STRINGIZE(x) #x
   printf("%s\n", STRINGIZE(Hello)); // Prints "Hello"
   ```

These are some of the common preprocessor directives in C. They are powerful tools that allow you to control the compilation process, customize your code for different platforms, and manage configuration settings.
