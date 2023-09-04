# Record I/O in C
To perform record I/O in a file in C, you often work with structured data, such as records or structs. You can read and write these records to and from a file using functions like `fwrite()`, `fread()`, and `fprintf()`. Here's a step-by-step example of how to perform record I/O in C:

Suppose you have a struct representing a record:

```c
#include <stdio.h>

// Define a struct to represent a record
struct Record {
    int id;
    char name[50];
    double salary;
};
```

### Writing Records to a File:

To write records to a file, you can use `fwrite()`:

```c
int main() {
    FILE *file;
    struct Record records[3];

    // Populate the records
    records[0].id = 1;
    snprintf(records[0].name, sizeof(records[0].name), "John");
    records[0].salary = 50000.0;

    records[1].id = 2;
    snprintf(records[1].name, sizeof(records[1].name), "Alice");
    records[1].salary = 60000.0;

    records[2].id = 3;
    snprintf(records[2].name, sizeof(records[2].name), "Bob");
    records[2].salary = 55000.0;

    // Open the file for writing
    file = fopen("records.dat", "wb");

    // Check if the file was opened successfully
    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    // Write the records to the file
    fwrite(records, sizeof(struct Record), 3, file);

    // Close the file
    fclose(file);

    return 0;
}
```

In this code:

- We define an array of `struct Record` to hold multiple records.
- We populate the records with data.
- We open the file in binary write mode ("wb") using `fopen()`.
- We use `fwrite()` to write the entire array of records to the file. The third argument (3) specifies the number of records to write.

### Reading Records from a File:

To read records from a file, you can use `fread()`:

```c
int main() {
    FILE *file;
    struct Record records[3];

    // Open the file for reading
    file = fopen("records.dat", "rb");

    // Check if the file was opened successfully
    if (file == NULL) {
        perror("Unable to open the file");
        return 1;
    }

    // Read the records from the file
    fread(records, sizeof(struct Record), 3, file);

    // Close the file
    fclose(file);

    // Display the read records
    for (int i = 0; i < 3; i++) {
        printf("Record %d:\n", i + 1);
        printf("ID: %d\n", records[i].id);
        printf("Name: %s\n", records[i].name);
        printf("Salary: %.2lf\n", records[i].salary);
    }

    return 0;
}
```

In this code:

- We open the same file in binary read mode ("rb") using `fopen()`.
- We use `fread()` to read the records from the file into our array of `struct Record`.
- We close the file.
- Finally, we display the read records.

This example demonstrates how to perform record I/O in C using binary file mode. You can adapt this code to your specific data structure and file format as needed.
