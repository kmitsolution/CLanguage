Conditional statements in the C programming language allow you to make decisions in your code by executing different blocks of code based on whether certain conditions are true or false. The primary conditional statements in C are the `if`, `else if`, `else`, and the `switch` statements.

1. **if Statement:**
   - The `if` statement is used to execute a block of code if a given condition is true.
   
   ```c
   #include <stdio.h>

   int main() {
       int x = 10;

       if (x > 5) {
           printf("x is greater than 5.\n");
       }

       return 0;
   }
   ```

2. **else if Statement:**
   - The `else if` statement is used in conjunction with `if` to test additional conditions if the first `if` condition is false.
   
   ```c
   #include <stdio.h>

   int main() {
       int x = 3;

       if (x > 5) {
           printf("x is greater than 5.\n");
       } else if (x < 5) {
           printf("x is less than 5.\n");
       }

       return 0;
   }
   ```

3. **else Statement:**
   - The `else` statement is used with `if` to specify a block of code to execute when the `if` condition is false.
   
   ```c
   #include <stdio.h>

   int main() {
       int x = 7;

       if (x > 10) {
           printf("x is greater than 10.\n");
       } else {
           printf("x is not greater than 10.\n");
       }

       return 0;
   }
   ```


These conditional statements allow you to control the flow of your program based on various conditions and make your programs more flexible and responsive.
