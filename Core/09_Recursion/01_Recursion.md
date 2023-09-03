Recursion is a powerful and fundamental concept in computer science and programming that allows a function to call itself. In C, as in many programming languages, you can create recursive functions. Recursive functions are used to solve problems that can be broken down into smaller, similar subproblems. Here's a basic example of a recursive function in C:

```c
#include <stdio.h>

// Recursive function to calculate the factorial of a non-negative integer
unsigned long long factorial(int n) {
    if (n == 0) {
        return 1; // Base case: factorial of 0 is 1
    } else {
        return n * factorial(n - 1); // Recursive case: n! = n * (n-1)!
    }
}

int main() {
    int num = 5;
    
    // Function call
    unsigned long long result = factorial(num);
    
    printf("Factorial of %d is %llu\n", num, result);
    
    return 0;
}
```

In this example:

1. We define a recursive function `factorial` that calculates the factorial of a non-negative integer `n`. The factorial of `n` is defined as `n! = n * (n-1)!`.

2. The function has a base case, which is when `n` equals 0. In this case, it returns 1 because the factorial of 0 is 1.

3. In the recursive case, the function calls itself with the argument `n - 1`, multiplying the result by `n`. This process continues until the base case is reached.

4. In the `main` function, we call the `factorial` function with `num = 5` and print the result.

When you run this program, it will calculate and display the factorial of 5, which is 5! = 5 * 4 * 3 * 2 * 1 = 120.

Recursion is a powerful technique for solving problems that exhibit a recursive or self-referencing structure. However, it's essential to ensure that your recursive function has a base case to prevent infinite recursion.
