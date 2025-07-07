## .WRITE A C PROGRAM TO FIND THE SUM OF ELEMENTS IN AN ARRAY USING A WHILE LOOP?
program
## 1️⃣ Program to Find the Sum of Elements in an Array Using `while` Loop
```
#include <stdio.h>
int main() {
    int arr[4];
    int sum = 0;

    printf("Enter the elements:\n");
    for(int i = 0; i < 4; i++) {
        scanf("%d", &arr[i]);
    }

    int i = 0;
    while(i < 4) {
        sum = sum + arr[i];
        i++;
    }

    printf("Sum of the elements: %d\n", sum);
    return 0;
} 

# Output
Enter the elements
1
2
3
4
Sum of the elements10
```

# 2 Reverse of an array
Program
```
#include <stdio.h>
int main() {
   int arr[]={34,56,54,32,67,89,90,32,21};
   int size=sizeof(arr)/sizeof(arr[0]);
   printf("Original array:\n");
   for(int i=0;i<size;i++){
       printf("%d\t",arr[i]);
   }
   printf("\n");
   printf("reverse of the array:\n");
   for(int i=8;i>=0;i--){
       printf("%d\t",arr[i]);
   }
    return 0;
}
# Output
Original array:
34	56	54	32	67	89	90	32	21	
reverse of the array:
21	32	90	89	67	32	54	56	34
```

# 3.Remove duplicate elements in the array
program
```
#include <stdio.h>
int main(){
    int arr[6];
    int size = 6;

    printf("Enter elements in the array:\n");
    for(int i = 0; i < size; i++){
        scanf("%d", &arr[i]);
    }

    for(int i = 0; i < size; i++){
        for(int j = i + 1; j < size;j++){
            if(arr[j] == arr[i]){
                for(int k = j; k < size; k++){
                    arr[k] = arr[k + 1];
                }
                size--;
                j--;
            }
        }
    }

    printf("After removing duplicates:\n");
    for(int i = 0; i < size; i++){
        printf("%d ", arr[i]);
    }

    return 0;
}
## Output
Enter elements in the array:
1 2 2 3 4 4
After removing duplicates:
1 2 3 4
```
## 4 Insertion of Element in the arry
```
// Online C compiler to run C program online
#include <stdio.h>
int main(){
int arr[6];
int position;
int number;
printf("Enter elements in the array:");
for(int i=0;i<5;i++){
        scanf("%d",&arr[i]);
}
printf("Original elements in the array:");
for(int i=0;i<5;i++){
        printf("%d",arr[i]);
}
printf("\nEnter the position");
scanf("%d",&position);
printf("\nEnter the number");
scanf("%d",&number);
for(int i=4;i>=position-1;i--){
        arr[i+1]=arr[i];
}
        arr[position-1]=number;
for(int i=0;i<=5;i++){
        printf("%d\n",arr[i]);
}
}
Output:
Enter elements in the array:1
2
4
7
6
Original elements in the array:12476
Enter the position2

Enter the number3
1
3
2
4
7
6
```
## 5  Write a program in C to count the total number of duplicate elements in an array.
```
#include <stdio.h>
int main() {
    int arr[6];
    int count = 0;
    printf("Enter elements in the array:\n");
    for (int i = 0; i < 6; i++) {
        scanf("%d", &arr[i]);
    }
    for (int i = 0; i < 6; i++) {
        for (int j = i + 1; j < 6; j++) {
            if (arr[i] == arr[j]) {
                printf("Duplicate element %d at index %d and %d\n", arr[i], i, j);
                count++;
                break;  // Once counted, skip to next i
            }
        }
    }
    if (count == 0) {
        printf("No duplicate elements in the array\n");
    } else {
        printf("Total duplicate elements found: %d\n", count);
    }
    return 0;
}
output
Enter elements in the array:
1
2
2
3
4
5
Duplicate element 2 at index 1 and 2
Total duplicate elements found: 1
```
## 6Write a program in C to print all unique elements in an array
```
#include <stdio.h>
int main(){
int arr[6];
printf("Enter elements in the array:");
for(int i=0;i<6;i++){
        scanf("%d",&arr[i]);

}
printf("Unique elements in the array\n");
for(int i=0;i<6;i++){
        int unique=0;
 for(int j=0;j<6;j++){
         if(arr[i]==arr[j]){
                 unique ++;
         }
}
if(unique==1){
  printf("%d\n",arr[i]);
}
}
}
output
Enter elements in the array:1
2
4
5
3
1
Unique elements in the array
2
4
5
3
```
## 7.. Write a program in C to find the sum of all elements of the array(2d arry)
```
#include <stdio.h>
int main(){
int arr[3][3];
int i,j;
printf("Enter the elements in the matrix:");
for(i=0;i<3;i++){
        for(j=0;j<3;j++){
                scanf("%d",&arr[i][j]);
        }
}
printf("Original matrix:\n");
for(i=0;i<3;i++){
        for(j=0;j<3;j++){
                printf("%d\t",arr[i][j]);
        }
        printf("\n");
}
for(i=0;i<3;i++){
        int sumrow=0;
        int sumcol=0;
  for(j=0;j<3;j++){
          sumrow=sumrow+arr[i][j];
          sumcol=sumcol+arr[j][i];
  }
  printf("\n sum of row=%d, sum of col=%d",sumrow,sumcol);
}
}
output
Enter the elements in the matrix:1
2
3
4
5
6
2
7
8
Original matrix:
1	2	3	
4	5	6	
2	7	8	

 sum of row=6, sum of col=7
 sum of row=15, sum of col=14
 sum of row=17, sum of col=17
```
## 8.Write a program in C to find the sum of all elements of the array(1d arry)
```
#include <stdio.h>
int main(){
 int arr1[5];
 int arr2[5];
 int sum[5];
 printf("Enter elements in the first array:");
 for(int i=0;i<5;i++){
   scanf("%d",&arr1[i]);
 }
 printf("enter elements in the second array:");
 for(int i=0;i<5;i++){
   scanf("%d",&arr2[i]);
 }
 for(int i=0;i<5;i++){
        sum[i]=arr1[i]+arr2[i];
        printf("sum of array index %d value is :%d\n",i,sum[i]);
 }
Output
Enter elements in the first array:1
2
3
4
5
enter elements in the second array:2
3
4
5
6
sum of array index 0 value is :3
sum of array index 1 value is :5
sum of array index 2 value is :7
sum of array index 3 value is :9
sum of array index 4 value is :11
```
## 9.Write a program in C to sort elements of an array in ascending order
```
#include <stdio.h>
int main(){
int arr[5];
printf("Enter elements in the array:");
for(int i=0;i<5;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<5;i++){
        for(int j=i+1;j<5;j++){
                if(arr[i]>arr[j]){
                     int temp=arr[i];
                     arr[i]=arr[j];
                     arr[j]=temp;
                }
        }
}
printf("Elements in ascending order\n");
for(int i=0;i<5;i++){
        printf("%d\n",arr[i]);
}
}
output
Enter elements in the array:1
3
4
2
6
Elements in ascending order
1
2
3
4
6
```
## 10  Write a program in C to sort the elements of the array in descending order
```
#include <stdio.h>
int main(){
int arr[5];
printf("Enter elements in the array:");
for(int i=0;i<5;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<5;i++){
        for(int j=i+1;j<5;j++){
                if(arr[i]<arr[j]){
                     int temp=arr[i];
                     arr[i]=arr[j];
                     arr[j]=temp;
                }
        }
}
printf("Elements in descending order\n");
for(int i=0;i<5;i++){
        printf("%d\n",arr[i]);
}
}
output
Enter elements in the array:2
4
7
1
9
Elements in descending order
9
7
4
2
1
```
## 11.
