In C, you can define your own data types using several mechanisms. Here are some ways to create user-defined data types:

1. **Structures (struct)**: Structures allow you to create custom data types by grouping together variables of different data types under a single name. Each variable inside the structure is referred to as a member.

   ```c
   struct Point {
       int x;
       int y;
   };
   ```

   Example usage:
   ```c
   struct Point p1;
   p1.x = 10;
   p1.y = 20;
   ```

2. **Unions**: Unions are similar to structures but use a single memory location for all their members. This means that a union can store only one of its members at any given time.

   ```c
   union Data {
       int i;
       float f;
   };
   ```

   Example usage:
   ```c
   union Data value;
   value.i = 42;
   ```

3. **Enumerations (enum)**: Enumerations define a set of named integer constants. They provide meaningful names to values, making the code more readable.

   ```c
   enum Days { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };
   ```

   Example usage:
   ```c
   enum Days today = Tuesday;
   ```

4. **Typedef**: Typedef allows you to create custom names for existing data types, which can improve code readability and maintainability.

   ```c
   typedef unsigned long long int ULLONG;
   ULLONG bigNumber = 123456789012345;
   ```

5. **Bit-fields**: Bit-fields allow you to define custom data types that use a specific number of bits for storage within a larger data type, such as an integer. This is often used for memory optimization.

   ```c
   struct Flags {
       unsigned int isSet : 1;
       unsigned int isEnabled : 1;
   };
   ```

   Example usage:
   ```c
   struct Flags myFlags;
   myFlags.isSet = 1;
   ```

6. **Custom Data Types**: You can create custom data types using combinations of the above techniques to suit your specific needs. For instance, you can use structures within structures, combine unions and structures, or use typedef with custom structures.

   ```c
   typedef struct {
       char name[50];
       int age;
   } Person;
   ```

   Example usage:
   ```c
   Person person1;
   strcpy(person1.name, "John");
   person1.age = 30;
   ```

User-defined data types in C provide flexibility and abstraction, allowing you to create complex and meaningful representations of data to suit the requirements of your programs.
