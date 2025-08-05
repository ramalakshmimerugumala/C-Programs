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
## 
