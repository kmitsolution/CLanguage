In the C programming language, operators are symbols that represent computations or operations to be performed on data. C provides a wide range of operators that can be classified into the following categories:

1. **Arithmetic Operators**:
   - `+` (Addition)
   - `-` (Subtraction)
   - `*` (Multiplication)
   - `/` (Division)
   - `%` (Modulus, calculates the remainder of division)

   Example:
   ```c
   int result = 10 + 5;   // result is 15
   ```

2. **Relational Operators**:
   - `==` (Equal to)
   - `!=` (Not equal to)
   - `<` (Less than)
   - `>` (Greater than)
   - `<=` (Less than or equal to)
   - `>=` (Greater than or equal to)

   Example:
   ```c
   int a = 5, b = 10;
   if (a < b) {
       // This condition is true
   }
   ```

3. **Logical Operators**:
   - `&&` (Logical AND)
   - `||` (Logical OR)
   - `!` (Logical NOT)

   Example:
   ```c
   int x = 5, y = 10;
   if (x < 10 && y > 5) {
       // Both conditions are true
   }
   ```

4. **Assignment Operators**:
   - `=` (Assignment)
   - `+=` (Addition assignment)
   - `-=` (Subtraction assignment)
   - `*=` (Multiplication assignment)
   - `/=` (Division assignment)
   - `%=` (Modulus assignment)
   - `=` (Assignment)

   Example:
   ```c
   int a = 5;
   a += 2;  // Equivalent to a = a + 2; (a is now 7)
   ```

5. **Increment and Decrement Operators**:
   - `++` (Increment by 1)
   - `--` (Decrement by 1)

   Example:
   ```c
   int count = 0;
   count++;  // Increment count by 1
   ```

6. **Bitwise Operators**:
   - `&` (Bitwise AND)
   - `|` (Bitwise OR)
   - `^` (Bitwise XOR)
   - `~` (Bitwise NOT)
   - `<<` (Left shift)
   - `>>` (Right shift)

   Example:
   ```c
   int x = 5, y = 3;
   int result = x & y;  // Bitwise AND (result is 1)
   ```

7. **Conditional (Ternary) Operator**:
   - `? :` (Conditional operator)
   
   Example:
   ```c
   int a = 5, b = 10;
   int result = (a > b) ? a : b;  // result is 10
   ```

8. **Comma Operator**:
   - `,` (Comma operator, evaluates expressions from left to right and returns the result of the rightmost expression)

   Example:
   ```c
   int x = 5, y = 10;
   int z = (x++, y++);  // z is 10 (the result of the rightmost expression)
   ```

These are some of the fundamental operators in C. Operators allow you to perform various operations on variables and values, making C a versatile language for performing a wide range of computations.
