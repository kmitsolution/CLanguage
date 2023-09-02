# Loops Instructions in C
In the C programming language, you can use loops to execute a block of code repeatedly. C provides three main types of loops: `for`, `while`, and `do-while`. Here are examples of each type:

1. **For Loop:**
   - A `for` loop is used when you know the number of iterations in advance.

   ```c
   #include <stdio.h>

   int main() {
       for (int i = 0; i < 5; i++) {
           printf("Iteration %d\n", i);
       }
       return 0;
   }
   ```

   In this example, the `for` loop runs five times, as specified by `i < 5`, and it prints the message "Iteration 0" through "Iteration 4."

2. **While Loop:**
   - A `while` loop is used when you want to repeat a block of code as long as a certain condition is true.

   ```c
   #include <stdio.h>

   int main() {
       int count = 0;
       while (count < 5) {
           printf("Count: %d\n", count);
           count++;
       }
       return 0;
   }
   ```

   The `while` loop continues executing as long as `count` is less than 5, and it increments `count` with each iteration.

3. **Do-While Loop:**
   - A `do-while` loop is similar to a `while` loop, but it ensures that the block of code is executed at least once before checking the condition.

   ```c
   #include <stdio.h>

   int main() {
       int x = 5;
       do {
           printf("Value of x: %d\n", x);
           x--;
       } while (x > 0);
       return 0;
   }
   ```

   In this example, the code inside the loop is executed at least once because the condition `x > 0` is checked after the first iteration.

4. **Loop Control Statements:**
   - In addition to the basic loop structures, C also provides loop control statements like `break` and `continue` that allow you to modify the flow of loops.
   - `break` is used to exit a loop prematurely.
   - `continue` is used to skip the current iteration of a loop and move to the next iteration.

These loop constructs are essential for creating repetitive tasks and implementing various algorithms in C programs.
