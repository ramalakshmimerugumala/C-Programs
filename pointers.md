## Write a Program to print the value and address of elements of an array using pointers notation
```
#include <stdio.h>
int main(){
int arr[5]={3,6,1,7,4};
int *ptr=arr;
for(int i=0;i<5;i++){
        printf("%d\t",*(ptr+i));
        printf("%p\n",(ptr+i));
}
}
output
3	0x7ffd825ef7e0
6	0x7ffd825ef7e4
1	0x7ffd825ef7e8
7	0x7ffd825ef7ec
4	0x7ffd825ef7f0
```
##  Write a program to print the value of array elements using pointers and subscript notation
```
#include <stdio.h>
int main(){
int arr[5]={7,8,4,3,9};
int *ptr=arr;
printf("Using pointer notation\n");
for(int i=0;i<5;i++)
printf("Values=%d\t",*(ptr+i));
printf("\nUsing subscript notation\n");
for(int i=0;i<5;i++)
printf("Values=%d\t",ptr[i]);
}
output
Using pointer notation
Values=7	Values=8	Values=4	Values=3	Values=9	
Using subscript notation
Values=7	Values=8	Values=4	Values=3	Values=9
```
## Write a program to print the value and address of array elements by subscripting a pointer variable
```
#include <stdio.h>
int main(){
int arr[5]={5,3,4,5,1};
int *ptr=arr;
for(int i=0;i<5;i++)
        printf("%d\t%d\t%p\n",i,ptr[i],&ptr[i]);
}
output
0	5	0x7ffdc2223dc0
1	3	0x7ffdc2223dc4
2	4	0x7ffdc2223dc8
3	5	0x7ffdc2223dcc
4	1	0x7ffdc2223dd0
```
##  Program to understand the difference between a to an integer and a pointer to an array of integers
```
#include <stdio.h>
int main(){
int a=10;
printf("Value=%d\n",a);
printf("Address=%p\n",&a);
int arr[5]={7,4,7,3,2};
int *ptr=arr;
printf("\n Using pointer to int\n");
for(int i=0;i<5;i++){
printf("Values using pointer=%d\t",*(ptr+i));
printf("Address using pointer=%p\n",(ptr+i));
}
int(*p)[5]=&arr;
printf("\n Using array pointer\n");
for(int i=0;i<5;i++){
printf("Values using array pointer %d\t",(*p)[i]);
printf("Address using Array pointer %p\n",&(*p)[i]);
}
}
output
Value=10
Address=0x7ffc13ab3f34

 Using pointer to int
Values using pointer=7	Address using pointer=0x7ffc13ab3f50
Values using pointer=4	Address using pointer=0x7ffc13ab3f54
Values using pointer=7	Address using pointer=0x7ffc13ab3f58
Values using pointer=3	Address using pointer=0x7ffc13ab3f5c
Values using pointer=2	Address using pointer=0x7ffc13ab3f60

 Using array pointer
Values using array pointer 7	Address using Array pointer 0x7ffc13ab3f50
Values using array pointer 4	Address using Array pointer 0x7ffc13ab3f54
Values using array pointer 7	Address using Array pointer 0x7ffc13ab3f58
Values using array pointer 3	Address using Array pointer 0x7ffc13ab3f5c
Values using array pointer 2	Address using Array pointer 0x7ffc13ab3f60
```
##  call by value
```
#include <stdio.h>
int callbyvalue(int x,int y);
int main(){
        int m,n;
        printf("Enter a number");
        scanf("%d",&m);
        printf("Enter a number2");
        scanf("%d",&n);
        callbyvalue(m,n);
        printf("%d%d\n",m,n);
}
int callbyvalue(int x,int y){
        x=6;
        y=7;
        x++;
        y++;
        printf("%d%d\n",x,y);
}
output
Enter a number14
Enter a number21
x=7 y=8
m=4 n=1

```
## call by reference
```
#include <stdio.h>
int callref(int *x,int *y);
int main(){
int a=5,b=8;
printf("a=%d,b=%d\n",a,b);
callref(&a,&b);
printf("a=%d,b=%d\n",a,b);
return 0;
}
int callref(int *x,int *y){
        (*x)++;
        (*y)++;
        printf("*p=%d,*q=%d\n",*x,*y);
}
output
a=5,b=8
*p=6,*q=9
a=6,b=9
```
##  Returning more than one value from a function using call by reference*
```
#include <stdio.h>
int *ret(int a,int b,int *sum,int *prod,int *diff);
int main(){
int a,b;
int sum,prod,diff;
printf("Enter a number");
scanf("%d",&a);
printf("Enter a number");
scanf("%d",&b);
int *ptr;
ret(a,b,&sum,&prod,&diff);
printf("sum=%d prod=%d diff=%d",sum,prod,diff);

}
int *ret(int a,int b,int *sum,int *prod,int *diff){
        *sum=a+b;
        *prod=a*b;
        *diff=a-b;
}
output
Enter a number5
Enter a number2
sum=7 prod=10 diff=3
```
##  Implement a function that returns the length of a string using pointers
```
#include <stdio.h>
int lenstr(char *str);
int main(){
 char str[100];
 printf("Enter a string");
 scanf("%s",str);
 int length=lenstr(str);
 printf("Length of a string=%d\n",length);
}
int lenstr(char *str){
        int count=0;
        while(*str!='\0'){
                count++;
                str++;
        }
        return count;
}
output
Enter a stringmoon
Length of a string=4
```
## Develop a function to reverse a string in place using pointers
```
#include <stdio.h>
char rev(char *str);
int main(){
char str[100];
printf("Enter a string");
scanf("%s",str);
rev(str);
printf("%s",str);
}
char rev(char *str){
        char *start=str;
        char *end=str;
        while(*end!='\0'){
                end++;
        }
        end--;
        while(start<end){
                char temp=*start;
                *start=*end;
                *end=temp;
                start++;
                end--;
        }
}
output
Enter a string Rama
amaR
```
##  Implement a function to copy one string into another using pointers, without using any standard library functions
```
#include <stdio.h>
char copy(char *str1,char *str2);
int main(){
char str1[100];
char str2[100];
printf("Enter a string");
scanf("%s",str1);
copy(str1,str2);
printf("Copied to string 2 %s",str2);
}
char copy(char *str1,char *str2){
        while(*str1!='\0'){
                *str2=*str1;
                str1++;
                str2++;
        }
        *str2!='\0';
}
output
Enter a stringhello
Copied to string 2 hello
```
## Write a program that calculates the sum of all elements in an integer array using pointer arithmetic
```
#include <stdio.h>
int main(){
int sum=0;
int arr[5]={1,2,3,4,5};
int *ptr=arr;
for(int i=0;i<5;i++){
        printf("%d",*(ptr+i));
        sum=sum+*(ptr+i);
}
printf("\n Sum of elements in the array=%d",sum);
}
output
12345
Sum of elements in the array=15
```
## Create a function that swaps two numbers using pointers
```
#include <stdio.h>
int swap(int *x,int *y);
int main(){
int x=10;
int y=5;
swap(&x,&y);
printf("x=%d\n",x);
printf("y=%d\n",y);
}
int swap(int *x,int *y){
int temp=*x;
    *x=*y;
    *y=temp;
}
output
x=5
y=10
```
## . Write a program to find the maximum and minimum elements in an array using pointers
```
#include <stdio.h>
int main(){
int arr[5]={2,4,6,7,9};
int max=arr[0];
int min=arr[0];
int (*ptr)[5];
ptr=&arr;
for(int i=0;i<5;i++){
        if((*ptr)[i]>max){
                max=(*ptr)[i];
        }
        else if((*ptr)[i]<min){
                min=(*ptr)[i];
        }
}
printf("Maximum elemnt=%d",max);
printf("Minimum element=%d",min);
}
output
Maximum elemnt=9Minimum element=2
```
## Write a program to find the factorial of a given number using pointers
```
#include <stdio.h>
int main(){
int n;
printf("Enter a number");
scanf("%d",&n);
int fact=1;
int *ptr;
ptr=&fact;
for(int i=1;i<=n;i++){
        *ptr=*ptr*i;
}
printf("Factorial of a number is %d",*ptr);
}
output
Enter a number4
Factorial of a number is 24
```
## Write a program to count the number of vowels and consonants in a string using a pointer
```
#include <stdio.h>
int main(){
char str[100];
int vowel=0;
int consonant=0;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
char *ptr;
ptr=str;
while(*ptr!='\0'){
        if((*ptr=='A'||*ptr=='E'||*ptr=='I'||*ptr=='O'||*ptr=='U')||(*ptr=='a'||*ptr=='e'||*ptr=='i'||*ptr=='o'||*ptr=='u')){
          vowel++;
        }
        else if((*ptr>='a'&&*ptr<='z')||(*ptr>='A' && *ptr<='Z')){
                consonant++;
        }
          ptr++;
}
printf("vowel count=%d",vowel);
printf("Consonant count=%d",consonant);
}
output
 Enter a stringrama
vowel count=2Consonant count=2
```
## Write a program to demonstrate how a function returns a pointer.
```
#include <stdio.h>
int prod(int x,int y,int *prod);
int main(){
int m,n;
printf("Enter a number1");
scanf("%d",&m);
printf("Enter number 2");
scanf("%d",&n);
int result;
prod(m,n,&result);
printf("%d",result);
}
int prod(int x,int y,int *prod){
        *prod=x*y;
}
output
Enter a number15
Enter number 23
15
```
## Write a program to find the largest element using Dynamic Memory Allocation.
```
#include <stdio.h>
#include <stdlib.h>
int main(){
int n;
printf("Enter the number of elements:");
scanf("%d",&n);
int *ptr;
ptr=(int *)malloc(n*sizeof(int));
if(ptr==NULL){
        printf("Memory is not allocated");
}
printf("Enter elements");
for(int i=0;i<n;i++){
        scanf("%d",(ptr+i));
}
int max=ptr[0];
for(int i=1;i<n;i++){
if(ptr[i]>max){
                max=ptr[i];
}
}
printf("Largest element is =%d\n",max);
free(ptr);
}
output
Enter the number of elements:5
Enter elements1 2 3 4 5
Largest element is =5
```
## Logic to search an element in an array using pointers
```
#include <stdio.h>
int main(){
int arr[5]={1,2,3,4,5};
int *ptr;
ptr=arr;
int search;
int found=0;
printf("Enter search element");
scanf("%d",&search);
for(int i=0;i<5;i++){
if((*ptr+i)==search){
        printf("Search element is found");
        found=1;
        break;
}
}
if(found==0){
printf("Element is not found");
}
}
output
Enter search element9
Element is not found
```
## Write a program to multiply two matrix using pointers
```
#include <stdio.h>
int main(){
int n,m;
int arr1[100][100];
int arr2[100][100];
int result[100][100]={0};
printf("Enter the size of rows and coulmns of 1st matrix");
scanf("%d %d",&n,&m);
printf("Enter the elments in the matrix1");
for(int i=0;i<n;i++){
for(int j=0;j<m;j++){
scanf("%d",(*(arr1+i)+j));
 }
}
int p,q;
printf("Enter the size of rows and columns in the array 2");
scanf("%d %d",&p,&q);
printf("Enter the elements in the array2");
for(int i=0;i<p;i++){
for(int j=0;j<q;j++){
scanf("%d",(*(arr2+i)+j));
 }
}
printf("Matrix multiplication\n");
for(int i=0;i<n;i++){
        for(int j=0;j<q;j++){
                for(int k=0;k<m;k++){
                        *(*(result+i)+j)+=*(*(arr1+i)+k)* *(*(arr2+k)+j);
                }
        }
}
for(int i=0;i<n;i++){
  for(int j=0;j<m;j++){
                printf("%d ",*(*(result+i)+j));
        }
        printf("\n");
}
}
output
Enter the size of rows and coulmns of 1st matrix3 3 
Enter the elments in the matrix11 2 3 4 5  6 7 8 9
Enter the size of rows and columns in the array 23 3
Enter the elements in the array21 2 3 4 5 6 7 8 9 
Matrix multiplication
30 36 42 
66 81 96 
102 126 150
```
## write a program to concatenate two strings using pointers
```
#include <stdio.h>
#include <string.h>
int main(){
char str1[100];
char str2[100];
printf("Enter string 1");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';
printf("Enter string 2");
fgets(str2,sizeof(str2),stdin);
str2[strcspn(str2,"\n")]='\0';
char *ptr=str1;
char *ptr2=str2;
while(*ptr!='\0'){
        ptr++;
}
while((*ptr++=*ptr2++)){
}
printf("%s",str1);
}
output
Enter string 1hello
Enter string 2world
helloworld
```
## Program to access dynamically allocated memory as a 1d array
```
#include <stdio.h>
#include <stdlib.h>
int main(){
int n;
printf("Enter the size");
scanf("%d",&n);
int (*ptr)[n];
ptr=malloc(sizeof(*ptr));
if(ptr==NULL){
        printf("Memory is not allocated");
}
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
 scanf("%d",&(*ptr)[i]);
}
for(int i=0;i<n;i++){
 printf("%d ",(*ptr)[i]);
}
free(ptr);
}
output
Enter the size5
Enter the elements in the array1 2 3 4 5
1 2 3 4 5
```
## Program to access dynamically allocate a 2-D array using a pointer to an array
```
#include <stdio.h>
#include <stdlib.h>
int main(){
int n,m;
printf("Enter the size of row");
scanf("%d",&n);
printf("Enter the size of the column");
scanf("%d",&m);
int (*ptr)[m];
ptr=malloc(n*sizeof(*ptr));
if(ptr==NULL){
        printf("Memory is not allocated");
}
printf("Enter the elements in the matrix");
for(int i=0;i<n;i++){
        for(int j=0;j<m;j++){
                scanf("%d",&ptr[i][j]);
 }
}
for(int i=0;i<n;i++){
        for(int j=0;j<m;j++){
                printf("%d",ptr[i][j]);
        }
        printf("\n");
}
free(ptr);
}
output
Enter the size of row3
Enter the size of the column4
Enter the elements in the matrix1 2 3 4 5 6 7 8 9 2 3 4
1234
5678
9234
```
## Write a program to print array of pointer
```
Using subscript and pointer
#include <stdio.h>
int main(){
int arr[5]={1,2,3,4,5};
int (*ptr)[5];
ptr=&arr;
for(int i=0;i<5;i++){
  printf("value= %d\t",(*ptr)[i]);
  printf("Address= %p\n",&(*ptr)[i]);
  printf("values=%d\t",*(*ptr+i));
  printf("Address=%p\n",(*ptr+i));
}
}
output
value= 1	Address= 0x7ffc5da53640
values=1	Address=0x7ffc5da53640
value= 2	Address= 0x7ffc5da53644
values=2	Address=0x7ffc5da53644
value= 3	Address= 0x7ffc5da53648
values=3	Address=0x7ffc5da53648
value= 4	Address= 0x7ffc5da5364c
values=4	Address=0x7ffc5da5364c
value= 5	Address= 0x7ffc5da53650
values=5	Address=0x7ffc5da53650

2d array
#include <stdio.h>
int main(){
int arr[2][3]={{1,2,3},
            {4,5,6}};
int (*ptr)[3];
ptr=arr;
for(int i=0;i<2;i++){
        for(int j=0;j<3;j++){
                printf("Value=%d\t",ptr[i][j]);
                printf("Address=%p\n",&ptr[i][j]);
                printf("values=%d\t",*(*(ptr+i)+j));
                printf("Address=%p\n",(*(ptr+i)+j));
        }
}
}
Value=1	Address=0x7fff1e5c64e0
values=1	Address=0x7fff1e5c64e0
Value=2	Address=0x7fff1e5c64e4
values=2	Address=0x7fff1e5c64e4
Value=3	Address=0x7fff1e5c64e8
values=3	Address=0x7fff1e5c64e8
Value=4	Address=0x7fff1e5c64ec
values=4	Address=0x7fff1e5c64ec
Value=5	Address=0x7fff1e5c64f0
values=5	Address=0x7fff1e5c64f0
Value=6	Address=0x7fff1e5c64f4
values=6	Address=0x7fff1e5c64f4
```
## Program to invoke a function using function pointer
```
#include <stdio.h>
int sum(int,int);
int main(){
int s=0;
int (*ptr)(int,int)=sum;
s=(*ptr)(1,2);
printf("Sum=%d",s);
}
int sum(int a,int b){
        return a+b;
}
```
## . Program to send a function ‘s address as an argument to other function
```
#include <stdio.h>
void sum(int a,int b){
        printf("sum=%d\n",a+b);
}
void sub(int a ,int b){
        printf("sub=%d\n",a-b);
}
void display(void (*fptr)(int,int)){
        fptr(5,1);
}
void main(){
        display(sum);
        display(sub);
}
```
##  Program to pass a pointer containing functions arguments address as an argument
```
#include <stdio.h>
void sum(int *a,int *b){
        printf("sum=%d\n",*a+*b);
}
void sub(int *a,int *b){
        printf("sub=%d\n",*a-*b);
}
void display(void (*fptr)(int*,int*),int *x,int *y){
        fptr(x,y);
}
void main(){
        int num1=5;
        int num2=4;
        display(sum,&num1,&num2);
        display(sub,&num1,&num2);
}
output
sum=9
sub=1
```














