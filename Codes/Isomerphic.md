```
#include <stdio.h>
#include <string.h>
int main(){
char str1[100];
printf("Enter string1");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';;
char str2[100];
printf("Enter string 2");
fgets(str2,sizeof(str2),stdin);
str2[strcspn(str2,"\n")]='\0';
int len=strlen(str1);
int len2=strlen(str2);
if(len!=len2){
        printf("Strings are not isomerphic");
}
char map1[256]={0};
char map2[256]={0};
for(int i=0;str1[i]!='\0';i++){
        if((map1[str1[i]] &&map1[str1[i]]!=str2[i])||
        (map2[str2[i]] && map2[str2[i]]!=str1[i])){
                printf("Strings are not isomerphic\n");
                return 0;
        }
        map1[str1[i]]=str2[i];
        map2[str2[i]]=str1[i];
}
printf("Strings are isomerphic");
return 0;
}
output
Enter string1egg
Enter string 2add
Strings are isomerphic
```
