# EX3 Implementation of Tower of Hanoi

## DATE: 24.02.2025

## Aim:

To write a C program to implement Tower of Hanoi.

## Algorithm:

Step1: Start with three rods: source (A), auxiliary (C), and destination (B).

Step2: If there is only one disk, move it directly from the source to the destination.

Step3: For more than one disk, move the top (n-1) disks from the source to the auxiliary rod using the destination as a helper.

Step4: Move the nth (largest) disk from the source to the destination rod.

Step5: Move the (n-1) disks from the auxiliary rod to the destination rod using the source as a helper.

Step6: Repeat the above steps recursively until all disks are moved to the destination rod.

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013 
*/
#include<stdio.h>
void TOH(int n,char x,char y,char z)
{
    if(n>0)
    {
        TOH(n-1,x,z,y);
        printf("%c to %c\n",x,y);
        TOH(n-1,z,y,x);
    }
    
}
int main()
{
    int n=2;
    TOH(n,'A','B','C');
}
```

## Output:

![WhatsApp Image 2025-04-29 at 11 24 52_7c8cccae](https://github.com/user-attachments/assets/d244dcf3-3715-4647-b44f-fc3840270e35)


## Result:

Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
