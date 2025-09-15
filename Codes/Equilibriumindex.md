```
#include <stdio.h>
int main(){
int n;
printf("Enter the size of an array");
scanf("%d",&n);
int arr[100];
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
int total_sum=0;
for(int i=0;i<n;i++){
        total_sum+=arr[i];
}
int left_sum=0;
for(int i=0;i<n;i++){
int right_sum=total_sum-left_sum-arr[i];
if(left_sum==right_sum){
        printf("Equilibiram index found ta %d",i);
        return 0;
}
left_sum+=arr[i];
}
printf("No equilibrium index");
}
output
Enter the size of an array5
Enter the elements in the array1 3 5 2 2
Equilibiram index found ta 2
```


