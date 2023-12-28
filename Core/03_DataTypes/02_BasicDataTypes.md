# Primitive or Basic Data Types in C
In C, there are several basic data types that are used to declare variables. These data types represent fundamental types of data. Here are the basic data types in C:

## 1. Integer data types

In C, the standard integer data types, including `short`, `long`, and specific bit-width types like `int32_t` and `int64_t`, are used to represent different ranges of integer values. Here's an overview of these common integer data types:

a. **`short(2 Byte Size)`**:
   - The `short` data type is used to represent integers with a relatively small range of values. It typically uses 16 bits (2 bytes) of memory, but its size may vary depending on the platform.
   - The range of values that can be stored in a `short` variable is implementation-dependent, but it is often from -32,768 to 32,767 in a two's complement representation.

   ```c
   short myShort = 32767;
   ```

b. **`long or int(4 Byte Size) `**:
   - The `long` data type is used to represent integers with a larger range compared to `int`. It typically uses 32 bits (4 bytes) of memory, but its size may vary depending on the platform.
   - The range of values that can be stored in a `long` variable is implementation-dependent, but it is often from approximately -2.1 billion to 2.1 billion in a two's complement representation.

   ```c
   long myLong = 2147483647;
   ```

c. **`int32_t`** (from `<stdint.h>`):
   - The `int32_t` data type is defined in the `<stdint.h>` header and is designed to provide a 32-bit signed integer with a well-defined range.
   - `int32_t` uses exactly 32 bits (4 bytes) of memory, and its range is from -2,147,483,648 to 2,147,483,647 in a two's complement representation.

   ```c
   #include <stdint.h>

   int32_t myInt32 = 2147483647;
   ```

d. **`int64_t`** (from `<stdint.h>`):
   - The `int64_t` data type is also defined in the `<stdint.h>` header and provides a 64-bit signed integer with a well-defined range.
   - `int64_t` uses exactly 64 bits (8 bytes) of memory, and its range is from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 in a two's complement representation.

   ```c
   #include <stdint.h>

   int64_t myInt64 = 9223372036854775807LL;
   ```

Using the fixed-width integer types like `int32_t` and `int64_t` from `<stdint.h>` is recommended when you need precise control over the size and range of your integer variables. These types ensure portability across different systems and compilers, as their sizes are defined in terms of a specific number of bits rather than relying on the platform's default sizes.


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

4. **char**: Used to store a single character. Characters are enclosed in single quotes.
   In C, a character variable holds the character's ASCII value (instead of the character itself). For instance, “A” has the ASCII value of 65. What this means is 
     that, if you assign 'A' to a character variable, 65 is stored in the variable rather than 'A' itself.
   ```
   AScii Value of 'A-Z' = 65-90
   AScii Value of 'a-z' = 97-122
   AScii Value of '0-9' = 48-57
```
   Example:
   ```c
   char grade = 'A';
   ```


6. **void**: Typically used as a return type for functions that do not return a value.

   Example:
   ```c
   void printMessage() {
       printf("Hello, World!\n");
   }
   ```

These basic data types are the building blocks for defining variables in C, and they are used to represent different types of data within your programs. Depending on the specific needs of your application, you'll choose the appropriate data type to work with your data effectively.
