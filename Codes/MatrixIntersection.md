```
#include <stdio.h>
int main(){
int n;
printf("ENter the size of an array");
scanf("%d",&n);
int arr[100][100];
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                scanf("%d",&arr[i][j]);
        }
}
int arr2[100][100];
printf("Enter the elements in the array2");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
   scanf("%d",&arr2[i][j]);
        }
}
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                for(int x=0;x<n;x++){
                        for(int y=0;y<n;y++){
                if(arr[i][j]==arr2[x][y]){
                        printf("%d ",arr[i][j]);
                        goto next;
                }
        }
}
next:;
}
}
printf("\n");
}
output
ENter the size of an array2
Enter the elements in the array1 2 3 4
Enter the elements in the array25 1 7 3
1 3
```
