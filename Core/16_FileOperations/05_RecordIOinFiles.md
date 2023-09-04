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

### Modifying records in a file typically involves the following steps:

1. **Open the File**: Open the file in a mode that allows both reading and writing (e.g., `"r+"` or `"rb+"` for binary files). You'll need read access to retrieve the existing data and write access to update it.

2. **Read Records**: Read the records from the file one by one, storing them in memory (e.g., in an array or struct). You can use `fread()` for binary files or `fgets()`/`fscanf()` for text files.

3. **Modify the Desired Record(s)**: Once you have the records in memory, make the necessary modifications to the specific record(s) you want to change.

4. **Rewrite the File**: Write the modified records back to the file. You may need to rewrite the entire file, including the unmodified records, or use a temporary file for updating.

5. **Close the Files**: Close both the input file (the one you read from) and the output file (the one you wrote to).

Here's an example of how to modify records in a binary file:

```c
#include <stdio.h>

struct Record {
    int id;
    char name[50];
    double salary;
};

int main() {
    FILE *inputFile, *outputFile;
    struct Record records[3]; // Assuming 3 records in the file

    // Open the input file for reading and writing
    inputFile = fopen("records.dat", "rb+");
    if (inputFile == NULL) {
        perror("Unable to open the input file");
        return 1;
    }

    // Read the records from the input file
    fread(records, sizeof(struct Record), 3, inputFile);

    // Modify the desired record(s)
    records[1].salary = 65000.0;

    // Open a temporary output file
    outputFile = fopen("temp.dat", "wb");
    if (outputFile == NULL) {
        perror("Unable to open the output file");
        return 1;
    }

    // Write the modified records to the output file
    fwrite(records, sizeof(struct Record), 3, outputFile);

    // Close both files
    fclose(inputFile);
    fclose(outputFile);

    // Rename the temporary file to replace the original file
    if (rename("temp.dat", "records.dat") != 0) {
        perror("Error renaming the file");
        return 1;
    }

    return 0;
}
```

In this example:

- We open the input file `"records.dat"` in `"rb+"` mode to allow reading and writing.
- We read the records into the `records` array.
- We modify the salary of the second record.
- We open a temporary output file `"temp.dat"` in `"wb"` mode for writing.
- We write the modified records to the output file.
- We close both the input and output files.
- Finally, we rename the temporary file to replace the original file, effectively updating the records in the file.

Please note that this example assumes fixed-size records. If your records have varying lengths, additional considerations are needed. Also, error handling and data validation are crucial when working with files to ensure the safety and integrity of your data.
