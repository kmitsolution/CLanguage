# Functions in C
Functions are fundamental in the C programming language, allowing you to encapsulate reusable blocks of code. Here are the basics of creating and using functions in C:

**Function Definition:**
A function in C consists of a function declaration and a function body. Here's the syntax for defining a function:

```c
return_type function_name(parameters) {
    // Function body
    // Code to be executed
    return return_value; // Optional return statement
}
```

- `return_type`: The data type of the value that the function returns (use `void` if the function doesn't return a value).
- `function_name`: The name of the function.
- `parameters`: Input values (arguments) passed to the function. These are optional but can be used to pass information to the function.
- `return_value`: The value returned by the function (if it's not `void`).

**Function Declaration:**
Before you can use a function in your code, you typically need to declare it. A function declaration specifies the function's name, return type, and parameters. It informs the compiler about the function's existence.

```c
return_type function_name(parameters); // Function declaration
```

**Function Call:**
To execute a function, you need to call it in your code. You call a function by using its name followed by parentheses containing the arguments (if any).

```c
return_type result = function_name(arguments); // Function call
```

**Example of a Simple Function:**

Here's an example of a simple function that adds two integers and returns the result:

```c
#include <stdio.h>

// Function declaration
int add(int a, int b);

int main() {
    int num1 = 5, num2 = 7;
    
    // Function call
    int sum = add(num1, num2);
    
    printf("Sum: %d\n", sum);
    
    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}
```

In this example:
- We declare the `add` function with the `int` return type and two `int` parameters.
- In the `main` function, we call `add` with two integers and store the result in the `sum` variable.
- The `add` function definition calculates the sum of its two parameters and returns the result.

**Function Prototypes:**
In C, it's common to declare a function prototype before the `main` function if the function definition appears later in the code. The prototype informs the compiler about the function's name, return type, and parameters so that it can correctly handle function calls.

```c
return_type function_name(parameters); // Function prototype
```

In summary, functions are essential for structuring your C code, promoting reusability, and making your code more manageable. They allow you to break down complex tasks into smaller, more manageable parts and facilitate code organization and maintenance.
