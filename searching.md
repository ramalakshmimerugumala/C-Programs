## Linear search
```
#include <stdio.h>
int linearsearch(int n,int arr[],int item);
int main(){
    int n;
    int arr[100];
    int item;
    printf("Enter the size of the array");
    scanf("%d",&n);
    printf("Enter the elements in the array");
    for(int i=0;i<n;i++)
     scanf("%d",&arr[i]);
     printf("Enter the element to search");
     scanf("%d",&item);
     int result=linearsearch(n,arr,item);
     if(result!=-1){
         printf("Element %d is found  at index %d\n",item,result);
     }
     else{
         printf("Search element is not found");
     }
}
int linearsearch(int n,int arr[],int item){
    int i=0;
    while(i<n && arr[i]!=item) {
        i++;
    }
    if(arr[i]==item)
     return i;
     else
     return -1;
}
output
Enter the size of the array5
Enter the elements in the array1
2
3
4
5
Enter the element to search5
Element 5 is found  at index 4
```
## Binary search
```
#include <stdio.h>
int binarysearch(int n,int arr[],int item);
int main(){
    int n;
    int arr[100];
    int item;
    printf("Enter the size of an array");
    scanf("%d",&n);
    printf("Enter the elements in the array");
    for(int i=0;i<n;i++)
    scanf("%d",&arr[i]);
    printf("Enter the element to search");
    scanf("%d",&item);
    int index=binarysearch(n,arr,item);
     if(index!=-1){
         printf("element %d Found at index at %d\n",item,index);
     }
     else{
         printf("Element is not found");
     }
     return 0;
    }
int binarysearch(int n,int arr[],int item){
    int i=0;
    int low,up,mid;
    low=0;
    up=n-1;
    while(low<=up){
        mid=(low+up)/2;
        if(item>arr[mid]){
        low=mid+1;
        }
        else if(item<arr[mid]){
        up=mid-1;
        }
        else{
        return mid;
        }
}
return -1;
}
output
Enter the size of an array10
Enter the elements in the array1
2
3
4
5
7
8
90
91
97
Enter the element to search4
element 4 Found at index at 3
```
##  Selection sort
```
#include <stdio.h>
int main(){
int arr[100];
int  n,temp,i,j,min;
printf("Enter the size of an array");
scanf("%d",&n);
printf("Enter the elements in the array:");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}

for(i=0;i<n-1;i++){
        min=i;
 for(j=i+1;j<n;j++){
         if(arr[min]>arr[j])
             min=j;
         }
if(i!=min){
         temp=arr[i];
        arr[i]=arr[min];
        arr[min]=temp;
}
}
printf("Sorted list");
for(i=0;i<n;i++){
        printf("%d ",arr[i]);
}
output
Enter the size of an array7
Enter the elements in the array:12
34
2
56
89
7823
23
Sorted list2 12 23 34 56 89 7823
```
## 

