Certainly! Here are some more examples of recursive functions in C:

**1. Fibonacci Sequence:**
```c
#include <stdio.h>

// Recursive function to compute the nth Fibonacci number
int fibonacci(int n) {
    if (n <= 1) {
        return n; // Base cases: Fibonacci(0) = 0, Fibonacci(1) = 1
    } else {
        return fibonacci(n - 1) + fibonacci(n - 2); // Recursive case
    }
}

int main() {
    int n = 10;
    
    // Calculate and print the first n Fibonacci numbers
    for (int i = 0; i < n; i++) {
        printf("%d ", fibonacci(i));
    }
    
    return 0;
}
```

This program calculates and prints the first `n` Fibonacci numbers using a recursive function.

**2. Binary Search:**
```c
#include <stdio.h>

// Recursive binary search function to find an element in a sorted array
int binarySearch(int arr[], int left, int right, int target) {
    if (left <= right) {
        int mid = left + (right - left) / 2; // Calculate the middle index

        if (arr[mid] == target) {
            return mid; // Element found
        } else if (arr[mid] < target) {
            return binarySearch(arr, mid + 1, right, target); // Search the right half
        } else {
            return binarySearch(arr, left, mid - 1, target); // Search the left half
        }
    }
    
    return -1; // Element not found
}

int main() {
    int arr[] = {2, 4, 7, 10, 15, 20};
    int n = sizeof(arr) / sizeof(arr[0]);
    int target = 10;
    
    int index = binarySearch(arr, 0, n - 1, target);
    
    if (index != -1) {
        printf("Element %d found at index %d\n", target, index);
    } else {
        printf("Element %d not found\n", target);
    }
    
    return 0;
}
```

This program uses a recursive binary search algorithm to find an element in a sorted array.

**3. Tower of Hanoi:**
```c
#include <stdio.h>

// Recursive function to solve the Tower of Hanoi puzzle
void towerOfHanoi(int n, char source, char auxiliary, char destination) {
    if (n == 1) {
        printf("Move disk 1 from %c to %c\n", source, destination);
        return;
    }

    towerOfHanoi(n - 1, source, destination, auxiliary);
    printf("Move disk %d from %c to %c\n", n, source, destination);
    towerOfHanoi(n - 1, auxiliary, source, destination);
}

int main() {
    int n = 3; // Number of disks

    towerOfHanoi(n, 'A', 'B', 'C');

    return 0;
}
```

This program uses a recursive function to solve the Tower of Hanoi puzzle for `n` disks.

These examples demonstrate the versatility of recursion in solving various types of problems, from calculating Fibonacci numbers to performing binary searches and solving complex puzzles like the Tower of Hanoi. Recursion is a powerful technique that simplifies problem-solving by breaking down complex problems into smaller, more manageable subproblems.
