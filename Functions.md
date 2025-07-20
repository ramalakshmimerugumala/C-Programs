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
## 7.
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



