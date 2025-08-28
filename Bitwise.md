## 1. Write a program to clear 4th and 2nd bit of a number input by user
```
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
```
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
```
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
```
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
```
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
