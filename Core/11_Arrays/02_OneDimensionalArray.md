# 1-D Array in C
A one-dimensional array in C is a collection of elements of the same data type, arranged in a linear sequence. Each element in the array is identified by its position or index, starting from 0. One-dimensional arrays are also commonly referred to as simply "arrays." Here's how you declare and work with a one-dimensional array in C:

**1. Declaration and Initialization:**
To declare a one-dimensional array, you specify the data type of its elements, followed by the array name and the size of the array in square brackets. You can also initialize the array at the time of declaration.

```c
data_type array_name[array_size];
```

For example:

```c
int numbers[5]; // Declares an integer array named 'numbers' with 5 elements
```

You can also initialize the array during declaration:

```c
int numbers[] = {1, 2, 3, 4, 5}; // Initializes an integer array with values
```

**2. Accessing Array Elements:**
You can access individual elements of a one-dimensional array using the array name followed by the index (position) of the element in square brackets. Array indices in C start from 0.

```c
int element = numbers[2]; // Accesses the third element (index 2) of the 'numbers' array
```

**3. Array Size:**
You can determine the size (number of elements) of an array using the `sizeof` operator.

```c
int size = sizeof(numbers) / sizeof(numbers[0]); // Calculates the size of the 'numbers' array
```

**4. Modifying Array Elements:**
You can change the value of an array element by assigning a new value to it using the assignment operator `=`.

```c
numbers[1] = 10; // Modifies the second element of the 'numbers' array
```

**5. Iterating Over an Array:**
You can use loops, such as `for` or `while`, to iterate over the elements of an array and perform operations on them.

```c
for (int i = 0; i < 5; i++) {
    printf("numbers[%d] = %d\n", i, numbers[i]);
}
```

**6. Array Functions:**
C provides functions and libraries for working with arrays, such as sorting, searching, and manipulating functions. For instance, you can use the `qsort` function from the `stdlib.h` library to sort an array.

```c
#include <stdio.h>
#include <stdlib.h>

int compare(const void *a, const void *b) {
    return (*(int *)a - *(int *)b);
}

int main() {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int size = sizeof(arr) / sizeof(arr[0]);

    qsort(arr, size, sizeof(int), compare);

    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

In this example, the `qsort` function is used to sort an integer array.

One-dimensional arrays are a fundamental data structure in C and are used to store and manipulate collections of data efficiently. Understanding how to declare, initialize, access, and manipulate one-dimensional arrays is essential for C programming.
