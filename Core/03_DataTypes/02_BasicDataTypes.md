# Primitive or Basic Data Types in C
In C, there are several basic data types that are used to declare variables. These data types represent fundamental types of data. Here are the basic data types in C:

1. **int**: Used to store integer values. It can hold both positive and negative whole numbers.
    
    1.1 Represents integer values, both positive and negative.
   
    1.2 Typically, it's 4 bytes in size on most systems, but this can vary depending on the compiler and system architecture

   Example:
   ```c
   int age = 25;
   ```

2. **float**: Used to store single-precision floating-point numbers, which are numbers with a decimal point.

    2.1 Represents single-precision floating-point numbers.
   
    2.2 Typically, it's 4 bytes in size and provides limited decimal precision.

   Example:
   ```c
   float temperature = 98.6;
   ```

3. **double**: Used to store double-precision floating-point numbers, which have higher precision and can represent larger numbers or more precise decimal values than float.

   3.1  Represents double-precision floating-point numbers.

   3.2  Typically, it's 8 bytes in size and provides higher decimal precision than float.

   Example:
   ```c
   double pi = 3.14159265359;
   ```

5. **char**: Used to store a single character. Characters are enclosed in single quotes.

   Example:
   ```c
   char grade = 'A';
   ```

6. **_Bool**: Used to store Boolean values, which can be either true (1) or false (0).

   Example:
   ```c
   _Bool isStudent = 1;  // true
   ```

7. **void**: Typically used as a return type for functions that do not return a value.

   Example:
   ```c
   void printMessage() {
       printf("Hello, World!\n");
   }
   ```

These basic data types are the building blocks for defining variables in C, and they are used to represent different types of data within your programs. Depending on the specific needs of your application, you'll choose the appropriate data type to work with your data effectively.
