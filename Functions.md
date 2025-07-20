##  Implement a function to reverse the elements of an array.
```
#include <stdio.h>
void reverse();
int main(){
        reverse();
}
void reverse(){
int arr[7];
printf("Enter elements");
for(int i=0;i<7;i++){
 scanf("%d",&arr[i]);
}
for(int i=6;i>=0;i--){
        printf("%d ",arr[i]);
}
}
output
Enter elements1
2
3
4
5
6
7
7 6 5 4 3 2 1
  ```
## 2 . Create a function to calculate the average of elements in an array
```
#include <stdio.h>
void average();
int main(){
        average();
}
void average(){
  int arr[5];
  int sum=0;
  printf("Enter elements in the array:");
  for(int i=0;i<5;i++){
          scanf("%d",&arr[i]);
  }
  for(int i=0;i<5;i++){
          sum=sum+arr[i];
  }
          int average=sum/5;
          printf("Average =%d",average);
}
output
Enter elements in the array:1
2
3
4
5
Average =3
```
## 3. Call by value
```
#include <stdio.h>
void fun(int,int);
void main(){
        int x=8,y=6;
        fun(x,y);
        printf("x=%d y=%d",x,y);
}
void fun(int x,int y){
         x=5;
         y=7;
printf("x=%d y=%d",x,y);
}
output
x=5 y=7x=8 y=6
```
## 4.Call by reference
```
#include <stdio.h>
void fun();
void main(){
      int x=4;
      int y=7;
        fun(&x,&y);
        printf("x=%d y=%d",x,y);
}
void fun(int *x,int *y){
        *x=5;
        *y=6;
        printf("x=%d y=%d",*x,*y);
}
output
x=5 y=6x=5 y=6
```
## 5 palindrome
```#include <stdio.h>
int reverse(int n);
int ispalindrome(int num);
int main(){
        int number;
        printf("Enter a number");
        scanf("%d",&number);
        if (ispalindrome(number))
                printf("number is palindrome");
        else{
                printf("Number is not plaindrome");
        }
}
int reverse(int n){
        int rev=0;
        int r;
        while(n>0){
 r=n%10;
        rev=rev*10+r;
        n/=10;
        }
        return rev;
}
int ispalindrome(int num){
        if(num==reverse(num))
                return 1;
        else{
                return 0;
        }
}
output
Enter a number323
number is palindrome
```
## 6 prime 
```
#include <stdio.h>
#include <math.h>
int isprime(int n);
int main(){
        int number;
        printf("Enter a number");
        scanf("%d",&number);
        if(isprime(number)){
                printf("Number is prime");
        }else{
                printf("Number is not prime");
        }
}
int isprime(int n){
        int i;
        for(i=2;i<=sqrt(n);i++){
                if (n%2==0){
                 return 0;
                }
                else{
                        return 1;
                }
        }
}
output
Enter a number5
Number is prime
```
## 7.Write a function that inputs two numbers and prints all prime numbers between those numbers.
```
#include <stdio.h>
#include <math.h>
int prime(int num1,int num2);
int isprime(int num);
int main(){
        int num1,num2;
        printf("Enter two numbers:");
        scanf("%d%d",&num1,&num2);
        printf("Prime numbers between %d and %d are",num1,num2);
        prime(num1,num2);
}

int prime(int num1,int num2){
        int i;
        for(i=num1;i<=num2;i++)
                if(isprime(i))
                        printf("%d ",i);
                        }
int isprime(int n)
{
        int i;
        for (int i=2;i<=sqrt(n);i++){
                if(n%i==0){
                        return 0;
                }
        }

                return 1;
}
output
Enter two numbers:2
8
Prime numbers between 2 and 8 are2 3 5 7 
```
## 8.Write a function that converts a decimal number to binary number.
```
#include <stdio.h>
int binary(int);
int main(){
        int n;
        printf("Enter a number");
        scanf("%d",&n);
        int result=binary(n);
        printf("Decima to binary of a number %d",result);
        return 0;
}
int binary(int num){
         int rem,div=0,place=1;
         while(num>0){
         rem=num%2;
         div=div+rem*place;
         num/=2;
         place=place*10;
          }
         return div;
}
output
Enter a number12
Decima to binary of a number 1100
```
##9 count the number of Zeroes
```
#include <stdio.h>
int countZeroes(int);
int main(){
        int num;
        printf("Enter a number");
        scanf("%d",&num);
        printf("No of zeroes in binary %d",countZeroes(num));
}
int countZeroes(int num){
        int count =0;
        while(num>0){
   if(num%2==0){
           count ++;
   }
num/=2;
        }

   return count;
}
output
Enter a number12
No of zeroes in binary 2
```
##10 Write a program to raise a floating point number to an integer power(eg. a" where a is floating point number
and n is an integer value.
```
#include <stdio.h>
#include <stdlib.h>
double power(double,int);
int main(){
        double a;
        int num;
        printf("Enter base");
        scanf("%lf",&a);
        printf("Enter Exponential");
        scanf("%d",&num);
        //printf("%.2lf to %d is %.3lf\n",a,num,power(a,num));
        printf("%.4lf",power(a,num));
}
double power(double a,int n){
        double p=1.0;
        if(n==0){
            return 1.0;
          }
        for(int i=1;i<=abs(n);i++){
                p=p*a;
        }
        if (n>0){
                return p;
        }
        else{
        return 1/p;
        }
  }
output
Enter base2.00
Enter Exponential3
8.0000
```
## 11.Write a function that inputs a binary or octal number and converts to decimal number.
```

#include <stdio.h>
#include <math.h>
int binary(long long int num){
        int i=0;
        int digit;
        int rem=0;
        while(num>0){
        digit=num%10;
        rem+=digit*pow(2,i);
        num/=10;
        i++;
        }
        return rem;
}
int octal(int num){
                int i=0;
                int r=0;
            while(num>0){
              int d=num%10;
               r+=d*pow(8,i);
               num=num/10;
               i++;
        }
        return r;
}
int main(){
        int number;
        int choice;
     printf("Options\n");
        printf("1.Binary\n");
        printf("2.Octal\n");
        printf("Enter your choices\n");
        scanf("%d",&choice);
if (choice==1){
        printf("Enter a number");
        scanf("%lld",&number);
        printf("Binary to Decimal is %d\n",binary(number));
}
else if(choice==2){
        printf("Enter a number");
        scanf("%d",&number);
        printf("Octal to Binary  %d\n",octal(number));
}
else{
 printf("Invalid Choice");
}
}
output
Options
1.Binary
2.Octal
Enter your choices
1
Enter a number1011
Binary to Decimal is 11
##another output
Options
1.Binary
2.Octal
Enter your choices
2
Enter a number17
Octal to Binary  15
```


                

