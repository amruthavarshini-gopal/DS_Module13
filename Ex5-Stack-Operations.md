# Ex5 Stack Operations

## DATE: 24.02.2025

## Aim:

To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm:

1. Initialize top as -1 and declare stack as a character array.

2. To push, increment top and assign the character to stack[top].

3. To pop, check if top is -1 and return -1 if true.

4. If not, return stack[top] and decrement top.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Amruthavarshini Gopal 
RegisterNumber: 212223230013  
*/
#include <stdio.h>

#define SIZE 100

char stack[SIZE];
int top = -1;

// Push an element onto the stack
void push(char x) {
    if (top == SIZE - 1) {
        printf("Stack Overflow\n");
        return;
    }
    stack[++top] = x;
}

// Pop an element from the stack
char pop() {
    if (top == -1) {
        printf("Stack Underflow\n");
        return -1;  // Error value
    }
    return stack[top--];
}
```

## Output:

![438593405-0af51829-ab47-44bf-8b06-4a6950af971e](https://github.com/user-attachments/assets/79b20ec0-854d-4d16-a092-5842222a0411)


## Result:

Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
