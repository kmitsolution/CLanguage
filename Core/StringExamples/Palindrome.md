# Check String is Palindrome or not
To check if a string is a palindrome in C, you can compare characters from the beginning and end of the string. If the characters match all the way through, the string is a palindrome. Here's a simple C program to do that:

```c
#include <stdio.h>
#include <string.h>
#include <stdbool.h>

// Function to check if a string is a palindrome
bool isPalindrome(const char *str) {
    int left = 0;
    int right = strlen(str) - 1;

    while (left < right) {
        if (str[left] != str[right]) {
            return false; // Not a palindrome
        }
        left++;
        right--;
    }

    return true; // It's a palindrome
}

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);

    if (isPalindrome(str)) {
        printf("%s is a palindrome.\n", str);
    } else {
        printf("%s is not a palindrome.\n", str);
    }

    return 0;
}
```

In this program:

1. The `isPalindrome` function takes a string as an argument and checks if it's a palindrome by comparing characters from the start and end of the string, moving towards the center.

2. The `main` function reads a string from the user, and then it calls the `isPalindrome` function to determine if the entered string is a palindrome.

Keep in mind that this program treats strings without spaces and considers the case of characters, so "racecar" would be recognized as a palindrome, but "A man a plan a canal Panama" would not be considered a palindrome. If you want to ignore spaces and case, you would need to preprocess the input string accordingly.
