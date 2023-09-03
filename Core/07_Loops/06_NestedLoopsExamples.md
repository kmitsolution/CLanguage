# Nested Loop Examples in C

### Example 1: Printing a Right-Angled Triangle of Numbers

This program uses nested loops to print a right-angled triangle of numbers:

```c
#include <stdio.h>

int main() {
    int rows;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= i; j++) {
            printf("%d ", j);
        }
        printf("\n");
    }

    return 0;
}
```

### Example 2: Printing a Pyramid Pattern of Stars

This program uses nested loops to print a pyramid pattern of stars:

```c
#include <stdio.h>

int main() {
    int rows;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= rows - i; j++) {
            printf(" ");
        }
        for (int k = 1; k <= 2 * i - 1; k++) {
            printf("*");
        }
        printf("\n");
    }

    return 0;
}
```

### Example 3: Multiplication Table

This program uses nested loops to print a multiplication table:

```c
#include <stdio.h>

int main() {
    int rows, cols;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);
    printf("Enter the number of columns: ");
    scanf("%d", &cols);

    for (int i = 1; i <= rows; i++) {
        for (int j = 1; j <= cols; j++) {
            printf("%3d ", i * j);
        }
        printf("\n");
    }

    return 0;
}
```

### Example 4: Printing a Diamond Pattern of Numbers

This program uses nested loops to print a diamond pattern of numbers:

```c
#include <stdio.h>

int main() {
    int n;

    printf("Enter the number of rows: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= n - i; j++) {
            printf(" ");
        }
        for (int k = 1; k <= 2 * i - 1; k++) {
            printf("%d", k);
        }
        printf("\n");
    }

    for (int i = n - 1; i >= 1; i--) {
        for (int j = 1; j <= n - i; j++) {
            printf(" ");
        }
        for (int k = 1; k <= 2 * i - 1; k++) {
            printf("%d", k);
        }
        printf("\n");
    }

    return 0;
}
```

These examples showcase more advanced patterns and use cases of nested loops in C. They demonstrate how nested loops can be used to create intricate patterns and solve various programming problems.
