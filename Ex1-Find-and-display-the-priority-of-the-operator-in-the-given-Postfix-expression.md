# EX 1 Display operator precedence in the infix expression.

## DATE: 24.02.2025

## Aim:

To write a C program to find and display the priority of the operator in the given Postfix expression.

## Algorithm:

Step 1 : Start the program and take the Postfix expression as input.

Step 2 : Traverse each character of the expression.

Step 3 : If the character is an operator (+, -, *, /, ^), find its priority: ^ → 3 *, / → 2 +, - → 1

Step 4 : Display the operator and its priority.

Step 5 : End the program.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression

Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013  
*/
#include <stdio.h>

int getPriority(char operator) {
    switch(operator) {
        case '^': return 3;
        case '*':
        case '/': return 2;
        case '+':
        case '-': return 1;
        default: return 0;
    }
}

int main() {
    char postfix[100];
    int i;
    
    printf("Enter a Postfix Expression: ");
    scanf("%s", postfix);
    
    printf("\nOperator priorities:\n");
    for(i = 0; postfix[i] != '\0'; i++) {
        if(postfix[i] == '+' || postfix[i] == '-' ||
           postfix[i] == '*' || postfix[i] == '/' ||
           postfix[i] == '^') {
            printf("Operator %c has priority %d\n", postfix[i], getPriority(postfix[i]));
        }
    }
    
    return 0;
}
```

## Output:

![WhatsApp Image 2025-04-29 at 11 25 18_c2822b66](https://github.com/user-attachments/assets/4b548ae0-fcf3-4bc1-9923-c1e9a565544b)

## Result:

Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
