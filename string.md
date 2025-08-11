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
## . Write a program in C to find the length of a string without using library functions
```
#include <stdio.h>
int main(){
char str[100];
printf("Enter a string");
//scanf("%s",str);
fgets(str,sizeof(str),stdin);
int count=0;
int i=0;
while(str[i]!='\0'){
        if(str[i]=='\n'){
                break;
        }
        count++;
        i++;
}
printf("Length of a string =%d",count);
}
output
Enter a stringubuntu
Length of a string =6
```
## Write a program in C to separate individual characters from a string
```
#include <stdio.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
int i=0;
printf("Individual character are:");
while(str[i]!='\0'){
        if(str[i]=='\n'){
                break;
        }
        printf("%c \n",str[i]);
        i++;
        }
        }
output
Enter a stringrama
Individual character are:r 
a 
m 
a 
```
## Write a program in C to print individual characters of a string in reverse order
```
#include <stdio.h>
int main(){
char str[100];
int len=0;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
int i=0;
while(str[len]!='\0'){
        if(str[len]=='\n'){
                break;
        }
        len++;
}
printf("Individual characters in a reverse order");
for(i=len-1;i>=0;i--){
        printf("%c\n",str[i]);
}
}
output
Enter a stringrama
Individual characters in a reverse ordera
m
a
r
```
## . Write a program in C to count the total number of words in a string
```
#include <stdio.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
int i=0;
int wordcount=0;
while(str[i]!='\0'){
        if((str[i]!=' '&& str[i]!='\n')&&
           (str[i+1]==' '|| str[i+1]=='\n'||str[i]=='\0')){
           wordcount ++;
        }
        i++;
}
printf("Number of words in a given string is =%d",wordcount);
}
output
Enter a stringhello world
Number of words in a given string is =2
```
## Write a program in C to compare two strings without using string library functions.
```
#include <stdio.h>
int main(){
char str[100];
char str2[100];
int flag=0;
printf("Enter a string1");
fgets(str,sizeof(str),stdin);
printf("Enter a string2");
fgets(str2,sizeof(str2),stdin);
int i=0;
while(str[i]!='\0' && str2[i]!='\0'){
        if(str[i]=='\n'||str2[i]=='\n'){
                break;
        }
        if(str[i]!=str2[i]){
                flag=1;
                break;
}
        i++;
}
if((str[i]!='\n'&&str[i]!='\0')||(str2[i]!='\n'&&str2[i]!='\0')){
        flag=1;
}
if(flag==0){
        printf("Strings are equal");
}
else{
        printf("Strings are not equal");
}
}
output
Enter a string1ram
Enter a string2rama
Strings are not equal
```
##  Write a program in C to count the total number of alphabets, digits and special characters in a string
```
#include <stdio.h>
int main(){
char str[100];
printf("Enter a string:");
fgets(str,sizeof(str),stdin);
int i=0;
int alpha=0;
int digits=0;
int count =0;
while(str[i]!='\0'){
        if(str[i]=='\n'){
                break;
        }
   if((str[i]>='A'&&str[i]<='Z')||(str[i]>='a'&& str[i]<='z')){
    alpha++;
   }
   else if(str[i]>='0'&&str[i]<='9'){
   digits++;
   }
   else{
           count++;
   }
   i++;
}
printf("Alphabet count =%d\n",alpha);
printf("Digits count=%d\n",digits);
printf("Special character count=%d\n",count);
}
output
Enter a string:rama@1456
Alphabet count =4
Digits count=4
Special character count=1
```
## 







