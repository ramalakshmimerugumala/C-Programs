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
## 
