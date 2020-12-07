# Cognizance2020

## Task-04
### * C Program to find the product of two numbers of same order below 10
1. First we declare three matrices namely A, B, mul matrix, and some variables required.
2. Then we will take the input of matrices about number of rows and columns.
3. Next, we take the values of elements of the two matrix.
4. Then the following program syntax will lead us to get the product matrix of A and B.




![Matrix](https://i1.wp.com/www.mathbootcamps.com/wp-content/uploads/square-matrix-multiply-identity.png?w=387&ssl=1)



```c

#include<stdio.h>    
#include<stdlib.h>  
int main()
{  
int A[10][10],B[10][10],mul[10][10],r,c,i,j,k;    
system("cls");  
printf("enter the number of row=");    
scanf("%d",&r);    
printf("enter the number of column=");    
scanf("%d",&c);    
printf("enter the first matrix element=\n");    
for(i=0;i<r;i++)    
{    
    for(j=0;j<c;j++)    
    {
        printf("enter A[%d][%d]=",i,j);    
        scanf("%d",&A[i][j]);    
    }    
}    
printf("enter the second matrix element=\n");    
for(i=0;i<r;i++)    
{    
    for(j=0;j<c;j++)    
    {    
        printf("enter B[%d][%d]=",i,j); 
        scanf("%d",&B[i][j]);    
    }    
}    
    
printf("multiply of the matrix=\n");    
for(i=0;i<r;i++)    
{    
    for(j=0;j<c;j++)    
    {    
        mul[i][j]=0;    
        for(k=0;k<c;k++)    
        {    
            mul[i][j]+=A[i][k]*B[k][j];    
        }    
    }    
}    
   
for(i=0;i<r;i++)    
{    
    printf("\n[");
    for(j=0;j<c;j++)    
    {    
        printf("%d\t",mul[i][j]);    
    }    
printf("]\n");    
}    
return 0;  
}  
```
>**Examples:**

In case of 2X2 matrices
||A||
|----|---|---|
|A[0][0]|A[0][1]
| A[1][0]|A[1][1]|


||B||
|----|---|---|
|B[0][0]|B[0][1]
| B[1][0]|B[1][1]|

>**Resultant Matrix:**

||A*B||
|----|---|---|
|A[0][0]*B[0][0]+A[0][1]*B[1][0]|A[0][0]*B[0][1]+A[0][1]*B[1][1]
|A[1][0]*B[0][0]+A[1][1]*B[1][0]|A[1][0]*B[0][1]+A[1][1]*B[1][1]|

