# 1. Basic String Operations

## Program Info
Implements string operations without using built-in string functions:
- Length calculation  
- Copy  
- Reverse  
- Concatenation  

---

## Pseudocode
START
READ str1, str2
CALCULATE length of str1
COPY str1 into copy
REVERSE str1 into rstr
CONCATENATE str1 and str2 into concat
PRINT results
END

cpp
Copy code

---

## Actual Program

#include <iostream>
using namespace std;

int main() {
    char VNKstr1[100], VNKstr2[100], VNKcopy[100], VNKrstr[100], VNKconcat[200];
    int VNKi, VNKlen = 0;

    cout << "Enter first string: ";
    cin.getline(VNKstr1, 100);

    cout << "Enter second string: ";
    cin.getline(VNKstr2, 100);

    // Length
    for (VNKi = 0; VNKstr1[VNKi] != '\0'; VNKi++) VNKlen++;

    // Copy
    for (VNKi = 0; VNKstr1[VNKi] != '\0'; VNKi++) VNKcopy[VNKi] = VNKstr1[VNKi];
    VNKcopy[VNKi] = '\0';

    // Reverse
    int VNKj = 0;
    for (VNKi = VNKlen - 1; VNKi >= 0; VNKi--) VNKrstr[VNKj++] = VNKstr1[VNKi];
    VNKrstr[VNKj] = '\0';

    // Concatenate
    VNKi = 0; VNKj = 0;
    while (VNKstr1[VNKi] != '\0') VNKconcat[VNKj++] = VNKstr1[VNKi++];
    VNKi = 0;
    while (VNKstr2[VNKi] != '\0') VNKconcat[VNKj++] = VNKstr2[VNKi++];
    VNKconcat[VNKj] = '\0';

    // Output
    cout << "\nLength of first string: " << VNKlen;
    cout << "\nCopy of first string: " << VNKcopy;
    cout << "\nReverse of first string: " << VNKrstr;
    cout << "\nConcatenation of two strings: " << VNKconcat << endl;

    return 0;
}

---------
 Output=

Enter first string: hello
Enter second string: world

Length of first string: 5
Copy of first string: hello
Reverse of first string: olleh
Concatenation of two strings: helloworld
```cpp
