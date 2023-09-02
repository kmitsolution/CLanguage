# Examples of for loop in C
### Calculates and prints prime numbers within a specified range:

```c
#include <stdio.h>

int main() {
    int start, end;

    printf("Enter the starting and ending numbers: ");
    scanf("%d %d", &start, &end);

    printf("Prime numbers between %d and %d are:\n", start, end);

    for (int num = start; num <= end; num++) {
        int isPrime = 1; // Assume num is prime initially

        if (num <= 1) {
            isPrime = 0; // Numbers less than or equal to 1 are not prime
        } else {
            for (int i = 2; i * i <= num; i++) {
                if (num % i == 0) {
                    isPrime = 0; // If num is divisible by any number, it's not prime
                    break;
                }
            }
        }

        if (isPrime) {
            printf("%d\n", num);
        }
    }

    return 0;
}
```

In this program:

1. The user is prompted to enter a starting and ending number to find prime numbers within a range.

2. The program iterates through the numbers from `start` to `end` using a `for` loop.

3. For each number `num`, it checks if it's prime or not. It initially assumes the number is prime (`isPrime = 1`).

4. If `num` is less than or equal to 1, it's not considered prime, so `isPrime` is set to 0.

5. For numbers greater than 1, it checks for divisors by iterating from 2 to the square root of `num`. If `num` is divisible by any number in this range, `isPrime` is set to 0, and the loop breaks.

6. If `isPrime` is still 1 after the loop, it means `num` is a prime number, and it is printed.

This program efficiently finds and displays prime numbers within the specified range using a `for` loop and nested conditional statements.

### Calculate the factorial of a number using a `for` loop in C. The factorial of a non-negative integer `n`, denoted as `n!`, is the product of all positive integers from 1 to `n`. Here's an example of how to calculate the factorial of a number using a `for` loop:

```c
#include <stdio.h>

int main() {
    int num;
    long long factorial = 1;

    // Prompt the user to enter a non-negative integer
    printf("Enter a non-negative integer: ");
    scanf("%d", &num);

    if (num < 0) {
        printf("Factorial is not defined for negative numbers.\n");
    } else {
        // Calculate the factorial using a for loop
        for (int i = 1; i <= num; i++) {
            factorial *= i;
        }

        // Display the result
        printf("Factorial of %d = %d\n", num, factorial);
    }

    return 0;
}
```

In this program:

1. The user is prompted to enter a non-negative integer.

2. If the entered number is negative, the program displays an error message because factorial is not defined for negative numbers.

3. If the entered number is non-negative, a `for` loop is used to calculate the factorial. The loop iterates from 1 to `num`, multiplying `factorial` by each integer in the range.

4. After the loop completes, the program displays the factorial of the entered number.

This program calculates and displays the factorial of a non-negative integer using a `for` loop.
