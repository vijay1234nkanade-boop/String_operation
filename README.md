
# 1. Basic String Operations

## Program Info
This program implements the following string operations without using built-in string functions:
- Length calculation  
- Copy  
- Reverse  
- Concatenation  

---

## Pseudocode
'''
START
READ VNKstr1, VNKstr2
CALCULATE length of VNKstr1
COPY VNKstr1 into VNKcopy
REVERSE VNKstr1 into VNKrstr
CONCATENATE VNKstr1 and VNKstr2 into VNKconcat
PRINT results
END

cpp
Copy code

---

## Actual Program
```c
#include <stdio.h>

int main() {
    char VNKstr1[100], VNKstr2[100], VNKcopy[100], VNKrstr[100], VNKconcat[200];
    int VNKi, VNKlen = 0;

    printf("Enter first string: ");
    gets(VNKstr1);

    printf("Enter second string: ");
    gets(VNKstr2);

    // Length
    for (VNKi = 0; VNKstr1[VNKi] != '\0'; VNKi++) {
        VNKlen++;
    }

    // Copy
    for (VNKi = 0; VNKstr1[VNKi] != '\0'; VNKi++) {
        VNKcopy[VNKi] = VNKstr1[VNKi];
    }
    VNKcopy[VNKi] = '\0';

    // Reverse
    int VNKj = 0;
    for (VNKi = VNKlen - 1; VNKi >= 0; VNKi--) {
        VNKrstr[VNKj++] = VNKstr1[VNKi];
    }
    VNKrstr[VNKj] = '\0';

    // Concatenation
    VNKi = 0; VNKj = 0;
    while (VNKstr1[VNKi] != '\0') {
        VNKconcat[VNKj++] = VNKstr1[VNKi++];
    }
    VNKi = 0;
    while (VNKstr2[VNKi] != '\0') {
        VNKconcat[VNKj++] = VNKstr2[VNKi++];
    }
    VNKconcat[VNKj] = '\0';

    // Output
    printf("\nLength of first string: %d", VNKlen);
    printf("\nCopy of first string: %s", VNKcopy);
    printf("\nReverse of first string: %s", VNKrstr);
    printf("\nConcatenation of two strings: %s\n", VNKconcat);

    return 0;
}

'''
 Output



Enter first string: hello
Enter second string: world

Length of first string: 5
Copy of first string: hello
Reverse of first string: olleh
Concatenation of two strings: helloworld
