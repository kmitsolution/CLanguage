Here are some examples of arrays in C with explanations:

**1. Initializing and Printing an Array:**

```c
#include <stdio.h>

int main() {
    int numbers[5]; // Declare an integer array with 5 elements

    // Initialize the array elements
    numbers[0] = 10;
    numbers[1] = 20;
    numbers[2] = 30;
    numbers[3] = 40;
    numbers[4] = 50;

    // Print the array elements
    for (int i = 0; i < 5; i++) {
        printf("numbers[%d] = %d\n", i, numbers[i]);
    }

    return 0;
}
```

This program declares an integer array named `numbers` with 5 elements, initializes the elements, and then prints them using a loop.

**2. Finding the Sum of Array Elements:**

```c
#include <stdio.h>

int main() {
    int numbers[] = {1, 2, 3, 4, 5}; // Declare and initialize an integer array

    int sum = 0;

    // Calculate the sum of array elements
    for (int i = 0; i < 5; i++) {
        sum += numbers[i];
    }

    printf("Sum of array elements: %d\n", sum);

    return 0;
}
```

This program calculates and prints the sum of the elements in an integer array.

**3. Finding the Maximum Element in an Array:**

```c
#include <stdio.h>

int main() {
    int numbers[] = {12, 45, 67, 23, 9, 54}; // Declare and initialize an integer array

    int max = numbers[0];

    // Find the maximum element in the array
    for (int i = 1; i < 6; i++) {
        if (numbers[i] > max) {
            max = numbers[i];
        }
    }

    printf("Maximum element in the array: %d\n", max);

    return 0;
}
```

This program finds and prints the maximum element in an integer array.

**4. Reversing an Array:**

```c
#include <stdio.h>

int main() {
    int numbers[] = {1, 2, 3, 4, 5}; // Declare and initialize an integer array
    int size = 5;
    int temp;

    // Reverse the array
    for (int i = 0; i < size / 2; i++) {
        temp = numbers[i];
        numbers[i] = numbers[size - 1 - i];
        numbers[size - 1 - i] = temp;
    }

    // Print the reversed array
    for (int i = 0; i < size; i++) {
        printf("numbers[%d] = %d\n", i, numbers[i]);
    }

    return 0;
}
```

This program reverses an integer array and then prints the reversed array.

**5. Searching for an Element in an Array:**

```c
#include <stdio.h>

int main() {
    int numbers[] = {12, 45, 67, 23, 9, 54}; // Declare and initialize an integer array
    int target = 23;
    int found = 0;

    // Search for the target element in the array
    for (int i = 0; i < 6; i++) {
        if (numbers[i] == target) {
            found = 1;
            break;
        }
    }

    if (found) {
        printf("Element %d found in the array.\n", target);
    } else {
        printf("Element %d not found in the array.\n", target);
    }

    return 0;
}
```

This program searches for a target element in an integer array and prints whether it was found or not.

These examples illustrate various operations you can perform on arrays in C, including initialization, element access, finding the sum and maximum element, reversing the array, and searching for specific elements. Arrays are fundamental data structures in C and are widely used for storing and manipulating collections of data.
