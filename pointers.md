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
## 


