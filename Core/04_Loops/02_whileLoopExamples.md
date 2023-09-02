# Example of while loop in C

### 1. Find the factorial of a positive number

```c
#include <stdio.h>

int main() {
    int num;
    long long factorial = 1;

    // Prompt the user to enter a positive integer
    printf("Enter a positive integer: ");
    scanf("%d", &num);

    // Check if the input is a non-negative integer
    if (num < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } else {
        // Calculate the factorial using a while loop
        int i = 1;
        while (i <= num) {
            factorial *= i;
            i++;
        }

        // Display the result
        printf("Factorial of %d = %lld\n", num, factorial);
    }

    return 0;
}
```

In this example:

1. The program prompts the user to enter a positive integer.

2. It checks if the input number is negative. If it's negative, it displays an error message because factorial is not defined for negative numbers.

3. If the input is non-negative, a `while` loop is used to calculate the factorial of the number. The `factorial` variable is initialized to 1, and the loop iterates from 1 to `num`, multiplying `factorial` by `i` in each iteration.

4. After the loop completes, the program displays the factorial of the input number.

This example demonstrates how a `while` loop can be used to perform a repetitive task until a specific condition is met. It calculates the factorial of a number, which is a common mathematical operation.

## Simple Calculator
Creating a simple calculator in C using a `while` loop is a common programming exercise. Here's a basic example of a calculator that performs addition, subtraction, multiplication, and division operations based on user input:

```c
#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    while (1) { // Infinite loop until the user chooses to exit
        // Prompt the user for operator choice
        printf("Choose an operation (+, -, *, /) or 'q' to quit: ");
        scanf(" %c", &operator);

        // Check if the user wants to quit
        if (operator == 'q' || operator == 'Q') {
            printf("Calculator exiting.\n");
            break; // Exit the loop
        }

        // Prompt the user for two numbers
        printf("Enter first number: ");
        scanf("%lf", &num1);
        printf("Enter second number: ");
        scanf("%lf", &num2);

        // Perform the selected operation
        switch (operator) {
            case '+':
                result = num1 + num2;
                printf("Result: %.2lf\n", result);
                break;
            case '-':
                result = num1 - num2;
                printf("Result: %.2lf\n", result);
                break;
            case '*':
                result = num1 * num2;
                printf("Result: %.2lf\n", result);
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    printf("Result: %.2lf\n", result);
                } else {
                    printf("Division by zero is not allowed.\n");
                }
                break;
            default:
                printf("Invalid operator. Please try again.\n");
        }
    }

    return 0;
}
```

In this program:

1. The `while (1)` loop creates an infinite loop that continues until the user chooses to exit by entering 'q' or 'Q'.

2. Inside the loop, the user is prompted to choose an operation ('+', '-', '*', or '/') or 'q' to quit.

3. Based on the selected operator, the user is prompted to enter two numbers.

4. The program performs the selected operation using a `switch` statement and displays the result. If the user attempts to divide by zero, it shows an error message.

5. If the user enters an invalid operator, the program displays an error message.

6. To exit the calculator, the user can enter 'q' or 'Q', which breaks out of the loop, ending the program.

This simple calculator allows the user to perform basic arithmetic operations repeatedly until they decide to quit.

### Fibonacci Series 
You can generate a Fibonacci series using a `while` loop in C. The Fibonacci series is a sequence of numbers where each number is the sum of the two preceding ones, typically starting with 0 and 1. Here's an example of how to generate a Fibonacci series using a `while` loop:

```c
#include <stdio.h>

int main() {
    int n, first = 0, second = 1, next, i = 2;

    printf("Enter the number of terms for the Fibonacci series: ");
    scanf("%d", &n);

    printf("Fibonacci Series: %d, %d, ", first, second);

    while (i < n) {
        next = first + second;
        printf("%d, ", next);
        first = second;
        second = next;
        i++;
    }

    printf("\n");

    return 0;
}
```

In this program:

1. The user is prompted to enter the number of terms (`n`) they want in the Fibonacci series.

2. The `first` and `second` variables are initialized to 0 and 1, which are the first two numbers in the Fibonacci sequence.

3. The program prints the initial values of `first` and `second`.

4. The `while` loop is used to generate the remaining terms in the series. It runs until `i` reaches `n`, where `i` is the index of the current term.

5. Inside the loop, the `next` variable is calculated as the sum of `first` and `second`, and it's printed as the next term in the series.

6. The values of `first` and `second` are updated to prepare for the next iteration.

7. The loop continues until `i` reaches `n`, at which point the program exits the loop.

This program will generate and print the Fibonacci series up to the specified number of terms (`n`).
