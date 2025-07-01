## Pattern1
```
#include <stdio.h>
int main(){
 for(int i=1;i<=4;i++){
         for(int j=1;j<=5;j++){
                 printf("%d ",j);
 }
         printf("\n");
 }
}
Output:
1 2 3 4 5 
1 2 3 4 5 
1 2 3 4 5 
1 2 3 4 5
```
## Pattern2
```
#include <stdio.h>
int main(){
 for(int i=1;i<=4;i++){
         for(int j=1;j<=4;j++){
                 printf("%d",i);
         }
         printf("\n");
 }
Output
1111
2222
3333
4444
```
## Pattern3
