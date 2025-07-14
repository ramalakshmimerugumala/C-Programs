## check wheather the number is divisible by 3 or 5 but not both
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
## Check wheather the entered character is alphabet or not using logical operator
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
