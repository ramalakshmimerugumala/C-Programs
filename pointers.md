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
