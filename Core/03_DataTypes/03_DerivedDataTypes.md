In C, derived data types are user-defined data types that are created by combining one or more basic data types or other derived data types. These derived data types are used to create more complex and structured data representations. Here are some commonly used derived data types in C:

1. **Arrays**: An array is a collection of elements of the same data type, stored in contiguous memory locations. Elements in an array can be accessed using an index.

   ```c
   int numbers[5]; // Declares an integer array of size 5
   ```
   **Strings** String is the collection of characters

   ```c
   char names[5]; // Declare a string with 5 character length
   ```
## Example of Array
```c
#include <stdio.h>
int main(){
    //Integer Array Example (Each element holds 4 bytes of memory)
    printf("###### Example of Integer Array ######");
    int numbers[5]={10,20,30,40,50};
    printf("\nFirst Element=%d and Addrr=%d",numbers[0],&numbers[0]);
    printf("\nSec Element=%d and Addrr=%d",numbers[1],&numbers[1]);
    //Char Array Example (Each element holds 1 byte of memory)
    printf("\n\n###### Example of Character Array ######");
    char name[4]={'a','b','c','d'};
  
    printf("\nFirst Element=%c and Addrr=%d",name[0],&name[0]);
    printf("\nSec Element=%c and Addrr=%d",name[1],&name[1]);
    
    return 0;
}
```
### output of above example
```
###### Example of Integer Array ######
First Element=10 and Addrr=6422280
Sec Element=20 and Addrr=6422284

###### Example of Character Array ######
First Element=a and Addrr=6422276
Sec Element=b and Addrr=6422277
```
3. **Pointers**: Pointers are variables that store memory addresses. They are used to point to other data types, allowing for dynamic memory allocation and manipulation.

   ```c
   int *ptr; // Declares a pointer to an integer
   ```
## Example of Pointer
```c
#include <stdio.h>
#include<conio.h>
int main(){
   
    int *ptr;
    int i=3;
    ptr =&i;
    printf ("\nAddress of i=%d and Add which pointer holds =%d", &i,ptr);
    printf ("\nValue of i=%d and Value which pointer holds =%d", i,*ptr);
    return 0;
}
```
### output of above example
```
Address of i=6422296 and Add which pointer holds =6422296
Value of i=3 and Value which pointer holds =3
```

