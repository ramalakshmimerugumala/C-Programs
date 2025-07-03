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
```
#include <stdio.h>
int main(){
for(char i='E';i>='A';i--){
        for(char j='A';j<=i;j++){
                printf("%c",j);
        }
        printf("\n");
}
}
Output
ABCDE
ABCD
ABC
AB
A
```
## Pattern 15
```
#include <stdio.h>
int main(){
    for(char i='A';i<='E';i++){
                for(char j=i;j<='E';j++){
                        printf("%c",j);
                }
                printf("\n");
        }
}
Output
ABCDE
BCDE
CDE
DE
E
```
## Pattern 16
```
#include <stdio.h>
int main(){
    for(char i='E';i>='A';i--){
                for(char j='E';j>=i;j--){
                        printf("%c ",j);
                }
                printf("\n");
        }
}
Output:
E 
E D 
E D C 
E D C B 
E D C B A
```
## Pattern 17
```
#include <stdio.h>
int main(){
    for(char i='A';i<='E';i++){
                for(char j='E';j>=i;j--){
                        printf("%c ",j);
                }
                printf("\n");
        }
}
Output:
E D C B A 
E D C B 
E D C 
E D 
E
```
## Pattern 18
```
#include <stdio.h>
int main() {
    for(char i='E';i>='A';i--){
        for(char j=i;j>='A';j--){
            printf("%c ",j);
        }
        printf("\n");
    }

    return 0;
}
Output
E D C B A 
D C B A 
C B A 
B A 
A
```
## Pattern 19
```
#include <stdio.h>
int main(){
for(int i=5;i>=1;i--){
        for(int j=1;j<=i;j++){
                printf(" * ");
        }
        printf("\n");
}
}
Output
*  *  *  *  * 
*  *  *  * 
*  *  * 
*  * 
* 
```
## Pattern 20
```
#include <stdio.h>
int main(){
for(int i=1;i<=5;i++){
        for(int j=1;j<=5;j++){
         if(i==1||i==5||j==1||j==5){
                printf(" * ");
         }
         else{
                 printf("   ");
         }
        }
        printf("\n");
}
}
Output
*  *  *  *  * 
*           * 
*           * 
*           * 
*  *  *  *  *
```
## Pattern 21
```
#include <stdio.h>
int main(){
for(int i=1;i<=5;i++){
        for(int j=1;j<=i;j++){
         if(i==5||j==1||i==j){
                printf("* ");
         }
         else{
                 printf("  ");
         }
        }
        printf("\n");
}
}
Output
* 
* * 
*   * 
*     * 
* * * * *
```
## Pattern 22
```
#include <stdio.h>
int main(){
 for (int i=1;i<=5;i++){
         for(int j=1;j<=i;j++){
                 printf("%d ",j%2);
         }
         printf("\n");
 }
}
~           
Output
1 
1 0 
1 0 1 
1 0 1 0 
1 0 1 0 1
```

## Pattern 23
```
#include <stdio.h>
int main(){
 for (int i=1;i<=5;i++){
         for(int j=1;j<=i;j++){
                 if(j==1||j==3||j==5){
                         printf("1");
                 }
                 else{
                         printf("0");
                 }
         }
         printf("\n");
 }
}
Output
1
10
101
1010
10101
```
## Pattern 24
```
#include <stdio.h>
int main(){
        int k=1;
 for(int i=1;i<=5;i++){
         for(int j=1;j<=i;j++){
                 printf("%d ",k);
                 k++;
         }
         printf("\n");
 }
}
Output
1 
2 3 
4 5 6 
7 8 9 10 
11 12 13 14 15
```
## Pattern 25
```
#include <stdio.h>
int main(){
        int k=1;
 for(int i=1;i<=5;i++){
         for(int j=1;j<=i;j++){
                 printf("%d ",k%2);
                 k++;
         }
         printf("\n");
 }
}
Output
1 
0 1 
0 1 0 
1 0 1 0 
1 0 1 0 1
```
## Pattern 26
```
#include <stdio.h>
int main(){
 for(int i=1;i<=5;i++){
         for(int k=5;k>=i;k--)
                 printf("  ");
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
## Pattern27
```
#include <stdio.h>
int main(){
 int num,k;
 num=5;
for(int i=1;i<=5;i++){
        for(k=5;k>=i;k--){
                printf("  ");
        }
        for(int j=1;j<=i;j++){
                printf("%d  ",j);
        }
        printf("\n");
}
}
Output
          1  
        1  2  
      1  2  3  
    1  2  3  4  
  1  2  3  4  5
```
## Pattern 28
```
#include <stdio.h>
int main(){
        for(int i=1;i<=5;i++){
                for(int j=1;j<=i;j++){
                        printf("%d",j);
                        }
                printf("\n");
        }
        for(int i=5;i>=1;i--){
                for(int j=1;j<=i;j++){
                        printf("%d",j);
                }
                printf("\n");
        }
Output
1
12
123
1234
12345
12345
1234
123
12
1
```
## Pattern 29
```
#include <stdio.h>
int main() {
    int num;
    printf("Enter a number");
    scanf("%d",&num);
    for(int i=1;i<=num;i++){
        for(int k=1;k<=num-i;k++){
            printf(" ");
        }
        for(int j=1;j<=i;j++){
            printf("%d",j);
        }
    
        for(int j=i-1;j>=1;j--){
            printf("%d",j);
        }
        printf("\n");
    }
    }
Output
    1
   121
  12321
 1234321
123454321
```
## Pattern 30
```
#include <stdio.h>
int main(){
int num;
printf("Enter how many rows you want:");
scanf("%d",&num);
for(int i=num;i>=1;i--){
        for(int k=1;k<=num-i;k++){
                printf(" ");
        }
                for(int j=1;j<=i;j++){
                        printf("* ");
        }
                printf("\n");
}
}
Output
* * * * * 
 * * * * 
  * * * 
   * * 
    * 
```
## Pattern 31
