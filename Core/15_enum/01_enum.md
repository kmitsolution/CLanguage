In C, an `enum` (short for enumeration) is a user-defined data type that consists of a set of named integer constants. It provides a way to assign meaningful names to integral values, making the code more readable and self-explanatory. Enums are often used to define a list of related symbolic values. Here's how you declare and use enums in C:

### Enum Declaration:

To declare an enum, you use the `enum` keyword followed by a list of comma-separated constant names enclosed in curly braces. Optionally, you can assign specific integer values to these constants. If you don't assign values, the compiler will automatically assign consecutive integer values, starting from 0.

```c
enum Days {
    Sunday,    // Assigned 0 by default
    Monday,    // Assigned 1 by default
    Tuesday,   // Assigned 2 by default
    Wednesday, // Assigned 3 by default
    Thursday,  // Assigned 4 by default
    Friday,    // Assigned 5 by default
    Saturday   // Assigned 6 by default
};
```

In this example, we've declared an enum named `Days` with seven constants, and the compiler will assign integer values starting from 0.

### Enum Variables:

You can declare variables of the enum type, just like any other data type:

```c
enum Days today = Tuesday;
```

Here, we've declared a variable `today` of type `enum Days` and assigned it the value `Tuesday`.

### Accessing Enum Constants:

You can use the named constants within an enum just like any other variables or constants. For example:

```c
enum Days currentDay = Sunday;

if (currentDay == Sunday) {
    printf("It's a lazy Sunday!\n");
}
```

### Explicitly Assigning Values:

You can explicitly assign values to enum constants if you want to control the underlying integer values. For example:

```c
enum Status {
    Inactive = 0,
    Active = 1,
    Suspended = 2
};
```

In this case, `Inactive` is explicitly assigned 0, `Active` is assigned 1, and `Suspended` is assigned 2.

### Size of Enum:

The size of an enum is typically the size of an integer (often 4 bytes on most systems), but it can vary depending on the compiler and platform.

Enums are helpful in making code more readable, especially when dealing with a set of related constants. They provide a way to give meaningful names to numeric values, making your code self-documenting and easier to understand.
