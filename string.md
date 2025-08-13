## substring found
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
## . Write a program in C to copy one string to another string
```
#include <stdio.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
char str2[100];
int i=0;
while(str[i]!='\0'){
        str2[i]=str[i];
         i++;
}
str2[i]='\0';
printf("Copied string=%s",str2);
}
output
Enter a stringhenry
Copied string=henry
```
## Write a program in C to count the total number of vowels or consonants in a string
```
#include <stdio.h>
int main(){
char str[100];
int vowelcount=0;
int consonant=0;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
for(int i=0;str[i]!='\0';i++){
        if((str[i]=='A'||str[i]=='E'||str[i]=='I'||str[i]=='O'||str[i]=='U')||(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')){
                vowelcount ++;
        }
        else if((str[i]>='A'&& str[i]<='Z')||(str[i]>='a'&& str[i]<='z')){
         consonant++;
        }
}
printf("Vowelcount=%d",vowelcount);
printf("Consonant count=%d",consonant);
}
output
Enter a stringramalakshmi
Vowelcount=4Consonant count=7
```
## . Write a program in C to find the maximum number of characters in a string
```
#include <stdio.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
int len=0;
int i=0;
while(str[i]!='\0'){
        if(str[i]=='\n'){
                break;
        }
        len++;
        i++;
}
printf("max characters in a string=%d",len);
}
output
Enter a stringrama
max characters in a string=4
```
## Another method
```
#include <string.h>
int main(){
int n;
int maxlen=0;
char str[100];
char longest[100];
printf("Enter number of strings");
scanf("%d",&n);
getchar();//removes the /n
for(int i=0;i<n;i++){
        printf("Enter a string\n");
        fgets(str,sizeof(str),stdin);
        str[strcspn(str,"\n")]='\0';
        int len=strlen(str);
        if(len>maxlen){
                maxlen=len;
                strcpy(longest,str);
 }
}
printf("Longest substring=%s\n",longest);
printf("Maximum number of characters=%d\n",maxlen);
}
output
Enter number of strings2
Enter a string
beetroot
Enter a string
root
Longest substring=beetroot
Maximum number of characters=8
```
## Write a C program to sort a string array in ascending orde
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
for(int i=0;str[i]!='\0';i++){
        for(int j=i+1;str[j]!='\0';j++){
                if(str[i]>str[j]){
                        char temp=str[i];
                        str[i]=str[j];
                        str[j]=temp;
                }
        }
}
printf("sorted string=%s",str);
}
output
Enter a stringhello
sorted string=ehllo
```
## . Write a program in C to extract a substring from a given string
```
#include <stdio.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
int start;
int end;
char substring[100];
int j=0;
printf("Enter start position");
scanf("%d",&start);
printf("Enter a end position");
scanf("%d",&end);
for(int i=start;i<=end&&str[i]!='\0';i++){
        substring[j++]=str[i];
}
substring[j]='\0';
printf("Extracted substring=%s\n",substring);
return 0;
}
output
Enter a stringgood morning
Enter start position2
Enter a end position5
Extracted substring=od m
```
## 5. Write a program in C to read a sentence and replace lowercase characters with uppercase and vice versa
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i=0;
while(str[i]!='\0'){
        if(str[i]>='a'&& str[i]<='z'){
                str[i]=str[i]-32;
        }
        else if(str[i]>='A' && str[i]<='Z'){
                str[i]=str[i]+32;
        }
        i++;
}
printf("Converted string =%s",str);
}
output
Enter a stringrama
Converted string =RAMA
```
## Write a program in C to find the number of times a given word 'the' appears in the given string
```
#include <string.h>
int main(){
char str[100];
char *token;
int count=0;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
token=strtok(str," ");
while(token!=NULL){
        if(strcmp(token,"the")==0){
                count ++;
        }
        token=strtok(NULL," ");
}
printf("count=%d\n",count);
}
output
Enter a stringthe sun in the east
count=2
````
## Write a program in C to find the frequency of characters
```
#include <string.h>
int main(){
char str[100];
char visited[100]={0};
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
for(int i=0;i<len;i++){
        if(visited[i]==1)
                continue;
        visited[i]=1;
        int count=1;
        for(int j=i+1;j<len;j++){
                if(str[i]==str[j]){
                        visited[j]=1;
                        count ++;
                }
        }
        printf("%c occurs %d times\n",str[i],count);
}
}
output
Enter a stringsriram
s occurs 1 times
r occurs 2 times
i occurs 1 times
a occurs 1 times
m occurs 1 times
```
## Write a program in C to remove characters from a string except alphabets
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
char result[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i,j;
 i=0;
 j=0;
while(str[i]!='\0'){
if((str[i]>='A' && str[i]<='Z')||(str[i]>='a'&& str[i]<='z')){
 result[j]=str[i];
 j++;
}
i++;
}
result[j]='\0';
printf("After removing %s\n",result);
}
output
Enter a stringrama@34!
After removing rama
```
## 9. Write a program in C to combine two strings manually
```
#include <stdio.h>
#include <string.h>
int main(){
char str1[100];
char str2[100];
printf("Enter a string 1");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';
printf("Enter a string2");
fgets(str2,sizeof(str2),stdin);
str2[strcspn(str2,"\n")]='\0';
int i=0;
while(str1[i]!='\0'){
        i++;
}
int j=0;
while((str1[i++]=str2[j++])){
}
printf("combined string=%s",str1);
}
output
Enter a string 1hii
Enter a string2hello
hiihello
```
## . Write a program in C to find the largest and smallest words in a string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[500];
char *token;
char largest[100];
char smallest[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
token=strtok(str," ");
strcpy(largest,token);
strcpy(smallest,token);
while(token!=NULL){
        int len=strlen(token);
        if(len>strlen(largest)){
                strcpy(largest,token);
        }
        if(len<strlen(smallest)){
                strcpy(smallest,token);
        }
        token=strtok(NULL," ");
}
printf("Largest word=%s",largest);
printf("Smallest word=%s",smallest);
}
output
Enter a stringsun rises in the east
Largest word=rises
Smallest word=in
```
## profram to find character is hexa digit or not
```
#include <stdio.h>
int main(){
char ch;
printf("Enter a character");
scanf("%c",&ch);
if((ch>='0'&&ch<='9')||(ch>='A'&&ch<='F')||(ch>='a'&&ch<='f')){
        printf("Hexadigit character");
}
        else{
                printf("Not a hexa digit");
        }
}
```
## Write a program in C to replace the spaces in a string with a specific character
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
char ch;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
printf("Enter a specific character");
scanf("%c",&ch);
for(int i=0;str[i]!='\0';i++){
        if(str[i]==' '){
                str[i]=ch;
        }
}
printf("final string=%s\n",str);
}
output
Enter a stringthe penguin
Enter a specific character_
final string=the_penguin
```
## Write a program in C to count the number of punctuation characters present in a string
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int count=0;
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
for(int i=0;str[i]!='\0';i++){
        if(ispunct(str[i])){
                count ++;
        }
}
printf("count=%d",count);
}
output
Enter a stringrama@1.,
count=3
```
## Write a program in C to print only the string before the new line character
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
printf("%s",str);
}
output
Enter a stringhello world
hello world
```
## Write a program in C to split strings by space into words
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
char *token;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
token=strtok(str," ");
while(token!=NULL){
        printf("%s\n",token);
token=strtok(NULL," ");
}
}
output
Enter a stringhello i am learning c
hello
i
am
learning
c
```
## Write a C program to find the repeated character in a string
```
#include <string.h>
int main(){
char str[100];
char visited[100]={0};
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
for(int i=0;i<len;i++){
        if(visited[i]==1)
                continue;
                int count=1;
        for(int j=i+1;j<len;j++){
                if(str[i]==str[j]){
                count ++;
                visited[j]=1;
        }
        }
        if(count>1 && str[i]!=' ')
        printf("%c occurs %d times\n",str[i],count);
}
}
output
Enter a stringrama
a occurs 2 times
```
## Write a C program to count each character in a given string
```
#include <string.h>
int main(){
char str[100];
char visited[100]={0};
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
for(int i=0;i<len;i++){
        if(visited[i]==1)
                continue;
                int count=1;
        for(int j=i+1;j<len;j++){
                if(str[i]==str[j]){
                count ++;
                visited[j]=1;
        }
        }
        printf("%c occurs %d times\n",str[i],count);
}
}
```
## . Write a C program to convert vowels into uppercase characters in a string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i=0;
while(str[i]!='\0'){
        if((str[i]=='A'||str[i]=='E'||str[i]=='I'||str[i]=='O'||str[i]=='U')||(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u'))
                str[i]=str[i]-32;
        i++;
}
printf("%s",str);
}
output
Enter a stringthe sun
thE sUn
```
## Write a C program to find the length of the longest substring of a given string without repeating characters.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int start=0;
int maxlen=0;
int maxstart;
int len=strlen(str);
for(int i=0;i<len;i++){
        for(int j=start;j<i;j++){
                if(str[i]==str[j]){
                        start=j+1;
                        break;
                }
        }
        int currentlen=i-start+1;
        if(currentlen>maxlen){
                maxlen=currentlen;
         maxstart=start;
        }
}
printf("Longest non repeated substring");
for(int k=0;k<maxlen;k++){
        printf("%c ",str[maxstart+k]);
}
        printf("length=%d\n",maxlen);
}
output
Enter a stringabafk
Longest non repeated substringbafk
length=4
```
## A given string contains the bracket characters '(', ')', '{', '}', '<', ‘>', '[' and ']', Write a C program to check if the string is valid or not. The input string will be valid when open brackets and closed brackets are the same type of brackets.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i=0;
while(1){
        int removed=0;
        for(int i=0;str[i]!='\0';i++){
                if((str[i]=='('&&str[i+1]==')')||
                  (str[i]=='{'&&str[i+1]=='}')||
                  (str[i]=='['&&str[i+1]==']')||
                  (str[i]=='<'&&str[i+1]=='>')){
                        int j;
                        for(j=i;str[j+2]!='\0';j++){
                                str[j]=str[j+2];
                        }
                        str[j]='\0';
                        removed=1;
                        break;
                }
}
                if(!removed)
                        break;
        }
if(strlen(str)==0){
        printf("It is a valid string");
}
else{
        printf("It is not a valid string");
}
}
output
Enter a string<{[]}>
It is a valid string
```
## Write a C program to multiply two positive numbers as strings. Return a string representation of the product.
```














