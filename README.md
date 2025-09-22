# String Operations in C (Without Inbuilt Functions)

## 🖥 Program Code

```c
#include <stdio.h>

void main() {
    char name_VNK[] = "Vijay";
    char str_VNK[] = "Kanade";
    int len_VNK = sizeof(name_VNK) / sizeof(name_VNK[0]);
    int str_len_VNK = (sizeof(str_VNK) / sizeof(str_VNK[0]))-1;
    printf("Length of the string %s is: %d", name_VNK, len_VNK-1);

    char copy_VNK[20];
    for (int i_VNK = 0; i_VNK < len_VNK; i_VNK++) {
        copy_VNK[i_VNK] = name_VNK[i_VNK];
    }
    printf("\nThe copied string is: %s", copy_VNK);

    char rev_VNK[20];
    int i_VNK;
    int j_VNK = 0;
    for (i_VNK = len_VNK-2; i_VNK >=0; i_VNK--) {
        rev_VNK[j_VNK] = name_VNK[i_VNK];
        j_VNK++;
    }
    rev_VNK[j_VNK] = '\0';  // Null terminate the reversed string
    printf("\nThe reversed string is: %s", rev_VNK);

    int x_VNK = 0;
    int y_VNK = 0;
    while (name_VNK[x_VNK] != '\0') {
        x_VNK++;
    }
    while (str_VNK[y_VNK] != '\0') {
        name_VNK[x_VNK] = str_VNK[y_VNK];
        x_VNK++;
        y_VNK++;
    }
    name_VNK[x_VNK] = '\0';  // Null terminate the concatenated string
    printf("\nConcatenated string is: %s", name_VNK);
}
📝 Algorithm Explanation
Length Calculation:

Initialize a counter and iterate through the string until the null terminator ('\0') is encountered, incrementing the counter for each character.

Using the formula sizeof(name_VNK) / sizeof(name_VNK[0]) to calculate the length of the string array.

String Copy:

Create a new character array to hold the copied string.

Use a loop to copy each character from the original string.

Ensure to copy the null terminator at the end.

Print the copied string.

String Reversal:

Create a new character array to hold the reversed string.

Use a loop to copy characters from the end of the original string to the start of the new array.

Add a null terminator at the end.

Print the reversed string.

String Concatenation:

Find the end of the first string.

Append characters from the second string.

Add a null terminator at the end.

Print the concatenated string.

Dry Run
Input: "Vijay", "Kanade"

Length Calculation:

rust
Copy code
- 'V' -> len_VNK = 1
- 'i' -> len_VNK = 2
- 'j' -> len_VNK = 3
- 'a' -> len_VNK = 4
- 'y' -> len_VNK = 5
- '\0' -> Stop iteration
Final length: 5

Output: "Length of the string Vijay is: 5"

String Copy:

rust
Copy code
- 'V' -> copy_VNK[0] = 'V'
- 'i' -> copy_VNK[1] = 'i'
- 'j' -> copy_VNK[2] = 'j'
- 'a' -> copy_VNK[3] = 'a'
- 'y' -> copy_VNK[4] = 'y'
- '\0' -> copy_VNK[5] = '\0'
Copied string: "Vijay"

Output: "The copied string is: Vijay"

String Reversal:

rust
Copy code
- 'y' -> rev_VNK[0] = 'y'
- 'a' -> rev_VNK[1] = 'a'
- 'j' -> rev_VNK[2] = 'j'
- 'i' -> rev_VNK[3] = 'i'
- 'V' -> rev_VNK[4] = 'V'
- '\0' -> rev_VNK[5] = '\0'
Reversed string: "yaj iV"

Output: "The reversed string is: yaj iV"

String Concatenation:

rust
Copy code
- Original: "Vijay"
- Append: "Kanade"
- Result: "VijayKanade"
Output: "Concatenated string is: VijayKanade"
