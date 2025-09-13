```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=0;
int maxlen=0;
int minlen=999;
int maxstart=0;
int minstart=0;
int wordstart=0;
int i=0;
while(1){
if(str[i]!=' ' && str[i]!='\0' && str[i]!='\n'){
        if(len==0)
                wordstart=i;
        len++;
}
else{
        if(len>0){
        if(len>maxlen){
                  maxlen=len;
                  maxstart=wordstart;
          }
          if(len<minlen){
                  minlen=len;
                  minstart=wordstart;
          }
          len=0;
        }
        if(str[i]=='\0')
                break;
}
i++;
}
printf("Longest word\n");
for(int i=maxstart;i<maxstart+maxlen;i++){
        printf("%c",str[i]);
}
printf("%d",maxlen);
printf("\n Smallest word\n");
for(int i=minstart;i<minstart+minlen;i++){
        printf("%c",str[i]);
}
printf("%d",minlen);
}
output
Enter a stringthe sun rises in the east
Longest word
rises5
Smallest word
in2
```
