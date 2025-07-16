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

