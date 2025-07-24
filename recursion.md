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
