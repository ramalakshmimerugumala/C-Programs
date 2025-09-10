```
#include <stdio.h>
int main(){
int arr[100][100];
int n;
printf("Enter the size of an array");
scanf("%d",&n);
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
        scanf("%d",&arr[i][j]);
}
}
int top=0,left=0,bottom=n-1,right=n-1;
while(top<=bottom && left<=right){
        for(int i=left;i<=right;i++){
                printf("%d ",arr[top][i]);
        }
         top++;
        for(int i=top;i<=bottom;i++){
                printf("%d ",arr[i][right]);
        }
        right--;
        if(top<=bottom){
                for(int i=right;i>=left;i--){
                        printf("%d ",arr[bottom][i]);
                }
                bottom --;
        }
        if(left<=right){
                for(int i=bottom;i>=top;i--){
                        printf("%d ",arr[i][left]);
                }
                   left++;
        }
}
}
output
Enter the size of an array4
Enter the elements in the array1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16
1 2 3 4 8 12 16 15 14 13 9 5 6 7 11 10
```


