# Ex2 Conversion of the infix expression into postfix expression

## DATE: 24.02.2025

## AIM:

To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm:

Step 1 : Initialize an empty stack to hold operators and set the top to -1.

Step 2 : Scan the input expression from left to right.

Step 3 : If operand, output it directly.

Step 4 : If '(, push it to stack; if ')', pop and output until '(' is found.

Step 5 : If operator, pop from stack and output while the top has higher or equal priority, then push the operator.

Step 6 : After scanning, pop and output all remaining operators from the stack.

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by: Amruthavarshini Gopal 
RegisterNumber: 212223230013 
*/
#include<stdio.h>
#include<ctype.h>
char stack[100];
int top=-1;
void push(char x)
{
    stack[++top]=x;
}
char pop()
{
    if(top==-1)
    {
        return -1;
    }
    else
    {
        return stack[top--];
    }
}
int priority(char x)
{
    if(x=='(')
    return 0;
    else if((x=='&')||(x=='|'))
    return 1;
    else if((x=='+')||(x=='-'))
    return 2;
    else if((x=='*')||(x=='/')||(x=='%'))
    return 3;
    else if(x=='^')
    return 4;
    return -1;
}
void post(char *exp)
{
    char *e=exp;
    char x;
    while(*e!='\0')
    {
        if(isalnum(*e))
        {
            printf("%c ",*e);
        }
        else if(*e=='(')
        {
            push(*e);
        }
        else if(*e==')')
        {
            while((x=pop())!='(')
            {
                printf("%c ",x);
            }
        }
        else
        {
            while(priority(stack[top])>=priority(*e))
            {
                printf("%c ",pop());
            }
            push(*e);
        }
        e++;
    }
    while(top!=-1)
    {
        printf("%c ",pop());
    }
}
int main()
{
    char exp[100]="4*(2+5)*9";
    post(exp);
    return 0;
    
}
```

## Output:

![image](https://github.com/user-attachments/assets/eece63ae-0f7e-41a7-8da8-3502d663f806)

## Result:

Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
