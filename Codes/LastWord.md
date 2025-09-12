```
#include <string.h>
int main(){
char str[100];
int count=0;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
int end=len-1;
int start;
for(int i=len-1;i>=0;i--){
        if(str[i]==' '){
        start=i+1;
        break;
        }
        if(i==0)
                start=0;
        }
for(int i=start;i<=end;i++){
        printf("%c",str[i]);
        count++;
}
printf("%d",count);
}
output
Enter a stringhi i am learning
learning8
```
