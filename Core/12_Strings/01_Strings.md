# Strings in C
In C, strings are represented as arrays of characters (`char`). Strings are used to store sequences of characters, such as words, sentences, or any text data. Unlike some programming languages that have built-in string types, C treats strings as character arrays with a null-terminated character (`'\0'`) to mark the end of the string. Here are some key aspects of working with strings in C:

**1. Declaring and Initializing Strings:**

Strings can be declared and initialized in various ways:

```c
char str1[] = "Hello, World!"; // Initialize with a string literal
char str2[20];                // Declare an array and later initialize it
str2[0] = 'H';                // Assign individual characters
str2[1] = 'i';
str2[2] = '\0';               // Null-terminate the string

char str3[10] = {'H', 'e', 'l', 'l', 'o', '\0'}; // Initialize with an array of characters
```

**2. String Input and Output:**

You can use the standard I/O functions like `printf` and `scanf` to display and input strings:

```c
char name[50];
printf("Enter your name: ");
scanf("%s", name); // Read a string from the user
printf("Hello, %s!\n", name); // Display the string
```

**3. String Functions:**

C provides a set of standard library functions for working with strings in the `<string.h>` header. Here are some commonly used string functions:

- `strlen`: Calculates the length of a string.
- `strcpy`: Copies one string to another.
- `strcat`: Concatenates two strings.
- `strcmp`: Compares two strings.
- `strchr`: Searches for a character in a string.
- `strstr`: Searches for a substring in a string.

For example:

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str1[] = "Hello";
    char str2[] = "World";
    
    // Concatenate str2 to str1
    strcat(str1, " ");
    strcat(str1, str2);
    
    printf("Concatenated string: %s\n", str1);
    
    return 0;
}
```

**4. Character Array vs. String:**

In C, a character array can be treated as a string by ensuring it is null-terminated. However, you should be cautious when manipulating character arrays to ensure they are properly null-terminated to avoid undefined behavior.

**5. String Literals:**

String literals are sequences of characters enclosed in double quotes. They are automatically null-terminated by the compiler. For example:

```c
char *greeting = "Hello"; // 'greeting' is a pointer to a string literal
```

**6. String Manipulation:**

Manipulating strings often involves using loops to iterate through characters, copying, concatenating, or modifying the characters within the array.

Here is a simple example to reverse a string:

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str[] = "Hello";
    int length = strlen(str);
    
    for (int i = 0; i < length / 2; i++) {
        char temp = str[i];
        str[i] = str[length - 1 - i];
        str[length - 1 - i] = temp;
    }
    
    printf("Reversed string: %s\n", str);
    
    return 0;
}
```

These are some fundamental concepts and operations related to strings in C. String manipulation in C often involves working directly with character arrays and using the standard library functions to simplify common tasks.
