Control flow instructions in the C programming language are used to determine the order in which statements are executed in a program. These instructions allow you to make decisions, repeat certain actions, and create more complex program structures. Here are some of the most common control flow instructions in C:

1. **Conditional Statements:**
   - **if Statement:** It allows you to execute a block of code if a certain condition is true.
     ```c
     if (condition) {
         // Code to execute if condition is true
     }
     ```
   ### Example
   ```c
   #include <stdio.h>

    int main() {
      int number = 10;

      // Check if 'number' is greater than 5
      if (number > 5) {
        printf("The number is greater than 5.\n");
    }

    return 0;
    }

   ```

   - **else Statement:** Used in conjunction with `if` to specify a block of code to execute if the condition is false.
     ```c
     if (condition) {
         // Code to execute if condition is true
     } else {
         // Code to execute if condition is false
     }
     ```
### Example
  ```c
  #include <stdio.h>

    int main() {
        int number = 10;
    
        // Check if 'number' is greater than 5
        if (number > 5) {
            printf("The number is greater than 5.\n");
        }
        else
           printf("The number is lessthan equal to 5.\n");
    
        return 0;
    }

  ```
### Example
```c
#include <stdio.h>
int main() {

  int n;
  printf("\nEnter a number");
  scanf("%d",&n);
  if(n>=10){
    printf("Number is >=10");
  }
  else
    printf("\nNumber is <10");
    return 0;
}

```
   - **else if Statement:** Allows you to test multiple conditions in sequence.
     ```c
     if (condition1) {
         // Code to execute if condition1 is true
     } else if (condition2) {
         // Code to execute if condition2 is true
     } else {
         // Code to execute if neither condition1 nor condition2 is true
     }
     ```
  ### Example
  ```c
    #include <stdio.h>
    
    int main() {
        int number = 7;
    
        // Check if 'number' is greater than 10
        if (number > 10) {
            printf("The number is greater than 10.\n");
        }
        // Check else if 'number' is less than 10
        else if (number < 10) {
            printf("The number is less than 10.\n");
        }
        // If neither of the above conditions is true
        else {
            printf("The number is exactly 10.\n");
        }
    
        return 0;
    }

  ```
### Example
```c


#include <stdio.h>
int main() {

  int marks;
  printf("\nEnter the marks of student");
  scanf("%d",&marks);
  if(marks>=90)
    printf("\n Your Grade is A");
  else if(marks>=80)  
    printf("\n Your Grade is B");
  else if(marks>=70)  
    printf("\n Your Grade is C");
  else
    printf("\n Your Grade is D")  ;
    return 0;
}
```
3. **Switch Statement:** Used to select one of many code blocks to be executed based on the value of an expression.
   ```c
   switch (expression) {
       case value1:
           // Code to execute if expression equals value1
           break;
       case value2:
           // Code to execute if expression equals value2
           break;
       // ...
       default:
           // Code to execute if expression doesn't match any case
   }
   ```

### Example
```c
#include <stdio.h>

int main() {
    char grade = 'B';

    switch (grade) {
        case 'A':
            printf("Excellent!\n");
            break;
        case 'B':
            printf("Good job!\n");
            break;
        case 'C':
            printf("You passed.\n");
            break;
        case 'D':
            printf("You need to improve.\n");
            break;
        case 'F':
            printf("You failed.\n");
            break;
        default:
            printf("Invalid grade.\n");
    }

    return 0;
}

```
