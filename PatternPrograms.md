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
```
#include <stdio.h>
int main(){
 for(int i='A';i<='E';i++){
         for(char j='A';j<='E';j++){
                 printf("%c ",j);
         }
         printf("\n");
 }
}
Output
A B C D E 
A B C D E 
A B C D E 
A B C D E 
A B C D E
```

## Pattern4
```
#include <stdio.h>
int main(){
 for(int i=5;i>=1;i--){
         for(int j=5;j>=1;j--){
                 printf("%d ",j);
         }
         printf("\n");
 }
}
Output
5 4 3 2 1 
5 4 3 2 1 
5 4 3 2 1 
5 4 3 2 1 
5 4 3 2 1
```
## Pattern5
```
#include <stdio.h>
int main(){
 for(int i=1;i<=5;i++){
         for(int j=1;j<=i;j++){
                 printf("%d ",j);
         }
         printf("\n");
 }
}
Output
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```
## Pattern6
```
#include <stdio.h>
int main(){
 for(int i='A';i<='E';i++){
         for(char j='A';j<=i;j++){
                 printf("%c ",j);
         }
         printf("\n");
 }
}
Output
A 
A B 
A B C 
A B C D 
A B C D E
```
## pattern 7
```
#include <stdio.h>
int main(){
for(int i=1;i<=5;i++){
        for(int j=i;j>=1;j--){
                printf("%d ",j);
        }
        printf("\n");

}
}
Output
1 
2 1 
3 2 1 
4 3 2 1 
5 4 3 2 1
```
## pattern 8
```
#include <stdio.h>
int main(){
 for(int i=5;i>=1;i--){
   for(int j=1;j<=i;j++){
           printf("%d " ,j);
   }
   printf("\n");
 }
}
Output
1 2 3 4 5 
1 2 3 4 
1 2 3 
1 2 
1 
```
## Pattern 9
```
#include <stdio.h>
int main(){
 for(int i=1;i<=5;i++){
         for(int j=i;j<=5;j++){
                 printf("%d ",j);
         }
         printf("\n");
 }
}
Output
1 2 3 4 5 
2 3 4 5 
3 4 5 
4 5 
5 
```
#  Pattern 10
```
#include <stdio.h>
int main(){
for(int i=5;i>=1;i--){
        for(int j=5;j>=i;j--){
                printf("%d ",j);
        }
        printf("\n");
}
}
Output
5 
5 4 
5 4 3 
5 4 3 2 
5 4 3 2 1
```
## Pattern 11
```
#include <stdio.h>
int main(){
        for(int i=1;i<=5;i++){
        for(int j=5;j>=i;j--){
                printf("%d ",j);
        }
        printf("\n");
        }
}
Output
5 4 3 2 1 
5 4 3 2 
5 4 3 
5 4 
5 
```
## Pattern 12
```
#include <stdio.h>
int main(){
 for(int i=5;i>=1;i--){
 for(int j=i;j>=1;j--){
         printf("%d ",j);
 }
 printf("\n");
 }
}
Output
5 4 3 2 1 
4 3 2 1 
3 2 1 
2 1 
1 
```
## Pattern 13
```
#include <stdio.h>
int main(){
for(char i='A';i<='E';i++){
        for(char j=i;j>='A';j--){
                printf("%c ",j);
        }
        printf("\n");
}
}

Output
A 
B A 
C B A 
D C B A 
E D C B A
```
## Pattern 14

