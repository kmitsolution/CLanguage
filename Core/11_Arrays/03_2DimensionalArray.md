# 2-D Array in C
A two-dimensional array in C is a matrix-like structure that consists of rows and columns. It can be thought of as an array of arrays, where each element is identified by two indices: a row index and a column index. Here's how you declare and work with a two-dimensional array in C:

**1. Declaration and Initialization:**
To declare a two-dimensional array, you specify the data type of its elements, followed by the array name and the number of rows and columns in square brackets.

```c
data_type array_name[rows][columns];
```

For example:

```c
int matrix[3][4]; // Declares a 2D integer array named 'matrix' with 3 rows and 4 columns
```

You can also initialize a two-dimensional array at the time of declaration:

```c
int matrix[3][4] = {
    {1, 2, 3, 4},
    {5, 6, 7, 8},
    {9, 10, 11, 12}
};
```

This initializes a 3x4 matrix with integer values.

**2. Accessing Array Elements:**
You can access individual elements of a two-dimensional array using two indices: the row index and the column index, separated by square brackets.

```c
int element = matrix[1][2]; // Accesses the element at row 1, column 2 of the 'matrix'
```

**3. Array Size:**
To determine the number of rows and columns in a two-dimensional array, you can use the `sizeof` operator and divide by the size of a single element.

```c
int rows = sizeof(matrix) / sizeof(matrix[0]);
int columns = sizeof(matrix[0]) / sizeof(matrix[0][0]);
```

In the example above, `rows` will be 3, and `columns` will be 4.

**4. Modifying Array Elements:**
You can change the value of an array element by specifying the row and column indices and assigning a new value to it using the assignment operator `=`.

```c
matrix[0][1] = 20; // Modifies the element at row 0, column 1 of the 'matrix'
```

**5. Iterating Over a 2D Array:**
You can use nested loops to iterate over the elements of a two-dimensional array. One loop iterates over the rows, and another loop iterates over the columns.

```c
for (int i = 0; i < rows; i++) {
    for (int j = 0; j < columns; j++) {
        printf("matrix[%d][%d] = %d\n", i, j, matrix[i][j]);
    }
}
```

This code will print all the elements of the `matrix`.

Two-dimensional arrays are commonly used for storing and manipulating data that can be organized in a grid or table-like structure, such as matrices, tables, and game boards. Understanding how to declare, initialize, access, and manipulate two-dimensional arrays is essential for working with such data structures in C programming.
