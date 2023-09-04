Bit manipulation operations in C allow you to work with individual bits within variables (usually integers) to perform various tasks, such as setting, clearing, toggling, or testing bits. These operations are useful when you need to control or manipulate specific flags, masks, or configuration settings. Below are some common bit manipulation operations in C:

### Setting a Bit:

To set (turn on) a specific bit in an integer variable, you can use the bitwise OR (`|`) operator with a bitmask:

```c
unsigned int setBit(unsigned int num, int pos) {
    return num | (1 << pos);
}
```

Here, `pos` represents the position of the bit to set (0 for the least significant bit). This function sets the specified bit in `num` to 1.

### Clearing a Bit:

To clear (turn off) a specific bit in an integer variable, you can use the bitwise AND (`&`) operator with a bitmask that has all bits set to 1 except the bit you want to clear:

```c
unsigned int clearBit(unsigned int num, int pos) {
    return num & ~(1 << pos);
}
```

Here, `pos` represents the position of the bit to clear. This function sets the specified bit in `num` to 0.

### Toggling a Bit:

To toggle (invert) a specific bit in an integer variable, you can use the bitwise XOR (`^`) operator with a bitmask:

```c
unsigned int toggleBit(unsigned int num, int pos) {
    return num ^ (1 << pos);
}
```

This function flips (changes from 0 to 1 or from 1 to 0) the specified bit in `num`.

### Checking a Bit:

To check the value of a specific bit in an integer variable, you can use the bitwise AND (`&`) operator with a bitmask:

```c
int checkBit(unsigned int num, int pos) {
    return (num >> pos) & 1;
}
```

Here, `pos` represents the position of the bit to check. This function returns 1 if the specified bit is set (1) and 0 if it is clear (0).

### Updating Multiple Bits:

To update multiple bits within an integer variable, you can use a combination of the above operations with appropriate bit masks.

For example, to set bits 3 and 5 in an integer variable `num`:

```c
num = setBit(num, 3); // Set bit 3
num = setBit(num, 5); // Set bit 5
```

To clear bits 2 and 4:

```c
num = clearBit(num, 2); // Clear bit 2
num = clearBit(num, 4); // Clear bit 4
```

These bit manipulation operations are often used in embedded systems, low-level programming, and hardware control to efficiently manage and manipulate individual bits within data.
