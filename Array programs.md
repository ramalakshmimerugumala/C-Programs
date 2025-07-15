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
## 21 Write a program in C to accept two matrices and check whether they are equal.
```
#include <stdio.h>
int main(){
int arr1[3][3];
int arr2[3][3];
int equal=1;
printf("Enter the elements in the first array:");
for(int i=0;i<3;i++){
        for(int j=0;j<3;j++){
                scanf("%d",&arr1[i][j]);
        }
}
printf("Enter the elements in the array2");
for(int i=0;i<3;i++){
        for(int j=0;j<3;j++){
                scanf("%d",&arr2[i][j]);
        }
}
for(int i=0;i<3;i++){
        for(int j=0;j<3;j++){
                if(arr1[i][j]!=arr2[i][j]){
                        equal=0;
                        break;
        }
}

}
if(equal)
        printf("Two array are equal");
else
        printf("Two arrays are not equal");
}
output
Enter the elements in the first array:1
2
3
1
4
5
6
8
0
Enter the elements in the array22
3 
5
1
7
8
2
6
9
Two arrays are not equal
```
## 22 Write a program in C to find the missing number in a given array. There are no duplicates in
the list.
```
#include <stdio.h>
int main(){
int arr[100];
int n,sum=0;
int expected_sum=0;
printf("Enter size of an array");
scanf("%d",&n);
printf("Enter elements in the array:");
for(int i=0;i<n;i++){
scanf("%d",&arr[i]);
}
for(int i=0;i<n;i++){
        sum=sum+arr[i];
}

        expected_sum=(n+1)*(n+2)/2;
        int missing=expected_sum-sum;
printf("Missing number is %d\n",missing);
}
output
Enter size of an array5
Enter elements in the array:1
2
4
5
6
```
## 23 Write a program in C to find the majority element of an array.
(A majority element in an array A[] of size n is an element that appears more than n/2 times
(and hence there is at most one such element).
```
#include <stdio.h>
int main(){
        int arr[100];
        int n;
        printf("Enter the size of the array:");
        scanf("%d",&n);
        printf("Enter the elements in the array:");
        for(int i=0;i<n;i++){
                scanf("%d",&arr[i]);
        }
        for(int i=0;i<n;i++){
                int count=0;
                for(int j=0;j<n;j++){
                if(arr[i]==arr[j])
                        count ++;
                }

                if(count>n/2){
                        printf("Majority of elements %d",arr[i]);
                        return 0;
                }
        }
                printf("No majority elements in the arry");
}
output
Enter the size of the array:5
Enter the elements in the array:1
1
1
1
2
Majority of elements 1
```
## 24 Write a program in C to find the two repeating elements in a given array.
```
#include <stdio.h>
int main(){
int arr[50];
int n;
int found=0;
printf("Enter size of an array:");
scanf("%d",&n);
printf("Enter elements in the array");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<n;i++){
        int count=1;
        if(arr[i]==-1)
                continue;
        for(int j=i+1;j<n;j++){
                if(arr[i]==arr[j]){
                        count++;
                        arr[j]=-1;
                }

        }
        if(count>1){
          printf(" repeating elements in the array are %d",arr[i]);
                found++;
        }
}
if(found==0)
printf("No repeating elemnts:");
}                                       
Output:
Enter size of an array:6
Enter elements in the array1
2
3
4
1
2
1 2
```
## 25 Write a program to check if a given element is present in an array.
```
#include <stdio.h>
int main(){
int arr[50];
int n;
int found=0;
int number;
printf("Enter the size of an array:");
scanf("%d",&n);
printf("Enter the elements in the array:");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
printf("Enter a number:");
scanf("%d",&number);
for(int i=0;i<n;i++){
                if(arr[i]==number){
                        found=1;
                }
        }

            if(found){
                printf("The number %d is present in the array",number);
            }
      else{
                printf("The number %d is not present in the array ",number);
        }

}
output
Enter the size of an array:5
Enter the elements in the array:1
2
3
4
5
Enter a number:2
The number 2 is present in the array
```
## 26 Write a program to count the number of even and odd elements in an array
```
#include <stdio.h>
int main(){
int arr[10];
int even,odd;
even=0;
odd=0;
printf("Enter elements in the array:");
for(int i=0;i<10;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<10;i++){
        if(arr[i]%2==0){
          even++;
        }

        else{
           odd++;
        }
}
printf("count of the even numbers :%d\n",even);
printf("count of the odd numbers :%d\n",odd);

}
output
Enter elements in the array:1
2
3
5
7
2
8
9
1
7
count of the even numbers :3
count of the odd numbers :7
```
## 27  Print Square of Array Elements in C
```
#include <stdio.h>
int main(){
int arr[50];
int n;
printf("Enter the size of an array:");
scanf("%d",&n);
printf("Enter the elements in the array:");
for(int i=0;i<n;i++){
scanf("%d",&arr[i]);
}
printf("Square of elements in the array:");
for(int i=0;i<n;i++){
        int square=arr[i]*arr[i];
        printf("%d ",square);
}
}
output
Enter the size of an array:5
Enter the elements in the array:1
2
3
4
5
Square of elements in the array:1 4 9 16 25
```
## 28 Print Ascii Values using Array in C
```
#include <stdio.h>
int main(){
int n;
char ch[500];
printf("Enter how many  character u want:");
scanf("%d",&n);
printf("Enter a character:");
for(int i=0;i<n;i++){
scanf(" %c",&ch[i]);
}
for(int i=0;i<n;i++){
printf("Ascii value of a character '%c' is  %d\n",ch[i],ch[i]);
}
}
output
Enter how many  character u want:5
Enter a 5 character:
4
A
a
r
R
Ascii value of a character '4' is  52
Ascii value of a character 'A' is  65
Ascii value of a character 'a' is  97
Ascii value of a character 'r' is  114
Ascii value of a character 'R' is  82
```
## 29.C Program To Find Two Elements whose Sum is Closest to Zero
```
#include <stdio.h>
#include <stdlib.h>
int main(){
int arr[300];
int n;
int num1=0;
int num2=0;
int min_num=999999;
printf("Enter size of an array:");
scanf("%d",&n);
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<n;i++){
        for(int j=i+1;j<n;j++){
                int sum=arr[i]+arr[j];
                if(abs(sum)<min_num){
                     min_num=abs(sum);
                     num1=arr[i];
                     num2=arr[j];
                }
        }
}
printf("the numbers which are closest to the zero are %d and %d\n",num1,num2);
printf("Sum of the two numbers are %d",num1+num2);
}
output
Enter size of an array:5
Enter the elements in the array5
6
-2
3
-1
the numbers which are closest to the zero are -2 and 3
Sum of the two numbers are 1
```
## 30.C Program to Print all Non Repeated Elements in an Array
```
#include <stdio.h>
int main(){
int arr[50];
int n;
int nonrepeated=1;
int count=0;
printf("Enter the size of the array:");
scanf("%d",&n);
printf("Enter the elements in the array");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<n;i++){
        count=0;
        for(int j=0;j<n;j++){
                if (i!=j && arr[i]==arr[j]){
                        count++;
        }
        }
        if(count==0){
                printf(" non repeated elements %d",arr[i]);
                nonrepeated=0;
        }
}
if(nonrepeated==1){
        printf("No non repeated elements in the array");
}
}
output
Enter the size of the array:5
Enter the elements in the array1
2
3
1
2
 nonrepeated elements 3
```
## 31 Write a program to write all the elements of 2-D Array into !-D Array in row wise
```
#include <stdio.h>
int main(){
int arr[100][100];
int arr1d[100];
int index=0;
int n;
printf("Enter the size of an array:");
scanf("%d",&n);
printf("Enter the elements in the array:");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                scanf("%d",&arr[i][j]);
        }
}
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
                printf("%d ",arr[i][j]);
              }
        printf("\n");
}
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
    arr1d[index++]=arr[i][j];
        }
}
printf("1D array in the row wise is:\n");
for(int i=0;i<index;i++){
 printf("%d",arr1d[i]);
}
}
output
Enter the size of an array:2
Enter the elements in the array:1
2
1
2
1 2 
1 2 
1D array in the row wise is:
1212
```
## 32 Write a program to check if elements of an array are distinct or not.
```
#include <stdio.h>
int main(){
int arr[100];
int n;
int count;
printf("Enter the size of an array:");
scanf("%d",&n);
printf("Enter the elemnts in the array:");
for(int i=0;i<n;i++){
scanf("%d",&arr[i]);
}
for(int i=0;i<n;i++){
        count=0;
        for(int j=0;j<n;j++){
                if(i!=j&&arr[i]==arr[j]){
                        count++;
                }
 }
}
        if(count==0){
                printf("Elements are distinct");
        }
        if(count==1){
                printf("Elements are non distinct");
        }
}
output
Enter the size of an array:4
Enter the elemnts in the array:1
2
1
2
Elements are non distinct
```
## 33 Write a program to remove duplicate elements from a sorted array
```
#include <stdio.h>
int main(){
int arr[100];
int n;
int count;
printf("Enter the size of an array:");
scanf("%d",&n);
printf("Enter the elements in the array:");
for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
}
for(int i=0;i<n;i++){
        for(int j=i+1;j<n;j++){
                if(arr[i]>arr[j]){
                        int temp=arr[i];
                        arr[i]=arr[j];
                        arr[j]=temp;
                       }
        }
}
printf("sorted array:");
for(int i=0;i<n;i++){
        printf("%d",arr[i]);
}
for(int i=0;i<n;i++){
        int count=0;
        for(int j=i+1;j<n;j++){
                if(arr[i]==arr[j]){
                        for(int k=j;k<n;k++){
                                arr[k]=arr[k+1];
                        count ++;
                }
                n--;
                j--;
 }
}
}
printf("\nAfter removing duplicates:");
for(int i=0;i<n;i++){
        printf("%d",arr[i]);
}
}
output
Enter the size of an array:5
Enter the elements in the array:1
3
1
2
4
sorted array:11234
After removing duplicates:1234
```
## 34. Write a program to write whether a matrix is symmetric or not
```
#include <stdio.h>
int main(){
 int arr[3][3];
int  issymmetric=1;
 printf("Enter elements in the matrix");
 for(int i=0;i<3;i++){
         for(int j=0;j<3;j++){
                 scanf("%d",&arr[i][j]);
         }
 }
 for(int i=0;i<3;i++){
         for(int j=0;j<3;j++){
                 printf("%d",arr[i][j]);
         }
         printf("\n");
 }
 for(int i=0;i<3;i++){
         for(int j=0;j<3;j++){
                 if(arr[i][j]!=arr[j][i]){
                        issymmetric=0;

                 }
                      }

                 }
         }
 if(issymmetric){
         printf("The matrix is symmetric matrix");
 }
 else{
         printf("The matrix is not symmetric");
 }
}

output
Enter elements in the matrix1
2
3
2
5
6
3
6
9
123
256
369
The matrix is symmetric matrix
```
## 35 Write a program in C for the multiplication of two square matrices.
```
#include <stdio.h>
int main(){
int arr1[100][100];
int arr2[100][100];
int m,n;
int result[100][100];
printf("Enter the size of m");
scanf("%d",&m);
printf("Enter the size of n");
scanf("%d",&n);
printf("Enter the elements ");
for(int i=0;i<m;i++){
        for(int j=0;j<m;j++){
        scanf("%d",&arr1[i][j]);
}
}
printf("Enter the elements ");
for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
        scanf("%d",&arr2[i][j]);
}
}
for(int i=0;i<m;i++){
        for(int j=0;j<m;j++){
                result[i][j]=0;
        }
}
for(int i=0;i<m;i++){
        for(int j=0;j<m;j++){
                for(int k=0;k<m;k++){
                result[i][j]+=arr1[i][k]*arr2[k][j];
        }
}
}
printf("Resultant matrix is");
for(int i=0;i<m;i++){
        for(int j=0;j<m;j++){
                printf("%d ",result[i][j]);
        }
        printf("\n");
}
}
output
Enter the size of m3
Enter the size of n3
Enter the elements 1
2
3
1
2
3
1
2
3
Enter the elements 1
2
3
1
2
3
1
2
3
Resultant matrix is6 12 18 
6 12 18 
6 12 18
```
## 36 Write a program to find the sum of rows and columns of a 2-d array and store the sums in
the same array.
```
#include <stdio.h>
int main(){
int arr[5][6];
int total=0;
printf("Enter the elements in the array:");
for(int i=0;i<4;i++){
        for(int j=0;j<5;j++){
                scanf("%d",&arr[i][j]);
        }
}
for(int i=0;i<4;i++){
        int rowsum=0;
        for(int j=0;j<5;j++){
                rowsum+=arr[i][j];
        }
        arr[i][5]=rowsum;
        total+=rowsum;
}
for(int j=0;j<5;j++){
        int colsum=0;
        for(int i=0;i<4;i++){
                colsum+=arr[i][j];
        }
        arr[4][j]=colsum;
}
arr[4][5]=total;
printf("Final matrix\n");
for(int i=0;i<5;i++){
        for(int j=0;j<6;j++){
                printf("%d\t",arr[i][j]);
        }
        printf("\n");
}
}
output
Enter the elements in the array:1
2
2
1
4
5
4
3
2
5
6
3
2
1
4
3
5
4
2
3
Final matrix
1	2	2	1	4	10	
5	4	3	2	5	19	
6	3	2	1	4	16	
3	5	4	2	3	17	
15	14	11	6	16	62
```
## 37.
