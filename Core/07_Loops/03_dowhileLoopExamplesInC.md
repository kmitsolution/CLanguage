# do-while loop examples

### Example 1. Simple guessing game where the user needs to guess a randomly generated number:

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int number, guess, attempts = 0;
    
    // Seed the random number generator
    srand(time(NULL));
    
    // Generate a random number between 1 and 100
    number = rand() % 100 + 1;

    printf("Welcome to the Guessing Game!\n");

    do {
        // Prompt the user for a guess
        printf("Guess the number (between 1 and 100): ");
        scanf("%d", &guess);

        attempts++; // Increase the number of attempts

        // Check if the guess is correct, too high, or too low
        if (guess == number) {
            printf("Congratulations! You guessed the number %d in %d attempts.\n", number, attempts);
        } else if (guess < number) {
            printf("Try higher.\n");
        } else {
            printf("Try lower.\n");
        }
    } while (guess != number);

    return 0;
}
```

In this program:

1. The program generates a random number between 1 and 100 using `rand()` and seeds the random number generator with the current time using `srand(time(NULL))`.

2. It initiates a `do-while` loop that continues until the user correctly guesses the random number.

3. Inside the loop, the user is prompted to enter a guess.

4. The program checks if the guess is correct, too high, or too low and provides appropriate feedback.

5. The `attempts` variable keeps track of the number of attempts the user has made.

6. When the user correctly guesses the number, the loop exits, and the program displays a congratulatory message along with the number of attempts it took to guess correctly.

This example demonstrates how to use a `do-while` loop to create an interactive guessing game. The loop ensures that the game continues until the user successfully guesses the random number.

Certainly! Here are a few more advanced examples of `do-while` loops in C:

### Example 2: Calculating the Factorial of a Number

In this example, we use a `do-while` loop to calculate the factorial of a positive integer entered by the user.

```c
#include <stdio.h>

int main() {
    int num;
    long long factorial = 1;

    do {
        printf("Enter a positive integer: ");
        scanf("%d", &num);
        
        if (num < 0) {
            printf("Please enter a positive integer.\n");
        }
    } while (num < 0);

    int i = 1;
    do {
        factorial *= i;
        i++;
    } while (i <= num);

    printf("Factorial of %d = %lld\n", num, factorial);

    return 0;
}
```

### Example 3: Handling User Menu Selection

This example simulates a menu-driven program using a `do-while` loop to repeatedly display a menu until the user decides to exit.

```c
#include <stdio.h>

int main() {
    char choice;

    do {
        printf("Main Menu:\n");
        printf("1. Option 1\n");
        printf("2. Option 2\n");
        printf("3. Quit\n");
        printf("Enter your choice: ");
        scanf(" %c", &choice);

        switch (choice) {
            case '1':
                printf("You selected Option 1.\n");
                break;
            case '2':
                printf("You selected Option 2.\n");
                break;
            case '3':
                printf("Exiting the program.\n");
                break;
            default:
                printf("Invalid choice. Please try again.\n");
        }
    } while (choice != '3');

    return 0;
}
```

### Example 4: Password Validation

In this example, a `do-while` loop is used to repeatedly prompt the user for a password until they enter the correct one.

```c
#include <stdio.h>
#include <string.h>

int main() {
    char password[] = "secret123";
    char input[20];
    int attempts = 0;

    do {
        printf("Enter the password: ");
        scanf("%s", input);
        attempts++;

        if (strcmp(input, password) == 0) {
            printf("Access granted after %d attempts.\n", attempts);
            break;
        } else {
            printf("Access denied. Please try again.\n");
        }
    } while (attempts < 3);

    if (attempts >= 3) {
        printf("Maximum login attempts reached. Account locked.\n");
    }

    return 0;
}
```

These examples illustrate how `do-while` loops can be used in various situations, including input validation, menu-driven programs, and iterative calculations, to create more interactive and robust programs.
