Custom Printf Function
This project consists of building a custom version of the printf function called _printf. The custom _printf function should be able to handle different data types and formatting options, as described below.

Features
Basic Features
_printf should be able to handle the following conversion specifiers:
c: character
s: string
%: literal percentage character
Advanced Features
Handle the following conversion specifiers:

d: signed decimal integer
i: signed decimal integer
Custom conversion specifier:

b: unsigned int argument converted to binary
Handle the following conversion specifiers:

u: unsigned decimal integer
o: unsigned octal integer
x: unsigned hexadecimal integer (lowercase)
X: unsigned hexadecimal integer (uppercase)
Use a local buffer of 1024 chars to optimize write system calls.

Custom conversion specifier:

S: string with non-printable characters (ASCII < 32 or >= 127) represented as \xHH, where HH is the hexadecimal value of the character.
Handle the conversion specifier p for pointer address.

Handle the following flag characters for non-custom conversion specifiers:

+: forces a sign
space: prints a space for positive numbers
#: alternate form
Handle the following length modifiers for non-custom conversion specifiers:

l: long int
h:

Conversion specifiers to handle: d, i, u, o, x, X
Handle the field width for non-custom conversion specifiers.

Handle the precision for non-custom conversion specifiers.

Handle the 0 flag character for non-custom conversion specifiers.

Handle the - flag character for non-custom conversion specifiers.

Custom conversion specifier:

r: prints the reversed string
Custom conversion specifier:
R: prints the rot13'ed string
Ensure all the above options work well together.
Repository
All the code for this project should be stored in the following GitHub repository: printf

Usage
To use the custom _printf function, include the header file main.h in your C code and call the _printf function as you would with the standard printf function. The custom _printf function should work with most format strings and conversion specifiers supported by the standard printf function, as well as the custom specifiers mentioned above.

c
Copy code
#include "main.h"

int main(void)
{
    _printf("Hello, %s!\n", "world");
    _printf("Decimal: %d\n", 42);
    _printf("Binary: %b", 45);
}