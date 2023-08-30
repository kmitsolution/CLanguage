In C programming, input and output operations are crucial for interacting with users and handling data. The `stdio.h` library provides functions for input and output operations. Here are some of the most commonly used input/output functions in C:

**Output Functions:**

1. `printf`: Used to print formatted output to the console.
   ```c
   printf("Hello, World!\n");
   ```

2. `puts`: Prints a string to the console followed by a newline character.
   ```c
   puts("Hello, World!");
   ```

3. `putchar`: Prints a single character to the console.
   ```c
   char ch = 'A';
   putchar(ch);
   ```

**Input Functions:**

1. `scanf`: Used to read formatted input from the console.
   ```c
   int num;
   scanf("%d", &num);
   ```

2. `gets` (deprecated): Reads a line of text from the console.
   ```c
   char buffer[100];
   gets(buffer);
   ```

3. `fgets`: Reads a line of text from the console along with the newline character.
   ```c
   char buffer[100];
   fgets(buffer, sizeof(buffer), stdin);
   ```

4. `getchar`: Reads a single character from the console.
   ```c
   char ch;
   ch = getchar();
   ```

Remember that some input functions, like `gets`, are considered unsafe because they can lead to buffer overflow vulnerabilities. It's recommended to use safer alternatives like `fgets` instead.

**Formatted Output:**

You can use formatting codes to control the appearance of output when using `printf`:
- `%d` or `%i`: Integer
- `%f`: Float or double
- `%c`: Character
- `%s`: String
- `%p`: Pointer address
- `%x` or `%X`: Hexadecimal
- `%o`: Octal
- `%u`: Unsigned integer
- `%e` or `%E`: Exponential notation
- `%g` or `%G`: Shortest of `%f` or `%e`
- `%%`: Prints a literal `%` character

For example:
```c
int age = 25;
printf("My age is %d\n", age);
```

These are just some of the basics of input and output in C. More advanced functionality, like file I/O, is also available through the `stdio.h` library.
