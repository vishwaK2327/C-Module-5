# Pointers: Reverse a String Using Pointers in C

## 🎯 Aim

To write a C program that prints a string in reverse using a pointer.

## 🧠 Algorithm

1. **Input**: Read a string from the user.
2. **Reverse String**:
   - Use a pointer to traverse the string to find its length.
   - Then, move the pointer to the last character of the string.
   - Print characters in reverse by decrementing the pointer.
3. **Output**: Display the reversed string.

## Program
```
#include <stdio.h>
int main() {
    char str[100];
    char *ptr;
    int length = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    while (str[length] != '\0') {
        if (str[length] == '\n') {
            str[length] = '\0';
            break;
        }
        length++;
    }
    ptr = str;
    ptr = ptr + length - 1;
    printf("Reversed string: ");
    while (length > 0) {
        printf("%c", *ptr);
        ptr--;
        length--;
    }
    printf("\n");
    return 0;
}
```

## Output
```
Enter a string: Hello World
Reversed string: dlroW olleH
```



## Result
The above programme is implemented and executed.
