Examples using `if`, `else if`, and `else` statements in C to handle various scenarios:

### Example 1: Determine the Largest of Three Numbers
This program determines the largest of three numbers entered by the user:

```c
#include <stdio.h>

int main() {
    int num1, num2, num3;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &num1, &num2, &num3);

    if (num1 >= num2 && num1 >= num3) {
        printf("%d is the largest number.\n", num1);
    } else if (num2 >= num1 && num2 >= num3) {
        printf("%d is the largest number.\n", num2);
    } else {
        printf("%d is the largest number.\n", num3);
    }

    return 0;
}
```

### Example 2: Check if a Year is Leap Year
This program checks if a given year is a leap year or not:

```c
#include <stdio.h>

int main() {
    int year;

    printf("Enter a year: ");
    scanf("%d", &year);

    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
        printf("%d is a leap year.\n", year);
    } else {
        printf("%d is not a leap year.\n", year);
    }

    return 0;
}
```

### Example 3: Determine the Quadrant of a Point
This program determines the quadrant in which a point lies in a Cartesian coordinate system:

```c
#include <stdio.h>

int main() {
    int x, y;

    printf("Enter the coordinates (x, y): ");
    scanf("%d %d", &x, &y);

    if (x > 0 && y > 0) {
        printf("The point is in Quadrant I.\n");
    } else if (x < 0 && y > 0) {
        printf("The point is in Quadrant II.\n");
    } else if (x < 0 && y < 0) {
        printf("The point is in Quadrant III.\n");
    } else if (x > 0 && y < 0) {
        printf("The point is in Quadrant IV.\n");
    } else {
        printf("The point is at the origin.\n");
    }

    return 0;
}
```

These examples showcase how `if`, `else if`, and `else` statements can be used to make decisions and perform different actions based on various conditions.
