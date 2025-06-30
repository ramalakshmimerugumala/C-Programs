## .WRITE A C PROGRAM TO FIND THE SUM OF ELEMENTS IN AN ARRAY USING A WHILE LOOP?
program
## 1️⃣ Program to Find the Sum of Elements in an Array Using `while` Loop

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

# 2 Reverse of an array
Program
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

# 3.
