# String Functions

In C, string functions are part of the standard library and are declared in the `<string.h>` header. These functions provide a wide range of operations for manipulating and working with strings (character arrays). Here are some commonly used string functions in C:

**1. `strlen` - String Length:**

```c
#include <string.h>

size_t strlen(const char *str);
```

This function calculates the length of a null-terminated string and returns the number of characters in the string, excluding the null terminator.

**2. `strcpy` - String Copy:**

```c
#include <string.h>

char *strcpy(char *dest, const char *src);
```

`strcpy` copies the content of the source string `src` into the destination string `dest` and returns a pointer to `dest`.

**3. `strcat` - String Concatenate:**

```c
#include <string.h>

char *strcat(char *dest, const char *src);
```

`strcat` appends the content of the source string `src` to the end of the destination string `dest` and returns a pointer to `dest`.

**4. `strcmp` - String Compare:**

```c
#include <string.h>

int strcmp(const char *str1, const char *str2);
```

`strcmp` compares two strings `str1` and `str2` and returns an integer indicating their relative order. It returns a negative value if `str1` is less than `str2`, 0 if they are equal, and a positive value if `str1` is greater than `str2`.

**5. `strchr` - String Character Search:**

```c
#include <string.h>

char *strchr(const char *str, int character);
```

`strchr` searches for the first occurrence of the character `character` in the string `str` and returns a pointer to that character or `NULL` if the character is not found.

**6. `strstr` - String Substring Search:**

```c
#include <string.h>

char *strstr(const char *haystack, const char *needle);
```

`strstr` searches for the first occurrence of the substring `needle` in the string `haystack` and returns a pointer to the beginning of the first occurrence or `NULL` if the substring is not found.

**7. `strncpy` - String Copy with Length Limit:**

```c
#include <string.h>

char *strncpy(char *dest, const char *src, size_t n);
```

`strncpy` copies at most `n` characters from the source string `src` to the destination string `dest`. It pads with null characters if necessary.

**8. `strncat` - String Concatenate with Length Limit:**

```c
#include <string.h>

char *strncat(char *dest, const char *src, size_t n);
```

`strncat` appends at most `n` characters from the source string `src` to the end of the destination string `dest`. It ensures that the result is null-terminated.

**9. `strncmp` - String Compare with Length Limit:**

```c
#include <string.h>

int strncmp(const char *str1, const char *str2, size_t n);
```

`strncmp` compares at most `n` characters of two strings `str1` and `str2`. It returns the same values as `strcmp`.

These are some of the fundamental string functions in C. They are used extensively in C programming for tasks such as copying, concatenating, comparing, and searching for strings. When working with strings, it's essential to use these functions to ensure proper handling and avoid common pitfalls like buffer overflows and memory corruption.
