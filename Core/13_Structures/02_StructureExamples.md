Here are some examples of structures in C:

**1. Basic Structure Example:**

```c
#include <stdio.h>

// Define a structure named 'Person'
struct Person {
    char name[50];
    int age;
    float height;
};

int main() {
    // Create an instance of the 'Person' structure
    struct Person person1;

    // Assign values to its members
    strcpy(person1.name, "Alice");
    person1.age = 25;
    person1.height = 5.7;

    // Display the information
    printf("Name: %s\n", person1.name);
    printf("Age: %d\n", person1.age);
    printf("Height: %.2f feet\n", person1.height);

    return 0;
}
```

This program defines a `Person` structure and creates an instance of it to store information about a person.

**2. Array of Structures:**

```c
#include <stdio.h>

struct Student {
    char name[50];
    int roll_number;
};

int main() {
    // Create an array of 'Student' structures
    struct Student students[3];

    // Initialize the array
    strcpy(students[0].name, "Alice");
    students[0].roll_number = 101;

    strcpy(students[1].name, "Bob");
    students[1].roll_number = 102;

    strcpy(students[2].name, "Charlie");
    students[2].roll_number = 103;

    // Display student information
    for (int i = 0; i < 3; i++) {
        printf("Name: %s\n", students[i].name);
        printf("Roll Number: %d\n", students[i].roll_number);
    }

    return 0;
}
```

This example uses an array of `Student` structures to store information about multiple students.

**3. Nested Structures:**

```c
#include <stdio.h>

struct Date {
    int day;
    int month;
    int year;
};

struct Employee {
    char name[50];
    struct Date birthdate;
};

int main() {
    struct Employee employee1;

    strcpy(employee1.name, "Alice");
    employee1.birthdate.day = 15;
    employee1.birthdate.month = 3;
    employee1.birthdate.year = 1990;

    printf("Name: %s\n", employee1.name);
    printf("Birthdate: %d/%d/%d\n", employee1.birthdate.day, employee1.birthdate.month, employee1.birthdate.year);

    return 0;
}
```

This example demonstrates the use of nested structures, where an `Employee` structure contains a `Date` structure for the birthdate.

Structures in C are versatile and allow you to organize and manage complex data effectively. You can create arrays of structures, nest structures, and use them to represent various real-world entities and data structures.
