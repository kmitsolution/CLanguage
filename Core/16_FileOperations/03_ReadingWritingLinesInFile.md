To read and write strings line by line in a file in C, you can use the `fgets()` function for reading lines and the `fprintf()` function for writing lines. Here's an example of how to do this:

### Reading Lines from a File:

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *file;
    char line[100]; // Assuming each line in the file is at most 100 characters long

    // Open the file for reading
    file = fopen("example.txt", "r");

    // Check if the file was opened successfully
    if (file == NULL) {
        perror("Unable to open the file");
        exit(1);
    }

    // Read and print each line from the file
    while (fgets(line, sizeof(line), file) != NULL) {
        printf("Read: %s", line);
    }

    // Close the file
    fclose(file);

    return 0;
}
```

In this code:

- We open a file named `"example.txt"` in read mode ("r").
- We use a character array `line` to store each line read from the file.
- We use a `while` loop to read lines from the file using `fgets()`. The loop continues until `fgets()` returns `NULL`, which indicates the end of the file.
- Each line is printed to the console.

### Writing Lines to a File:

```c
#include <stdio.h>

int main() {
    FILE *file;
    char line[100];

    // Open the file for writing
    file = fopen("output.txt", "w");

    // Check if the file was opened successfully
    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    // Write lines to the file
    fprintf(file, "Line 1: This is the first line\n");
    fprintf(file, "Line 2: This is the second line\n");
    fprintf(file, "Line 3: This is the third line\n");

    // Close the file
    fclose(file);

    return 0;
}
```

In this code:

- We open a file named `"output.txt"` in write mode ("w").
- We use `fprintf()` to write lines to the file. Each call to `fprintf()` writes a line to the file.
- After writing the lines, we close the file using `fclose()`.

These examples demonstrate how to read lines from a file using `fgets()` and write lines to a file using `fprintf()`. You can modify the content of the `line` variable and the content written to the file as needed for your specific use case.
