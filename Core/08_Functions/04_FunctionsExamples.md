Certainly! Here are more examples of functions without recursion:

**1. Function to Find the Maximum of Two Numbers:**
```c
#include <stdio.h>

// Function declaration
int findMax(int a, int b);

int main() {
    int num1 = 5, num2 = 7;
    
    // Function call
    int max = findMax(num1, num2);
    
    printf("Maximum: %d\n", max);
    
    return 0;
}

// Function definition
int findMax(int a, int b) {
    return (a > b) ? a : b;
}
```

In this example, the `findMax` function takes two integers as parameters and returns the maximum of the two.

**2. Function to Calculate the Square of a Number:**
```c
#include <stdio.h>

// Function declaration
int square(int x);

int main() {
    int num = 5;
    
    // Function call
    int result = square(num);
    
    printf("Square: %d\n", result);
    
    return 0;
}

// Function definition
int square(int x) {
    return x * x;
}
```

This example defines a function `square` that takes an integer as a parameter and returns its square.

**3. Function to Check if a Number is Even:**
```c
#include <stdio.h>

// Function declaration
int isEven(int x);

int main() {
    int num = 10;
    
    // Function call
    if (isEven(num)) {
        printf("%d is even.\n", num);
    } else {
        printf("%d is odd.\n", num);
    }
    
    return 0;
}

// Function definition
int isEven(int x) {
    return (x % 2 == 0);
}
```

In this example, the `isEven` function checks if a given integer is even and returns 1 (true) if it is, or 0 (false) if it's odd.

These examples illustrate various functions that perform different tasks without using recursion. Functions in C can handle a wide range of tasks and calculations, making them essential for code organization and reusability.
