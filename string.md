## substring
```
#include <stdio.h>
#include <string.h>
int main(){
char ch1[100];
char ch2[100];
printf("Enter a string");
scanf("%s",ch1);
printf("Enter a string2");
scanf("%s",ch2);
if(strstr(ch1,ch2)){
        printf("String found");
}
else{
        printf("String not found");
}
}
output
Enter a stringhello
Enter a string2ll
String found
```
## Extract a substring from a string from the start index and end index
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
int start,end;
char sub[100];
int j=0;
int len=strlen(str);
printf("Enter a string");
fgets(str,sizeof(str),stdin);
printf("Enter start index");
scanf("%d",&start);
printf("Enter end index");
scanf("%d",&end);
for(int i=start;i<=end && str[i]!='\0';i++){
  sub[j++]=str[i];
}
sub[j]='\0';
printf("Substrings in a string %s",sub);
}
output
Enter a stringhello
Enter start index0
Enter end index3
Substrings in a string hell
```
## Program to remove duplicates in a given string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
int len=strlen(str);
for(int i=0;i<len;i++){
  for(int j=i+1;j<len;){
          if(str[j]==str[i]){
                  for(int k=j;k<len;k++){
                          str[k]=str[k+1];
                  }
                  len--;
         }
          else{
                  j++;
                          j++;
          }
  }
}
printf("%s\n",str);
}
output
Enter a stringrama
ram
```
## 

