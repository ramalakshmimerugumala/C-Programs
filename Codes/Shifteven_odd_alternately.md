```
#include <stdio.h>
int main(){
    int n;
    int even[100];
    int odd[100];
    int ei=0;
    int oi=0;
    int result[100];
    printf("Enter the size of an arry");
    scanf("%d",&n);
    int arr[100];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    for(int i=0;i<n;i++){
        if(arr[i]%2==0){
            even[ei++]=arr[i];
        }
        else{
            odd[oi++]=arr[i];
        }
    }
    int i=0,e=0,o=0;
    while(e<ei && o<oi){
        result[i++]=even[e++];
        result[i++]=odd[o++];
    }
    while(e<ei){
        result[i++]=even[e++];
    }
    while(o<oi){
        result[i++]=odd[o++];
    }
    for(int k=0;k<n;k++){
        printf("%d ",result[k]);
    }
}
output
Enter the size of an arry7
1 6 2 4 8 7 9 
6 1 2 7 4 9 8 
```
