In C, loops are used to execute a block of code repeatedly. C provides three main types of loops: `for`, `while`, and `do-while`. Here's an overview of each loop type:

1. **For Loop:**
   - The `for` loop is used when you know the number of iterations in advance.
   - It consists of three parts: initialization, condition, and iteration.
   
   ```c
   for (initialization; condition; iteration) {
       // Code to be executed in each iteration
   }
   ```
   
   Example:

   ```c
   #include <stdio.h>

   int main() {
       for (int i = 0; i < 5; i++) {
           printf("Iteration %d\n", i);
       }
       return 0;
   }
   ```

2. **While Loop:**
   - The `while` loop is used when you want to repeat a block of code as long as a certain condition is true.
   
   ```c
   while (condition) {
       // Code to be executed while the condition is true
   }
   ```

   Example:

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

3. **Do-While Loop:**
   - The `do-while` loop is similar to a `while` loop, but it ensures that the block of code is executed at least once before checking the condition.
   
   ```c
   do {
       // Code to be executed
   } while (condition);
   ```

   Example:

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

4. **Loop Control Statements:**
   - In addition to the basic loop structures, C provides loop control statements like `break` and `continue` that allow you to modify the flow of loops.
   - `break` is used to exit a loop prematurely.
   - `continue` is used to skip the current iteration of a loop and move to the next iteration.

Loops are fundamental for creating repetitive tasks, iterating over arrays, and implementing various algorithms in C programs. They allow you to efficiently perform tasks that require repeating a specific action multiple times.
