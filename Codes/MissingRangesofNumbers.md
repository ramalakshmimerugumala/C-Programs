```
#include <stdio.h>
int main(){
int n;
int arr[100];
printf("Enter the size of an arrry");
scanf("%d",&n);
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
int lower;
printf("Enter start value");
scanf("%d",&lower);
int upper;
printf("Enter upper value");
scanf("%d",&upper);
int prev=lower-1;
for(int i=0;i<=n;i++){
        int current=(i<n)?arr[i]:upper+1;
        if(prev+1<=current -1){
          if(prev+1==current-1){
                  printf("[%d,%d]\n",prev+1,prev+1);
          }
          else{
                  printf("[%d,%d]\n",prev+1,current-1);
          }
        }
        prev=current;
}
}
output
Enter the size of an arrry6
Enter the elements in the array14 15 20 30 31 45
Enter start value10
Enter upper value50
[10,13]
[16,19]
[21,29]
[32,44]
[46,50]
```
