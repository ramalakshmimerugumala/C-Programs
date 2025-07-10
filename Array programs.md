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
## 7.. Write a program in C to find the sum of rows and columns of the array(2d arry)
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
## 11. Write a program in C to merge two arrays of the same size sorted in descending order
```
#include <stdio.h>
int main(){
int arr1[5];
int arr2[4];
printf("Enter elements in  the array1:");
for(int i=0;i<5;i++){
        scanf("%d",&arr1[i]);
}
printf("Enter elements in the array2:");
for(int i=0;i<4;i++){
        scanf("%d",&arr2[i]);                               
        }
for(int i=0;i<4;i++){
        arr1[5+i]=arr2[i];
}
printf("Merge of two arrays:");
for(int i=0;i<9;i++){
        printf("%d ",arr1[i]);
}
for(int i=0;i<9;i++){
    for(int j=i+1;j<9;j++){
        if(arr1[i]<arr1[j]){
           int temp=arr1[i];
            arr1[i]=arr1[j];
            arr1[j]=temp;
        }
    }
}
printf("\nElements after descending order:");
for(int i=0;i<9;i++){
    printf("%d ",arr1[i]);
}
}
Output
Enter elements in  the array1:3
2
1
8
3
Enter elements in the array2:9
1
4
7
Merge of two arrays:3 2 1 8 3 9 1 4 7 
Elements after descending order:9 8 4 3 3 2 1 1 1
```
## 12. Write a program in C to count the frequency of each element of an array
```
#include <stdio.h>
int main(){
int arr[5];
int frequency[5];
printf("Enter elements in the array:");
for(int i=0;i<5;i++){
        scanf("%d",&arr[i]);
        frequency[i]=-1;
}
for(int i=0;i<5;i++){
        int count=1;
        if(frequency[i]==0)
                continue;
        for(int j=i+1;j<5;j++){
           if(arr[j]==arr[i]){
                   count++;
                   frequency[j]=0;
}
        }
           frequency[i]=count;
        }

printf("Frequency of elements in the arrat are:");
for(int i=0;i<5;i++){
        if(frequency[i]!=0){
        printf("%d occurs %d times\n",arr[i],frequency[i]);
}

}
}
output
Enter elements in the array:1
3
2
1
4
Frequency of elements in the arrat are:1 occurs 2 times
3 occurs 1 times
2 occurs 1 times
4 occurs 1 times
```
## 13 Write a program in C to find the second largest element in an array
```
#include <stdio.h>
int main(){
int arr[8];
int max1=arr[0];
int max2=arr[0];
printf("Enter elements in the array:");
for(int i=0;i<8;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<8;i++){
        if(arr[i]>max1){
                max2=max1;
                max1=arr[i];
        }
        else if(arr[i]>max2&&arr[i]<max1){
                max2=arr[i];
        }
           }
printf("Largest number in the array is %d:",max1);
printf("\nSecond largest number in the arry is %d:",max2);
}

Output
Enter elements in the array:2
4
1
7
3
8
4
1
Largest number in the array is 8:
Second largest number in the arry is 7
```
## Write a program in C to find the second smallest element in an array.
```
#include <stdio.h>
int main(){
int arr[7];
printf("Enter elements in the array:");
for(int i=0;i<7;i++){
        scanf("%d",&arr[i]);
}
        int min=arr[0];
        int second_min=arr[0];
for(int i=0;i<7;i++){
        if(arr[i]<min){
                second_min=min;
                min=arr[i];
        }
        else if(arr[i]<second_min && arr[i]>min){
                second_min=arr[i];
        }
}
}
printf("Second minimum number %d",second_min);
Output
Enter elements in the array:7
2
8
6
4
3
7
Second minimum number 3
```
## 15 Write a program in C for adding two matrices of the same size
```
#include <stdio.h>
int main(){
int arr1[2][3];
int arr2[2][3];
int arr3[2][3];
printf("Enter elements:");
for(int i=0;i<2;i++){
 for(int j=0;j<3;j++){
        scanf("%d",&arr1[i][j]);
 }
}
printf("Enter elements:");
for(int i=0;i<2;i++){
        for(int j=0;j<3;j++){
                scanf("%d",&arr2[i][j]);
        }
}
for(int i=0;i<2;i++){
        for(int j=0;j<3;j++){
                arr3[i][j]=arr1[i][j]+arr2[i][j];
}

}
printf("sum of two matrices :\n");
for(int i=0;i<2;i++){
        for(int j=0;j<3;j++){
                printf("%d\t",arr3[i][j]);
}
printf("\n");
}
}
Output
Enter elements:5
2
1
1
2
1
Enter elements:1
1
1
1
1
1
sum of two matrices :
6	3	2	
2	3	2
```
## 16 Write a program in C to find the sum of the right diagonals of a matrix.
```
#include <stdio.h>
int main(){
int n;
int mat[30][30];
int sum=0;
printf("Enter the size of the matrix:");
scanf("%d",&n);
printf("Enter the elements in the matrix:");
for(int i=0;i<n;i++){
for(int j=0;j<n;j++){
        scanf("%d",&mat[i][j]);
}
}
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                if(i+j==n-1){
                        sum=sum+mat[i][j];
                       }
        }
}
        printf("sum of rightdiagonal matrix %d",sum);
}
output
Enter the size of the matrix:3
Enter the elements in the matrix:1
2
3
1
2
3
1
2
3
sum of rightdiagonal matrix 6
```
## 17.Write a program in C to find the sum of the left diagonals of a matrix
```
#include <stdio.h>
int main(){
int arr[20][20];
int n,sum=0;
printf("Size of the matrix:");
scanf("%d",&n);
printf("Enter elements in the matrix:");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                scanf("%d",&arr[i][j]);
        }
}
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                if(i==j){
                        sum=sum+arr[i][j];
                }
   }
        }
}
printf("Sum of left  diagonal is %d:",sum);
}
output
Size of the matrix:3
Enter elements in the matrix:1
2
3
1
2
3
1
2
3
Sum of left  diagonal is 6
```
## 18 Write a program in C to print or display the lower triangular of a given matrix.
```
#include <stdio.h>
int main(){
int arr[30][30];
int n;
printf("Enter the size if the matrix");
scanf("%d",&n);
printf("Enter the elements in the matrix:");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                scanf("%d",&arr[i][j]);
        }
}
printf("Original matrix\n");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                printf("%d ",arr[i][j]);
        }
}
        printf("\n");
}
printf("Lower triangle matrix is\n");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                if(i>=j)
                 printf("%d",arr[i][j]);
                else
                        printf(" ");
        }
        printf("\n");
}
}
output
Enter the size if the matrix3
Enter the elements in the matrix:1
2
3
4
5
6
7
8
9
Original matrix
1 2 3 
4 5 6 
7 8 9 
Lower triangle matrix is
1  
45 
789
```
## 19 Write a program in C to print or display an upper triangular matrix
```
#include <stdio.h>
int main(){
int arr[30][30];
int n;
printf("Enter the size if the matrix");
scanf("%d",&n);
printf("Enter the elements in the matrix:");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                scanf("%d",&arr[i][j]);
        }
}
printf("Original matrix\n");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                printf("%d ",arr[i][j]);
        }
        printf("\n");
}
printf("upper triangle matrix is\n");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                if(i<=j)
 printf("%d",arr[i][j]);

                else
                        printf(" ");

        }
        printf("\n");

}
}
output
Enter the size if the matrix3
Enter the elements in the matrix:1
2
3
4
5
6
7
8
6
Original matrix
1 2 3 
4 5 6 
7 8 6 
upper triangle matrix is
123
 56
  6
```
## 20 Write a program in C to calculate the determinant of a 3 x 3 matrix.
```
# include <stdio.h>
int main(){
int arr[3][3];
int determinant;
printf("Enter elements in the matrix:");
for(int i=0;i<3;i++){
        for(int j=0;j<3;j++){
        scanf("%d",&arr[i][j]);
        }
}
for(int i=0;i<3;i++){
        for(int j=0;j<3;j++){
                printf("%d ",arr[i][j]);
        }
        printf("\n");
}
determinant=arr[0][0]*((arr[1][1]*arr[2][2])-(arr[1][2]*arr[2][1]))-
            arr[0][1]*((arr[1][0]*arr[2][2])-(arr[2][0]*arr[1][2]))+
            arr[0][2]*((arr[1][0]*arr[2][1])-(arr[2][0]*arr[1][1]));
printf("Determinant matrix is %d",determinant);
}
Enter elements in the matrix:1
2
3
1
2
3
1
2
3
1 2 3 
1 2 3 
1 2 3 
Determinant matrix is 0
```
##
