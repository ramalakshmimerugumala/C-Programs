```
#include <stdio.h>
#include <string.h>
int value(char r){
        switch(r){
          case 'I':
                return 1;
           case 'V':
                return 5;
           case 'X':
                return 10;
            case 'L':
                return 50;
            case 'C':
                return 100;
           case 'D':
                return 500;
           case 'M':
               return 1000;
           default:
                return -1;
        }
}
int romantoint(char str[]){
        int len=strlen(str);
        int result=0;
         for(int i=0;i<len;i++){
                 int s1=value(str[i]);
                 if(i+1<len){
                         int s2=value(str[i+1]);
                         if(s1>=s2){
                                 result+=s1;
                         }else{
                                 result+=(s2-s1);
                                 i++;
  }
                 }
                         else{
                                 result+=s1;
                         }
                 }
                 return result;
         }

int main(){
        char s[20];
        printf("Enter ROman number");
        scanf("%s",s);
        int ans=romantoint(s);
        printf("Integer value=%d\n",ans);
}
output
Enter ROman numberXL
Integer value=40
```

