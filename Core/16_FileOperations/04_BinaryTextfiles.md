In C, you can work with both text and binary files. Text files contain human-readable characters, while binary files store data in a more compact and efficient format without considering human readability. Here's how to work with both types of files in C:

### Text Files:

**Reading from a Text File:**

To read from a text file, you typically use functions like `fopen()`, `fgets()`, or `fscanf()`. Here's an example of reading lines from a text file:

```c
#include <stdio.h>

int main() {
    FILE *file;
    char line[100];

    // Open the text file for reading
    file = fopen("textfile.txt", "r");

    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    while (fgets(line, sizeof(line), file) != NULL) {
        printf("Read: %s", line);
    }

    fclose(file);
    return 0;
}
```

**Writing to a Text File:**

To write to a text file, you often use functions like `fopen()`, `fprintf()`, or `fputs()`. Here's an example of writing lines to a text file:

```c
#include <stdio.h>

int main() {
    FILE *file;

    // Open the text file for writing
    file = fopen("output.txt", "w");

    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    fprintf(file, "Line 1: This is the first line\n");
    fprintf(file, "Line 2: This is the second line\n");

    fclose(file);
    return 0;
}
```

### Binary Files:

**Reading from a Binary File:**

Binary files can contain any kind of data, including non-textual data like images or serialized objects. To read from a binary file, you use functions like `fopen()`, `fread()`, and `fwrite()`. Here's an example of reading binary data from a file:

```c
#include <stdio.h>

struct Data {
    int number;
    double value;
};

int main() {
    FILE *file;
    struct Data data;

    // Open the binary file for reading
    file = fopen("binaryfile.bin", "rb");

    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    while (fread(&data, sizeof(struct Data), 1, file) == 1) {
        printf("Read: Number=%d, Value=%.2lf\n", data.number, data.value);
    }

    fclose(file);
    return 0;
}
```

**Writing to a Binary File:**

To write binary data to a file, you can use functions like `fopen()`, `fwrite()`, and `fread()`. Here's an example of writing binary data to a file:

```c
#include <stdio.h>

struct Data {
    int number;
    double value;
};

int main() {
    FILE *file;
    struct Data data;

    // Open the binary file for writing
    file = fopen("output.bin", "wb");

    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    data.number = 42;
    data.value = 3.14159;

    fwrite(&data, sizeof(struct Data), 1, file);

    fclose(file);
    return 0;
}
```

Working with binary files is particularly useful when dealing with non-textual data or when you need to preserve the exact data representation. Binary files are not human-readable like text files, so they are used for efficiency and data integrity. Be cautious when working with binary files to ensure data consistency and portability across different platforms.
