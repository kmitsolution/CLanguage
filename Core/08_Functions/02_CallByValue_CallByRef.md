In C, function arguments can be passed to functions using two different mechanisms: call by value (also known as pass by value) and call by reference (also known as pass by reference). These mechanisms determine how changes to function parameters affect the original values outside the function. Let's explore both concepts:

**Call by Value (Pass by Value):**

In call by value, a copy of the argument's value is passed to the function. This means that any changes made to the parameter within the function do not affect the original variable in the calling function. Call by value is the default mechanism for passing arguments to functions in C.

Here's an example of call by value:

```c
#include <stdio.h>

void modifyValue(int x) {
    x = x + 10;
}

int main() {
    int num = 5;
    
    // Call by value
    modifyValue(num);
    
    printf("Original value: %d\n", num); // Output: Original value: 5
    
    return 0;
}
```

In the example above, the `modifyValue` function receives a copy of the `num` variable. Any changes made to `x` within the function do not affect the original `num` variable outside the function.

**Call by Reference (Pass by Reference):**

In C, call by reference is achieved by passing the address (pointer) of the argument to the function. This allows the function to directly modify the original variable in the calling function. To implement call by reference, you need to use pointers.

Here's an example of call by reference:

```c
#include <stdio.h>

void modifyValue(int *x) {
    *x = *x + 10;
}

int main() {
    int num = 5;
    
    // Call by reference
    modifyValue(&num);
    
    printf("Modified value: %d\n", num); // Output: Modified value: 15
    
    return 0;
}
```

In this example, we pass the address of the `num` variable to the `modifyValue` function using a pointer (`&num`). The function modifies the value stored at that address directly, so when we print `num` in the `main` function after the function call, it reflects the change made within `modifyValue`.

To summarize, call by value involves passing a copy of the argument's value to a function, while call by reference involves passing a pointer to the argument, allowing the function to directly modify the original variable. In C, call by value is the default mechanism, but you can achieve call by reference by using pointers.
