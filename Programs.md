## 1. check wheather the number is divisible by 3 or 5 but not both
```
#include <stdio.h>
int main(){
int num;
printf("Enter a number:\n");
scanf("%d",&num);
if((num%3==0||num%5==0)&&num%15!=0){
        printf("It is divisible by 3 or 5 but not both");

}
else{
        printf("The numebr is either divisible by both or neither");
}
}

Output
Enter a number:
3
It is divisible by 3 or 5 but not both
```
## 2.Check wheather the entered character is alphabet or not using logical operator
```
#include <stdio.h>
int main(){
char ch;
printf("Enter a character:");
scanf("%c",&ch);
if(ch=='A'||ch >='Z'||ch=='a'||ch >='z'){
        printf("It is an alphabet");
}
else{
        printf("It is not an alphabet");
}
}
output
Enter a character:#
It is not an alphabet
```
## 3. Write the program to count the no of words in a string
```
#include <stdio.h>
int main(){
char str[100];
int i=0;
int wordcount=0;
printf("Enter a string ");
fgets(str,sizeof(str),stdin);
while(str[i]!='\0'){
        if((str[i]!=' '&&str[i]!='\n')&&
         (str[i+1]==' ' ||str[i+1]=='\n'||str[i+1]=='\0')){
        wordcount++;
        }
i++;
}
printf("No.of words in a  string %d",wordcount);
}
output
Enter a string moon sun
No.of words in a  string 2
``` 
## 4 Count the no of digits in a number
```
#include <stdio.h>
int main(){
        int num;
        int rem=0;
        int count=0;
    printf("Enter the number");
    scanf("%d",&num);
    while(num>0){
            int digit=num%10;
            int rem=rem+digit;
            num=num/10;
            count ++;
    }
    printf("Count the no of digits in a given number %d",count);
}
output
Enter the number345
Count the no of digits in a given number 3
```
## 5 reverse order with difference 2
```
#include <stdio.h>
int main(){
for(int i=10;i>=1;i=i-2){
        printf("%d ",i);
}
}
output
10 8 6 4 2 
```
## 6 sum of the terms
```
#include<stdio.h>
int main(){
        int n,sum=0;
        int term=1;
        printf("Enter the term");
        scanf("%d",&n);
        for(int i=0;i<n;i++){
           sum=sum+term;
           term=term+i;
        }
        printf("%d ",sum);
}
output
Enter the term5
15 
```
## 7 sum of the digits upto single term
```
#include <stdio.h>
int main(){
int number;
    int sum=0;
    int var;
printf("Enter a number");
scanf("%d",&number);
var=number;
while(number>0){
        int digit=number%10;
         sum=sum+digit;
        number=number/10;
}
printf("Sum of the digits in a number is %d",sum);
while(sum>10){
number=sum;
        sum=0;
        while(number>0){
                int digit=number%10;
                sum=sum+digit;
                number=number/10;
        }
}
printf("\nFinal single digit %d\n",sum);
}
output
enter a number 12345
final single digit 6
```
##  Program to get difference of two dates in years, months, days*/
```
#include <stdio.h>
int main(){
int d1,m1,y1;
int d2,m2,y2;
int daysInMonth[]={31,28,31,30,31,30,31,31,30,31,30,31};
printf("enter date1(dd mm yyyy)");
scanf("%d%d%d",&d1,&m1,&y1);
printf("Enter date2(dd mm yyyy)");
scanf("%d%d%d",&d2,&m2,&y2);
if(d2<d1){
        m2=m2-1;
        d2=d2+daysInMonth[(m2-1+12)%12];
}
if(m2<m1){
        y2=y2-1;
        m2=m2+12;
}
int diff_days=d2-d1;
int diff_months=m2-m1;
int diff_years=y2-y1;
printf("difference in days %d",diff_days);
printf("differences in months %d",diff_months);
printf("differences in years %d",diff_years);
}
 output
enter date1(dd mm yyyy)28 02 2020
Enter date2(dd mm yyyy)2 3 2023
difference in days 2
differences in months 0
differences in years 3
```
##   Program to find out the number of notes required for a given amount of money*/ 
```
#include <stdio.h>
int main(){
        int n,choice,notes;
        printf("Enter the amount");
        scanf("%d",&n);
        printf("Enter the value of notes which u begin from");
        scanf("%d",&choice);
        switch(choice){
                case 100:
                   notes=n/100;
                printf("Number of 100 rupess notes required %d\n",notes);
                n=n%100;
               case 50:
                notes=n/50;
                printf("Number of 50 rupess notes are requires %d\n",notes);
                n=n%50;
               case 20:
                notes=n/20;
                printf("Number of 20 rupess notes are required %d\n",notes);
                n=n%20;
               case 10:
                notes=n/10;
                printf("Number of 10 rupess notes required %d\n",notes);
                n=n%10;
               case 5:
                notes=n/5;
                printf("Number of 5 rupees notes are requires %d\n",notes);
                n=n%5;
               case 2:
                notes=n/2;
                printf("Number of 2 rupess notes are required %d\n",notes);
                n=n%2;
           case 1:
                notes=n/1;
                printf("Number of 1 rupee notes are requires %d\n",notes);
                n=n%1;
                break;
               default:
                printf("Enter valid value");
                break;
        }
        printf("\n");
}
output
Enter the amount748
Enter the value of notes which u begin from50
Number of 50 rupess notes are requires 14
Number of 20 rupess notes are required 2
Number of 10 rupess notes required 0
Number of 5 rupees notes are requires 1
Number of 2 rupess notes are required 1
Number of 1 rupee notes are requires 1
```
## Write a program to print all prime numbers from 1 to 99.
```
#include <stdio.h>
int main(){
        int n;
        printf("Enter a number");
        scanf("%d",&n);
        for(int n=2;n<=99;n++){
                int isprime=1;
        for(int i=2;i*i<=n;i++){
                if(n%i==0){
                    isprime=0;
                }
        }
         if(isprime){

                        printf("%d ",n);
        }
}
output
Enter a number1
2 3 5 7 11 13 17 19 23 29 31 37 41 43 47 53 59 61 67 71 73 79 83 89 97
```
## Count the frequency of the digit using while loop
```
#include <stdio.h>
int main(){
int n;
int rem=0;
int digit;
int count=0;
printf("Enter a number");
scanf("%d",&n);
printf("Enter a digit");
scanf("%d",&digit);
while(n>0){
        int di=n%10;
        if(di==digit){
        count ++;
        }
        n=n/10;
}
printf("Count of the number %d",count);
}

output
Enter a number23112
Enter a digit1
Count of the number 2
```
## Pascal triangle
```
#include <stdio.h>
int main(){
int n;
printf("Enter the size");
scanf("%d",&n);
for(int i=0;i<n;i++){
        int val=1;
        for(int j=0;j<=i;j++){
                printf("%d",val);
                val=val*(i-j)/(j+1);
        }
        printf("\n");
}
return 0;
}
output
1
11
121
1331
14641
15101051
1615201561
```
##  even or odd using bitwise
```
#include <stdio.h>
int main(){
int num;
printf("Enter a number");
scanf("%d",&num);
if(num&1){
        printf("%d is  an odd number",num);
}
else{
        printf("%d is an eve number",num);
}
}
```
## little endian
```
#include <stdio.h>
int main(){
unsigned int x=1;
unsigned char *ptr=(unsigned char*)&x;
if(*ptr==1){
        printf("Little endian");
}
        else{
                printf("Big Endian");
        }
}
```
## plus one to arary    
```
#include <stdio.h>
#include <math.h>
int main(){
int n;
int arr[100];
printf("Enter the size of an array");
scanf("%d",&n);
int sum=0;
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
    scanf("%d",&arr[i]);
}
int d=pow(10,n-1);
for(int i=0;i<n;i++){
    sum+=arr[i]*d;
    d=d/10;
}
printf("%d",sum+1);
}
output
Enter the size of an array4
Enter the elements in the array1 2 3 4
1235
```
## Array leader
```
#include <stdio.h>
int main(){
int n;
int leader[100];
int k=0;
int arr[100];
printf("Enter the size of an array");
scanf("%d",&n);
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
int right_most=arr[n-1];
leader[k++]=right_most;
for(int i=n-1;i>=0;i--){
        if(arr[i]>right_most){
                right_most=arr[i];
leader[k++]=right_most++;
        }
}
for(int i=k-1;i>=0;i--){
        printf("%d ",leader[i]);
}
}
output
Enter the size of an array6
Enter the elements in the array16 17 4 3 5 2
17 5 2
```
##  Rearrange the values by sign
```
#include <stdio.h>
int main(){
    int n;
    int arr[100];
    int positive[100];
    int negative[100];
    int result[100];
    int pi=0;
    int ni=0;
    printf("Enter the size of an array");
    scanf("%d",&n);
    printf("Enter the elements in the array");
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    for(int i=0;i<n;i++){
        if(arr[i]>=0){
            positive[pi++]=arr[i];
        }
        else{
            negative[ni++]=arr[i];
        }
    }
    int p=0,q=0,i=0;
    while(p<pi &&q<ni){
        result[i++]=positive[p++];
        result[i++]=negative[q++];
    }
    while(p<pi){
        result[i++]=positive[p++];
    }
    while(q<ni){
        result[i++]=negative[q++];
    }
    for(int k=0;k<n;k++){
        printf("%d ",result[k]);
    }
   }
output
Enter the size of an array5
Enter the elements in the array1 3 -3 2 -8
1 -3 3 -8 2
```
## Removing all the occurances
```
#include <stdio.h>
int main(){
    int n;
    int arr[100];
    printf("Enter the size of the array");
    scanf("%d",&n);
    int num;
    printf("Enter the elements in the array");
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    printf("Enter the number to remove");
    scanf("%d",&num);
    int j=0;
    for(int i=0;i<n;i++){
        if(arr[i]!=num){
            arr[j++]=arr[i];
        }
    }
    for(int i=0;i<j;i++){
        printf("%d ",arr[i]);
    }
}
output
Enter the size of the array5
Enter the elements in the array1 2 3 3 4
Enter the number to remove3
1 2 4
```
