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
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
int multi(char str1[],char str2[]);
int main(){
char str1[100];
char str2[100];
printf("Enter a string 1");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';
printf("Enter string2");
fgets(str2,sizeof(str2),stdin);
str2[strcspn(str2,"\n")]='\0';
int result=multi(str1,str2);
printf("result=%d",result);
}
int multi(char str1[],char str2[]){
        int num1=atoi(str1);
        int num2=atoi(str2);
        return num1*num2;
}
output
Enter a string 14
Enter string25
result=20
```
##  Write a C program to reverse all the vowels present in a given string. Return the newly created string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
char vowel[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int j=0;
for(int i=0;str[i]!='\0';i++){
        if((str[i]=='A'||str[i]=='E'||str[i]=='I'||str[i]=='O'||str[i]=='U')||(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')){
                vowel[j]=str[i];
                j++;
        }
}
vowel[j]='\0';
printf("%s\n",vowel);
int len=strlen(vowel);
printf("Reverse of vowels");
char temp;
for(int i=0,j=len-1;i<j;i++,j--){
       temp=vowel[i];
      vowel[i]=vowel[j];
       vowel[j]=temp;
}
printf("%s ",vowel);
j=0;
for(int i=0;str[i]!='\0';i++){
        if((str[i]=='A'||str[i]=='E'||str[i]=='I'||str[i]=='O'||str[i]=='U')||(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')){
                str[i]=vowel[j++];
        }
}
printf("\nfinal string %s",str);
}
output
Enter a stringhello 
eo
Reverse of vowelsoe 
final string holle
```
## palindrome string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
int ispalindrome=1;
for(int i=0,j=len-1;i<j;i++,j--){
        if(str[i]!=str[j]){
                ispalindrome=0;
                break;
        }
}
if(ispalindrome){
        printf("It is a palindrome string");
}
else{
        printf("It is not a plaindrome string");
}
}
```
##  Write a C program to find the longest palindromic substring from a given string. Return the substring
```
#include <stdio.h>
#include <stdbool.h>
#include <string.h>
bool ispalindrome(char str[],int left,int right){
        while(left<right){
          if(str[left]!=str[right]){
                  return false;
          }
          left++;
          right--;
        }
        return true;
}
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int maxlen=0;
int maxstart=0;
int len=strlen(str);
for(int i=0;i<len;i++){
        for(int j=i;j<len;j++){
                if(ispalindrome(str,i,j)){
                        int currentlen=j-i+1;
                        if(currentlen>maxlen){
                                maxlen=currentlen;
                                maxstart=i;
                        }
                }
                        }

}
printf("Longest palindrome");
for(int k=maxstart;k<maxstart+maxlen;k++){
        printf("%c",str[k]);
        }
        }
output
Enter a stringabcsdgbab
Longest palindromebab
```
## Write a C program to calculate the length of the longest common subsequence of two given strings.
```
#include <stdio.h>
#include <string.h>
int max(int a,int b){
        return a>b?a:b;
}
int main(){
char str1[100];
char str2[100];
printf("Enter a string 1");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';
printf("Enter a string 2");
fgets(str2,sizeof(str2),stdin);
str2[strcspn(str2,"\n")]='\0';
int len1=strlen(str1);
int len2=strlen(str2);
int dp[len1+1][len2+1];
for(int i=0;i<=len1;i++){
  for(int j=0;j<=len2;j++){
          if(i==0||j==0){
                  dp[i][j]=0;
          }
          else if(str1[i-1]==str2[j-1]){
           dp[i][j]=1+dp[i-1][j-1];
          }
          else{
                  dp[i][j]=max(dp[i-1][j],dp[i][j-1]);
          }
  }
}
int i=len1,j=len2;
char lcs[100];
int index=dp[len1][len2];
lcs[index]='\0';
while(i>0 &&j>0){
        if(str1[i-1]==str2[j-1]){
                lcs[index-1]=str1[i-1];
                i--;
                j--;
                index--;
        }
        else if(dp[i-1][j]>dp[i][j-1])
                i--;
        else
                j--;
}
   printf("LCS string=%s\n",lcs);
  printf("Length of longest common subsequence %d",dp[len1][len2]);
}
output
Enter a string 1abc
Enter a string 2ac
LCS string=ac
Length of longest common subsequence 2
```
## Write a C program to compare two strings
```
#include <stdio.h>
#include <string.h>
int main(){
char str1[100];
char str2[100];
int flag=0;
printf("Enter a string1");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';
printf("Enter a string 2");
fgets(str2,sizeof(str2),stdin);
str2[strcspn(str2,"\n")]='\0';
for(int i=0;str1[i]!='\0'||str2[i]!='\0';i++){
                if(str1[i]!=str2[i]){
                        flag=1;
                        break;
        }
}
if(flag==0){
        printf("both are equal");
}
else{
        printf("Both are not equal");
}
}
output
Enter a string1hello
Enter a string 2hello
both are equal
```
## Write a C program to toggle the case of each character of a string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
for(int i=0;str[i]!='\0';i++){
if(str[i]>='A' && str[i]<='Z'){
        str[i]=str[i]+32;
}
else if(str[i]>='a' && str[i]<='z'){
        str[i]=str[i]-32;
}
}
printf("toggele= %s",str);
}
output
Enter a stringRAMA
toggele= rama
```
## Write a C program to reverse order of words in a given string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
int len=0;
printf("Enter the string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i=0;
while(str[len]!='\0'){
       if(str[len]=='\n'){
               str[len]='\0';
               break;
       }
       len++;
}
char temp;
int j;
for(i=0,j=len-1;i<j;i++,j--){
      temp=str[i];
      str[i]=str[j];
      str[j]=temp;
}
printf("First revese=%s\n",str);
for(i=0,j=len-1;i<j;i++,j--){
        temp=str[i];
        str[i]=str[j];
        str[j]=temp;
}
printf("Orginal string=%s\n",str);
}
output
Enter the stringi know
First revese=wonk i
Orginal string=i know
```
## . Write a C program to find the first occurrence of a character in a given string.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char ch;
printf("Enter the character to search");
scanf(" %c",&ch);
int found=0;
int i;
for(i=0;str[i]!='\0';i++){
        if(str[i]==ch){
                found=1;
                break;
        }
}
if(found==1){
        printf("Fist occurence %c character found at index=%d",ch,i);
}
else{
        printf("not found");
}
}
output
Enter a stringhello world
Enter the character to searcho
Fist occurence o character found at index=4
```
## Write a C program to find the last occurrence of a character in a given string
```
#include <stdio.h>
#include <string.h>
int main(){
char str1[100];
printf("Enter the string");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';
char ch;
printf("Enter a character to search");
scanf("%c",&ch);
int found=0;
int lastindex=-1;
int i;
for(i=0;str1[i]!='\0';i++){
        if(str1[i]==ch){
                found=1;
                lastindex=i;
                 }
}
if(lastindex!=-1){
        printf("Last occurence %c character found at index=%d\n",ch,lastindex);
}
else{
        printf("Not found");
}
}
output
Enter the stringhello world
Enter a character to searcho
Last occurence o character found at index=7
```
## Write a C program to search all occurrences of a character in a given string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char ch;
printf("Enter a character");
scanf("%c",&ch);
int found=0;
int i;
for(i=0;str[i]!='\0';i++){
        if(str[i]==ch){
                printf("occurs at =%d ",i);
                found=1;
        }
}
if(!found){
        printf("None");
}
printf("\n");
}
output
Enter a stringhello world
Enter a charactero
occurs at =4 occurs at =7
```
## . Write a C program to count occurrences of a character in a given string.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i;
int count=0;
char ch;
printf("Enter a character");
scanf("%c",&ch);
for(i=0;str[i]!='\0';i++){
        if(str[i]==ch){
                count ++;
        }
}
printf("%c occurs %d times\n",ch,count);
}
output
Enter a stringhello world
Enter a characterl
character l occurs 3 times
```
##  Write a C program to find the highest frequency character in a string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
int visited[100]={0};
int maxcount=0;
char maxchar;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
int count;
for(int i=0;i<len;i++){
        if(visited[i]==1){
                continue;
        }
           count=1;
for(int j=i+1;j<len;j++){
                if(str[i]==str[j]){
                        visited[j]=1;
                        count ++;
                }
        }
if(count>maxcount){
        maxcount=count;
        maxchar=str[i];
}
}
printf("Highest frequency =%c occurs %d times",maxchar,maxcount);
}
  output
Enter a stringrama
Highest frequency =a occurs 2 times
```
## . Write a C program to find the lowest frequency character in a string
```
#include<stdio.h>
#include <string.h>
int main(){
char str[100];
int visited[100]={0};
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
int count;
int mincount=len;
char minchar;
for(int i=0;i<len;i++){
        if(visited[i]==1)
                continue;
                count=1;
        for(int j=i+1;j<len;j++){
     if(str[i]==str[j]){
                        visited[j]=1;
                        count++;
                }
        }
        if(count<mincount){
                mincount=count;
                minchar=str[i];
        }
}
printf("Lowest frequency  %c occurs %d times",minchar,mincount);
}
output
Enter a stringheell
Lowest frequency  h occurs 1 times
```
## . Write a C program to remove all occurrences of a character from a string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char ch;
printf("Enter a character");
scanf("%c",&ch);
int j=0;
for(int i=0;str[i]!='\0';i++){
        if(str[i]!=ch){
          str[j]=str[i];
          j++;
        }
}
str[j]='\0';
printf("After removing all occurances %c:%s",ch,str);
}
output
Enter a stringhello world
Enter a characterl
After removing all occurances l:heo word
```
## Write a C program to remove all repeated characters from a given string.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[200];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int len=strlen(str);
for(int i=0;i<len;i++){
        for(int j=i+1;j<len;j++){
                if(str[i]==str[j]){
                        for(int k=j;k<len;k++){
                          str[k]=str[k+1];
                        }
                        j--;
                        len--;
                }
}
}
printf("String after removing duplicates =%s",str);
}
output
Enter a stringrama
String after removing duplicates =ram
```
## Write a C program to replace the last occurrence of a character with another in a string.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char ch;
printf("Enter a character to replace");
scanf(" %c",&ch);
char newchar;
printf("Enter a newcharacter");
scanf(" %c",&newchar);
int lastindex=-1;
for(int i=0;str[i]!='\0';i++){
        if(str[i]==ch){
                lastindex=i;
}
}
if(lastindex!=1){
        str[lastindex]=newchar;
}
printf("Modified string=%s",str);
}
output
Enter a stringhello world
Enter a character to replaceo
Enter a newcharacterx
```
## Write a C program to replace the first occurrence of a character with another in a string.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("enter the string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char ch;
printf("Enter a character");
scanf(" %c",&ch);
char new;
printf("Enter new character to replace");
scanf(" %c",&new);
for(int i=0;str[i]!='\0';i++){
        if(str[i]==ch){
                str[i]=new;
                break;
                 }
}
printf("Modified string:%s\n",str);
}
output
enter the stringhello
Enter a characterl
Enter new character to replacex
Modified string:hexlo
```
## Write a C program to replace all occurrences of a character with another in a string.
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char ch;
printf("Enter a character  to replace");
scanf(" %c",&ch);
char new;
printf("enter a character");
scanf(" %c",&new);
for(int i=0;str[i]!='\0';i++){
        if(str[i]==ch){
                str[i]=new;
        }
}
printf("Modified string %s",str);
}
output
Enter a stringhello world
Enter a character  to replacel
enter a characterx
Modified string hexxo worxd
```
## trim leading
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("enter a string:");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i=0;
while(str[i]=='\''||str[i]=='"')i++;
while(str[i]==' '||str[i]=='\t')
        i++;
int j=0;
while(str[i]!='\0'){
        str[j++]=str[i++];
}
str[j]='\0';
printf("Modified string %s\n",str);
}
output
enter a string:  hello
modified string hello
```
## Write a C program to trim both leading and trailing white space characters from given string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter the string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i=0;
while(str[i]=='\''|| str[i]=='"'||str[i]==' '||str[i]=='\t'||str[i]=='\n')
        i++;
int j=0;
while(str[i]!='\0'){
        str[j++]=str[i++];
}
str[j]='\0';
int len=strlen(str);
while(len>0&&(str[len-1]=='\''||str[len-1]=='"')||str[len-1]==' '||str[len-1]=='\t'||str[len-1]=='\n'){
    str[len-1]='\0';
    len --;
    }
printf("Modified string =%s",str);
}
output
Enter the string'  hello  '
Modified string =hello
```
##  Write a C program to remove all extra blank spaces from given string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int i=0;
while(str[i]=='\''||str[i]=='"'||str[i]==' '||str[i]=='\t'||str[i]=='\n'){
        i++;
}
int j=0;
while(str[i]!='\0'){
        str[j++]=str[i++];
}
str[j]='\0';
int len=strlen(str);
while(len>0 &&(str[len-1]=='\''||str[len-1]=='"'||str[len-1]==' '||str[len-1]=='\t'||str[len-1]=='\n')){
        str[len-1]='\0';
        len--;
}
i=0;
j=0;
int space_flag=0;
while(str[i]!='\0'){
        if(str[i]!=' '&& str[i]!='\t'){
                str[j++]=str[i];
                space_flag=0;
        }
        else{
                if(space_flag==0){
             str[j++]=' ';
                        space_flag=1;
                }
        }
        i++;
}
str[j]='\0';
printf("Modified string :%s\n",str);
}
output
Enter a string'  hello   world  '
Modified string :hello world
```
## substring found
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
char sub[100];
int found=0;
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
printf("Enter a substring");
fgets(sub,sizeof(sub),stdin);
sub[strcspn(sub,"\n")]='\0';
int len1=strlen(str);
int len2=strlen(sub);
int j;
for(int i=0;i<len1-len2+1;i++){
        for(j=0;j<len2;j++){
                if(str[i+j]!=sub[j]){
                        break;
                }
        }
        if(j==len2){
                found=1;
break;
        }
}
if(found){
        printf("substring found");
}
else{
        printf("Substring is not found");
}
}

output
Enter a stringabcabb
Enter a substringabc
substring found
```
## Deleting a specific word from a given string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
char del[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
printf("Enter a string to delte");
fgets(del,sizeof(del),stdin);
del[strcspn(del,"\n")]='\0';
int match;
int len1=strlen(str);
int len2=strlen(del);
int j;
for(int i=0;i<len1-len2+1;i++){
        int match=1;
        for(j=0;j<len2;j++){
                if(str[i+j]!=del[j]){
                        match=0;
                        break;
                }
        }
if(match){
                for(int k=i;k<len1-len2+1;k++){
                        str[k]=str[k+len2];
                }
                len1=len1-len2;
                i--;
        }
}
printf("After deleting %s\n",str);
}
output
Enter a stringi love moon
Enter a string to deltelove
After deleting i  moon
```
##  captalize each word first letter
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
for(int i=0;str[i]!='\0';i++){
        if(i==0 ||str[i-1]==' '){
                if(str[i]>='a'&& str[i]<='z'){
                        str[i]=str[i]-32;
                }
        }
}
printf("captialized string=%s",str);
}
output
Enter a stringrama lakshmi
captialized string=Rama Lakshmi
```
##  Removing special characters from string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
int j=0;
for(int i=0;str[i]!='\0';i++){
if((str[i]>='A' && str[i]<='Z')||
  (str[i]>='a' && str[i]<='z')||
  (str[i]>='0' && str[i]<='9')){
  str[j++]=str[i];
}
}
str[j]='\0';
printf("string=%s",str);
}
output
Enter a stringrama@12#%^
string=rama12
```

## convert string to int
```
#include <stdio.h>
#include <string.h>
int main(){
int num=0;
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
for(int i=0;str[i]!='\0';i++){
num=num*10+(str[i]-'0');
}
printf("Integer value=%d",num);
}
output
Enter a string24
Integer value=24
```
## Anagram
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
char visited[100]={0};
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char str2[100];
printf("Enter a string");
fgets(str2,sizeof(str2),stdin);
str2[strcspn(str2,"\n")]='\0';
int len=strlen(str);
int len2=strlen(str2);
if(len!=len2){
        printf("Anagram is not possible");
        return 0;
}
for(int i=0;i<len;i++){
        if(visited[i]==1)
                continue;
        int count=1;
        for(int j=i+1;j<len;j++){
if(str[i]==str[j]){
                        visited[j]=1;
                        count ++;
                }
        }
        int count1=0;
        for(int k=0;k<len2;k++){
                if(str2[k]==str[i]){
                        count1 ++;
        }
}
if(count1!=count){
        printf("Not anagram");
        return 0;
}
}
        printf("Anagram");
}
output
Enter a stringsilent
Enter a stringlisten
Anagram
```
##  Revesing each word in a string
```
#include <stdio.h>
#include <string.h>
void reversestring(char str[],int start,int end){
        while(start<end){
                char temp=str[start];
                str[start]=str[end];
                str[end]=temp;
                start ++;
                end--;
        }
}
int main(){
        char str[100];
        printf("Enter a string");
        fgets(str,sizeof(str),stdin);
        str[strcspn(str,"\n")]='\0';
        int len=strlen(str);
        int start=0;
        for(int i=0;i<=len;i++){
                if(str[i]==' '||str[i]=='\0'){
                        int end=i-1;
 reversestring(str,start,end);
                        start=i+1;
                }
        }
        printf("Reverse of each word %s",str);
}

output
nter a stringrama lakshmi
Reverse of each word amar imhskal
```
or 
```
#include <stdio.h>
#include <string.h>
int main(){
    char str[100];
    printf("Enter a string");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int start=0;
    int len=strlen(str);
    for(int i=0;i<=len;i++){
        if(str[i]==' '){
            for(int j=i-1;j>=start;j--){
                printf("%c",str[j]);
                }
                printf(" ");
                start=i+1;
        }
    }
    for(int j=len-1;j>=start;j--){
        printf("%c",str[j]);
    }
}
````
## reverse order of words
```
#include <stdio.h>
#include <string.h>
int main(){
    char str[100];
    printf("Enter a string");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int len=strlen(str);
    int end=len-1;
    for(int i=end;i>=0;i--){
        if(str[i]==' '){
            for(int j=i+1;j<=end;j++){
                printf("%c",str[j]);
                }
                printf(" ");
                end=i-1;
        }
    }
    for(int j=0;j<=end;j++){
        printf("%c",str[j]);
    }
}
output
Enter a stringvivan embedded
embedded vivan
```
## C program sort storing in array
```
#include <stdio.h>
#include <string.h>
int main(){
int n;
char str[10][50];
char temp[50];
printf("Enter number of strings");
scanf("%d",&n);
printf("Enter a string");
for(int i=0;i<n;i++){
        scanf("%s",str[i]);
}
for(int i=0;i<n-1;i++){
        for(int j=0;j<n-i-1;j++){
                if(strcmp(str[j],str[j+1])>0){
                        strcpy(temp,str[j]);
                        strcpy(str[j],str[j+1]);
                          strcpy(str[j+1],temp);
                }
        }
}
printf("Sorted strings");
for(int i=0;i<n;i++){
        printf("%s ",str[i]);
}
}
output
Enter number of strings3
Enter a stringmango
banana
apple
Sorted strings apple banana mango
```
## Insering word in string
```
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
char word[50];
int position;
printf("Enter a position");
scanf("%d",&position);
printf("Enter the a word to insert");
scanf("%s",word);
int index=position-1;
int len=strlen(str);
int wordlen=strlen(word);
for(int i=len-1;i>=index;i--){
        str[i+wordlen]=str[i];
}
for(int i=0;i<wordlen;i++){
str[index+i]=word[i];
}
printf("%s",str);
}
output
Enter a stringrama lakshmi
Enter a position5
Enter the a word to insertui
ramaui lakshmi
```
## Deleting word in a string
```
#include <stdio.h>
#include <string.h>
int main(){
char str[100];
printf("Enter a string");
fgets(str,sizeof(str),stdin);
int position;
printf("Enter a position");
scanf("%d",&position);
int len=strlen(str);
char word[50];
printf("Enter a word");
scanf("%s",word);
int wordlen=strlen(word);
for(int i=position;i<=len-wordlen;i++){
        str[i]=str[i+wordlen];
}
printf("%s",str);
}
Enter a stringrama lakshmi
Enter a position5 
Enter a wordlakshmi
rama
```





                       






                                
















