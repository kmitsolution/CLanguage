Here are some examples of working with matrices (two-dimensional arrays) in C:

**1. Initializing and Printing a Matrix:**

```c
#include <stdio.h>

int main() {
    int matrix[3][3]; // Declare a 3x3 integer matrix

    // Initialize the matrix elements
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            matrix[i][j] = i * 3 + j + 1;
        }
    }

    // Print the matrix elements
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

This program declares a 3x3 integer matrix, initializes its elements, and then prints the matrix.

**2. Matrix Addition:**

```c
#include <stdio.h>

int main() {
    int matrix1[2][2] = {{1, 2}, {3, 4}};
    int matrix2[2][2] = {{5, 6}, {7, 8}};
    int result[2][2];

    // Perform matrix addition
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            result[i][j] = matrix1[i][j] + matrix2[i][j];
        }
    }

    // Print the result matrix
    printf("Result of matrix addition:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            printf("%d\t", result[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

This program performs matrix addition on two 2x2 matrices and prints the result.

**3. Matrix Multiplication:**

```c
#include <stdio.h>

int main() {
    int matrix1[2][3] = {{1, 2, 3}, {4, 5, 6}};
    int matrix2[3][2] = {{7, 8}, {9, 10}, {11, 12}};
    int result[2][2];

    // Perform matrix multiplication
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            result[i][j] = 0;
            for (int k = 0; k < 3; k++) {
                result[i][j] += matrix1[i][k] * matrix2[k][j];
            }
        }
    }

    // Print the result matrix
    printf("Result of matrix multiplication:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            printf("%d\t", result[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

This program performs matrix multiplication on a 2x3 matrix and a 3x2 matrix and prints the result.

**4. Transposing a Matrix:**

```c
#include <stdio.h>

int main() {
    int original[3][2] = {{1, 2}, {3, 4}, {5, 6}};
    int transposed[2][3];

    // Perform matrix transpose
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 2; j++) {
            transposed[j][i] = original[i][j];
        }
    }

    // Print the transposed matrix
    printf("Transposed matrix:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d\t", transposed[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

This program transposes a 3x2 matrix and prints the transposed matrix.

These examples demonstrate various operations you can perform on matrices (two-dimensional arrays) in C, including initialization, addition, multiplication, and transposition. Matrices are essential for many mathematical and scientific computations.
