```
#include <string.h>
int myatoi(char str[]){
        int i=0,sign=1,num=0;
        if(str[i]=='-'){
                sign=-1;
                i++;
        }
        else if(str[i]=='+'){
                i++;
        }
        for(;str[i]!='\0';i++){
                num=num*10+(str[i]-'0');
        }
        return num*sign;
}
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int result=myatoi(str);
printf("%d\n",result);
output
Enter a string-4567
-4567
```
