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
                if (n%i==0)
                 return 0;
        }
        return 1;
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
## Write a program to implement these formulae of permutations and combinations.
Number of permutations of n objects taken r at a time: p(n, r) = n! / (n-r)!
Number of combinations of n objects taken r at a time is: c(n, r) = n! / (r! * (n-r)!) = p(n, r) /r!
```
#include <stdio.h>
int factorial(int n);
int perm(int num,int r);
int comb(int numb,int r);
int main(){
        int number,r;
        printf("Enter a number and r");
        scanf("%d%d",&number,&r);
        printf("%d\n",perm(number,r));
        printf("%d\n",comb(number,r));
}
int factorial(int n){
        int fact=1;
        for(int i=1;i<=n;i++){
                fact=fact*i;
        }
        return fact;
       }
int perm(int num,int r){
        int p;
        p=factorial(num)/factorial(num-r);
         return p;
}
int comb(int numb,int r){
        int c;
        c=perm(numb,r)/factorial(r);
        return c;
}
output
Enter a number and r 5
3
 permutation 60
 combination 10
```
## Program to convert decimal number to roman number
```
#include <stdio.h>
int roman(int,int,char);
int main(void){
        int number;
        printf("Enter a number");
        scanf("%d",&number);
      if(number>=1000)
              number=roman(number,1000,'M');
      if(number>=500)
              number=roman(number,500,'D');
      if(number>=100)
              number=roman(number,100,'C');
      if(number>=50)
              number=roman(number,50,'L');
      if(number>=10)
              number=roman(number,10,'X');
      if(number>=5)
       number=roman(number,5,'V');
      if(number>=1)
              roman(number,1,'I');
      printf("\n");
      return 0;
}
int roman(int n,int k,char ch){
        while(n>=k){
                printf("%c",ch);
        n=n-k;
        }
        return n;
}
output
Enter a number6
VI
```
## Prime Factors of a given number
```
#include <stdio.h>
int primefact(int);
int main(){
        int num;
        printf("Enter a number");
        scanf("%d",&num);
        primefact(num);
        return 0;
}
int primefact(int n){
        int i=1;
        for(int i=2;n!=1;i++){
                while(n%i==0){
                        printf("%d",i);
                        n=n/i;
                }
        }
}
output
Enter a number60
2235
```
##  Write a function that inputs a number and prints the multiplication table of that number
```
#include <stdio.h>
int Multiplication(int n);
int main(){
        int number;
        printf("Enter a number");
        scanf("%d",&number);
        Multiplication(number);
}
int Multiplication(int n){
        for(int i=1;i<=10;i++){
                printf("%d*%d=%d\n",n,i,n*i);
        }
}
output
Enter a number4
4*1=4
4*2=8
4*3=12
4*4=16
4*5=20
4*6=24
4*7=28
4*8=32
4*9=36
4*10=40
```
## Armstrong
```
#include <stdio.h>
int cubesum(int n);
int printarmstrong(int n);
int main(){
        int number;
        printf("Enter a number");
        scanf("%d",&number);
        cubesum(number);
        printarmstrong(number);
}
int cubesum(int num){
        int digit,rem=0;
        while(num>0){
        digit=num%10;
        rem=rem+digit*digit*digit;
        num=num/10;
}
return rem;
}
int printarmstrong(int n){
        if(n==cubesum(n)){
                printf("It is an armstrong number");
        }
        else{
        printf("Not an armstrong number");
}
return 0;
}
output
enter a number 152
not an armstrong number
```
## Write a function cubesum() that accepts an integer and returns the sum of the cubes of individual digits of thatnumber. Use this function to make functions PrintArmstrong() and isArmstrong () to print Armstrong numbersand to find whether a number is an Armstrong number.
```
#include <stdio.h>
int cubesum(int n);
int Armstrong(int n);
int printarmstrong();
int main(){
        int number;
        printf("Enter a number");
        scanf("%d",&number);
        if(isArmstrong(number))
                printf("%d is an Armstrong Number",number);
        else
           printf("%d is not an armstrong number",number);
        printarmstrong();
}
int cubesum(int num){
        int digit,rem=0;
        while(num>0){
digit=num%10;
        rem=rem+digit*digit*digit;
        num=num/10;
}
return rem;
}
int isArmstrong(int n){
        return(n==cubesum(n));
}
int printarmstrong(){
        printf("\nArmstrong numbers between 1 to 1000 are:\n");
        for(int i=1;i<1000;i++){
                if(isArmstrong(i))
                        printf("%d\t",i);
        }

printf("\n");
}
output
Enter a number153
153 is an Armstrong Number
Armstrong numbers between 1 to 1000 are:
1	153	370	371	407	
```
## Write a function prodDigits () that inputs a number and returns the product of digits of that number.
```
#include <stdio.h>
int prodDigits(int n);
int main(){
        int number;
        printf("Enter a number");
        scanf("%d",&number);
        printf("%d",prodDigits(number));
        return 0;
  }
int prodDigits(int n){
        int prod=1;
        while(n>0){
     int digit=n%10;
      prod=prod*digit;
      n=n/10;
     }
        return prod;
}
output
Enter a number24
8
```
##  If all digits of a number n are multiplied by each other repeating with the product, the one digit number obtained at last iscalled the multiplicative digital root of n. The number of times digits need to be multiplied to reach one digit is called themultiplicative persistence of n.
```
#include <stdio.h>
int proDigits(int num){
        int digit,rem=1;
        while(num>0){
        digit=num%10;
        rem=rem*digit;
        num/=10;
        }
        return rem;
}
int main(){
        int number;
        int step=0;
        printf("Enter a number");
        scanf("%d",&number);
        int original=number;
        while(number>=10){
    number=proDigits(number);
        step++;
        }
        printf("Multiplicative Digital root =%d\n",number);
        printf("Multiplicative persistence =%d\n",step);
        return 0;
}
output
Enter a number25
Multiplicative Digital root =0
Multiplicative persistence =2
```
## A number is called perfect if the sum of proper divisors of that number is equal to the number. For example 28 is aperfect number, since 1+2+4+7+14 =28. Write a program to print all the perfect numbers in a given range.
```
#include <stdio.h>
int perfect(int m,int n);
int main(){
int m,n;
printf("Enter and m and n values:");
scanf("%d%d",&m,&n);
 perfect(m,n);
}
int perfect(int m,int n){
printf("Perfect squares between these numbers are\n");
        for(int i=m;i<=n;i++){
                int sum=0;
                for(int j=1;j<i;j++){
                        if(i%j==0){
                                sum+=j;
                        }
                }
                  if(sum==i)
                        printf("%d ",i);
        }
}


output
Enter and m and n values:1
1000
Perfect squares between these numbers are
 6 28 496
```
## function to convert inches to cms  first srgument should be length should be connverted second argument should be char(i or c)denoting the measuremet unit of the length given in the first argumengt tell me how to do 
```
#include <stdio.h>
float convert(float length,char unit){
        if(unit=='i'|| unit=='I'){
                return length*2.54;
        }
        else if(unit=='c'||unit=='C'){
                return length/2.54;
        }
        else{
                printf("Invalid unit.enter i or c");
                return -1;
        }
}
int main(){
        float length,result;
        char unit;
        printf("Enter length:");
      scanf("%f",&length);

        printf("Enter unit");
        scanf(" %c",&unit);

        result=convert(length,unit);
        if(result !=-1){
        printf("%.2f",result);
}
return 0;
}
output
Enter length:24
Enter unit i
60.96
```

       

