Certainly! Here are some examples of working with strings in C:

**1. Using `strlen` to Find String Length:**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str[] = "Hello, World!";
    int length = strlen(str);
    
    printf("The length of the string is: %d\n", length);
    
    return 0;
}
```

This program uses the `strlen` function to find the length of a string and then prints the result.

**2. Concatenating Strings using `strcat`:**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char greeting[20] = "Hello, ";
    char name[] = "Alice";
    
    strcat(greeting, name);
    
    printf("%s\n", greeting);
    
    return 0;
}
```

This program uses `strcat` to concatenate two strings and prints the result.

**3. Comparing Strings using `strcmp`:**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str1[] = "apple";
    char str2[] = "banana";
    
    int result = strcmp(str1, str2);
    
    if (result < 0) {
        printf("%s is less than %s\n", str1, str2);
    } else if (result > 0) {
        printf("%s is greater than %s\n", str1, str2);
    } else {
        printf("%s is equal to %s\n", str1, str2);
    }
    
    return 0;
}
```

This program uses `strcmp` to compare two strings and prints whether one is less than, greater than, or equal to the other.

**4. Searching for a Substring using `strstr`:**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char sentence[] = "The quick brown fox jumps over the lazy dog";
    char word[] = "fox";
    
    char *result = strstr(sentence, word);
    
    if (result != NULL) {
        printf("'%s' found at position %d\n", word, (int)(result - sentence));
    } else {
        printf("'%s' not found in the sentence.\n", word);
    }
    
    return 0;
}
```

This program uses `strstr` to search for a substring within a larger string and prints its position if found.

**5. Reversing a String:**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char str[] = "Hello, World!";
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

This program reverses a string by swapping characters from the beginning to the end.

These examples demonstrate various operations you can perform with strings in C, including finding string length, concatenating strings, comparing strings, searching for substrings, and reversing strings. Strings are a fundamental part of C programming and are used extensively in various applications.
