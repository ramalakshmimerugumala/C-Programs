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
