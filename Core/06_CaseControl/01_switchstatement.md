# Case Control in C
The `switch` statement in C is used to select one of many code blocks to execute based on the value of an expression. It provides a way to simplify and optimize code when you have multiple conditions to check against a single variable. Here's the basic syntax of a `switch` statement:

```c
switch (expression) {
    case constant1:
        // Code to execute if expression equals constant1
        break;

    case constant2:
        // Code to execute if expression equals constant2
        break;

    // Additional cases...

    default:
        // Code to execute if expression doesn't match any case
}
```

- The `switch` keyword is followed by an expression inside the parentheses.
- Inside the `switch` block, you have one or more `case` labels, each followed by a constant value.
- When the `switch` statement is executed, it evaluates the expression and compares it to the constants in the `case` labels.
- If a match is found, the corresponding code block is executed. The `break` statement is used to exit the `switch` block after executing the code.
- If no match is found, the code in the `default` block is executed (optional).

Here's an example of a `switch` statement in C that determines the day of the week based on a user-input number:

```c
#include <stdio.h>

int main() {
    int day;

    printf("Enter a number (1-7): ");
    scanf("%d", &day);

    switch (day) {
        case 1:
            printf("Sunday\n");
            break;
        case 2:
            printf("Monday\n");
            break;
        case 3:
            printf("Tuesday\n");
            break;
        case 4:
            printf("Wednesday\n");
            break;
        case 5:
            printf("Thursday\n");
            break;
        case 6:
            printf("Friday\n");
            break;
        case 7:
            printf("Saturday\n");
            break;
        default:
            printf("Invalid input, please enter a number between 1 and 7.\n");
    }

    return 0;
}
```

In this example, the user enters a number between 1 and 7, and the `switch` statement determines the corresponding day of the week. If the input is not within the specified range, the `default` block is executed, providing an error message.
