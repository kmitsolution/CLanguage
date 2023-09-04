Advanced file operations in C involve more complex tasks such as working with structured data, handling errors, and implementing various file processing techniques. Here are some advanced file operation examples in C:

### Reading and Writing Structured Data to Binary Files:

In this example, we define a structure to represent records, read records from a binary file, and write records to the file.

```c
#include <stdio.h>

struct Record {
    int id;
    char name[50];
    double salary;
};

int main() {
    FILE *file;
    struct Record records[3]; // Assuming 3 records in the file

    // Open the binary file for reading and writing
    file = fopen("records.dat", "rb+");
    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    // Read the records from the input file
    fread(records, sizeof(struct Record), 3, file);

    // Modify the desired record(s)
    records[1].salary = 65000.0;

    // Write the modified records back to the file
    fseek(file, 0, SEEK_SET); // Set the file position to the beginning
    fwrite(records, sizeof(struct Record), 3, file);

    // Close the file
    fclose(file);

    return 0;
}
```

### Error Handling and File Existence Check:

This example demonstrates error handling and checking whether a file exists before attempting to read or write.

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *file;

    // Check if the file exists
    if ((file = fopen("data.txt", "r")) == NULL) {
        perror("Error opening the file");
        return 1;
    }

    // Perform file operations here...

    // Close the file
    fclose(file);

    return 0;
}
```

### Appending Data to a Text File:

In this example, we open a text file in append mode to add new data without overwriting the existing content.

```c
#include <stdio.h>

int main() {
    FILE *file;

    // Open the text file for appending
    file = fopen("log.txt", "a");
    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    // Append new data to the file
    fprintf(file, "New log entry\n");

    // Close the file
    fclose(file);

    return 0;
}
```

### Copying Files:

This example reads data from one file and writes it to another to create a file copy.

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *source, *destination;
    char ch;

    source = fopen("source.txt", "r");
    if (source == NULL) {
        perror("Error opening the source file");
        return 1;
    }

    destination = fopen("destination.txt", "w");
    if (destination == NULL) {
        perror("Error opening the destination file");
        fclose(source);
        return 1;
    }

    while ((ch = fgetc(source)) != EOF) {
        fputc(ch, destination);
    }

    fclose(source);
    fclose(destination);

    return 0;
}
```

These examples cover various advanced file operations in C, including working with structured data, error handling, appending data to files, and copying files. Depending on your specific requirements, you can adapt these examples or combine techniques to achieve more complex file processing tasks.
