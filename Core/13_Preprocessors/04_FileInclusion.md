File inclusion in the C preprocessor is done using the `#include` directive. This directive allows you to include the contents of another file in your C source code. This is commonly used to include header files containing function prototypes, constants, and macros. Here's how you use the `#include` directive in the preprocessor with an example:

Suppose you have a header file named `myheader.h` that contains the following content:

```c
// myheader.h
#ifndef MYHEADER_H
#define MYHEADER_H

void printHello();

#endif
```

Now, let's create a C source file (`main.c`) that includes this header file and uses the functions declared in it:

```c
// main.c
#include <stdio.h>     // Standard library header
#include "myheader.h"  // User-defined header

int main() {
    printf("Hello from main.c\n");
    printHello();  // Call the function declared in myheader.h
    return 0;
}
```

In the `main.c` file, you use the `#include` directive to include the standard header file `<stdio.h>` and your user-defined header file `"myheader.h"`.

Here's what happens when you compile this code:

1. The C preprocessor processes the `main.c` file before the actual compilation. It looks for `#include` directives.

2. When it encounters `#include <stdio.h>`, it includes the contents of the standard C library's `stdio.h` header file. This provides declarations for functions like `printf()`.

3. When it encounters `#include "myheader.h"`, it includes the contents of your `myheader.h` header file. This provides the declaration for the `printHello()` function.

4. The resulting preprocessed code is passed to the compiler, which compiles it into an executable.

Note that you should use angle brackets (`< >`) with system header files, like `<stdio.h>`, and double quotes (`" "`) with your own header files or files located in the same directory as your source code.

By including header files, you can organize your code, declare functions, constants, and macros in separate files, and promote code reusability and modularity in your C programs.
