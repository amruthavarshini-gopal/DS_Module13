# Ex4 Evaluation of prefix expression

## DATE: 24.02.2025

## Aim:

To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm:

1. Start the program.

2. Initialize an empty stack s with a variable top for tracking the stack index.

3. Define a push() function to add an element to the stack.

4. Define a pop() function to remove and return the top element from the stack.

5. In evalprefix(), loop through the given prefix expression from right to left.

6. For each character, if it’s an operator (+, *), pop two operands from the stack, perform the 
operation, and push the result.

7. If it's a digit, convert it to an integer and push it onto the stack; finally, print the result after 
the loop ends.

8. End the program.

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013 
*/
#include<stdio.h> 
#include<string.h> 
#include<ctype.h>
int s[50]; 
int top=0;
void push(int ch)
{
top++; 
s[top]=ch;
}
int pop()
{
int ch; 
ch=s[top]; 
top=top-1; 
return(ch);
}
void evalprefix(char p[50])
{
int a,b,c,i;
for(i=strlen(p)-1;i>=0;i--)
{
if(p[i]=='+')
{
a=pop();
b=pop(); 
c=a+b; 
push(c);
}
else if(p[i]=='*')
{
a=pop();
b=pop(); 
c=a*b; 
push(c);
}
else
{
push(p[i]-48);
}
}
printf("%d",pop());
}
```

## Output:

![WhatsApp Image 2025-04-29 at 11 37 47_e2f75a8e](https://github.com/user-attachments/assets/24f138c8-f041-432c-a45b-e34d892caa08)


## Result:

Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
