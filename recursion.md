## Factorial
```
#include <stdio.h>
int factorial(int num);
int main(){
        int num;
        printf("Enter a number");
        scanf("%d",&num);
        printf("factorial of a number is %d",factorial(num));
}
int factorial(int num){
        if(num==1){
                return 1;
        }
        return num*factorial(num-1);
}
output
Enter a number5
factorial of a number is 120
```
## Fibnocii
```
#include <stdio.h>
int fibnoci(int n);
int main(){
        int terms;
        printf("Enter how many terms u want");
        scanf("%d",&terms);
        for(int i=0;i<terms;i++){
        printf("%d ",fibnoci(i));
        }
        return 0;
}
int fibnoci(int n){
        if(n==0){
                return 0;
        }
        if(n==1){
                return 1;
        }
        else{
       return fibnoci(n-1)+fibnoci(n-2);
        }
}
output
Enter how many terms u want10
0 1 1 2 3 5 8 13 21 34 
```
##  Reverse of an array using recursion
```
#include <stdio.h>
int reverse(int arr[],int n);
int main(){
int n;
int arr[100];
printf("Enter the size of an array");
scanf("%d",&n);
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
printf("Reversed array");
reverse(arr,n-1);
}
int reverse(int arr[],int n){
        if(n<0)
                return;
        printf("%d ",arr[n]);
        reverse(arr,n-1);
}
output
Enter the size of an array5
Enter the elements in the array1 2 3 4 5
Reversed array5 4 3 2 1
```
