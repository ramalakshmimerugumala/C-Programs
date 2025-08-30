## 1. Write a program to clear 4th and 2nd bit of a number input by user
```c
#include <stdio.h>
int main(){
unsigned int num;
printf("Enter a number");
scanf("%i",&num);
num&=~((1<<2)|(1<<4));
printf("%u",num);
}
output
Enter a number0x53
After clearing 4th and 2nd bit=67
```
## 2.Write a program to set 5th ,3rd &1st bit of the number by user
```c
#include <stdio.h>
int main(){
unsigned int num;
printf("Enter a number");
scanf("%i",&num);
num|=((1<<1)|(1<<3)|(1<<5));
printf("%u",num);
}
output
Enter a number0x53
123
```
## 3.Write a program to find the state of 3rd and 2nd bit input by user
```c
#include <stdio.h>
int main(){
unsigned int num;
printf("Enter a number");
scanf("%i",&num);
if(num&(1<<2))
        printf("2nd bit set to 1\n");
else
        printf("2nd bit is clear  0\n");
if(num&(1<<3))
        printf("3rd bit set to 1\n");
else
        printf("3rd bit is clear\n");
}
output
Enter a number0x54
2nd bit set to 1
3rd bit is clear
```
## 4. Write  a program to toggle 7th,5th,4th, and 1st by taking the user input
```c
#include <stdio.h>
int main(){
unsigned int num;
printf("Enter a number");
scanf("%i",&num);
num ^=((1<<7)|(1<<5)|(1<<4)|(1<<1));
printf("After toggling=%u",num);
}
output
Enter a number0x53
After toggling=225
```
## 5 Write a program to count number of set bits in a number
```c
#include <stdio.h>
int main(){
unsigned int num;
printf("Enter a number");
scanf("%i",&num);
int count=0;
while(num){
        if(num&1)
                count ++;
         num>>=1;
}
printf("count=%d\n",count);
}
output
Enter a number0x53
count=4
```
## 6.write a program to check wheather the number is power of 2 or not using biwise
```c
#include <stdio.h>
int main(){
int num;
printf("Enter a number");
scanf("%d",&num);
if(num>0&&(num&(num-1))==0){
        printf("Power of 2");
}
else{
        printf("Not a power of 2");
}
}
output
Enter a number128
Power of 2
```
## 7.Write a program divide by 2
```c
#include <stdio.h>
int main(){
int num;
printf("Enter a number");
scanf("%d",&num);
int res;
res=num>>1;
printf("%d",res);
}
output
Enter a number2
1
```
## 8. write a program to print binary digits of a number by user input
```c
 hexa decimal

#include <stdio.h>
int main(){
unsigned int num;
printf("Enter a number");
scanf("%i",&num);
for(int i=31;i>=0;i--){
        int bit=(num>>i)&1;
        printf("%u",bit);
        if(i%4==0)
                printf("\n");
}
printf("Hexadecimal %x\n",num);
}
output
Enter a number0x53
0000
0000
0000
0000
0000
0000
0101
0011
Hexadecimal 53
```
using int
```c
#include <stdio.h>
int main(){
int num;
printf("Enter a number");
scanf("%d",&num);
for(int i=31;i>=0;i--){
        int bit=(num>>i)&1;
        printf("%d",bit);
}
printf("\n");
}
output
Enter a number6
00000000000000000000000000000110
```
## 9. write a program to swap lower and higher nibbles of a number by user input
```c
include <stdio.h>
int main(){
unsigned int num,result;
printf("Enter a number");
scanf("%i",&num);
result=((num&0x0F)<<4)|((num&0xF0)>>4);
printf("orginal num=0x%x\n",num);
printf("swapped number=0x%x\n",result);
}
output
Enter a number0x53
orginal num=0x53
swapped number=0x35
```
