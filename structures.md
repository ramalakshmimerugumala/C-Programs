## 1. Structute pointers
```
#include <stdio.h>
struct book{
        int rollno;
        char name[20];
        float marks;
};
int main(){
        struct book s;
        struct book *ptr=&s;
       printf("Enter the info of s");
       scanf("%d %s %f",&ptr->rollno,ptr->name,&ptr->marks);
       printf("%d %s %f\n",ptr->rollno,ptr->name,ptr->marks);
       printf("Information Again\n");
       scanf("%d %s %f",&(*ptr).rollno,(*ptr).name,&(*ptr).marks);
       printf("%d %s %f",(*ptr).rollno,(*ptr).name,(*ptr).marks);
}
output
Enter the info of s1 ram 90
1 ram 90.000000
Information Again
1 moon 98
1 moon 98.000000
```
## 2.. Define a union to store either an integer or a floatingpoint number. Write a function to accept the type of data (integer or float) and then read the corresponding value from the user. Store the value in the union and print it
```
#include <stdio.h>
union number{
        int i;
        float f;
};
int readandprint(int choice){
        union number n;
        if(choice==1){
                printf("Enter a integer");
                scanf("%d",&n.i);
                printf("you entered number=%d",n.i);
        }
        else if(choice==2){
                printf("Enter a number");
                scanf("%f",&n.f);
                printf("you entererd number=%.3f",n.f);
        }
else{
                printf("Invalid choice");
        }
}
int main(){
int choice;
printf("Enter a choice");
scanf("%d",&choice);
readandprint(choice);
}
output
Enter a choice2
Enter a number6
you entererd number=6.000
```
## 3 Define a structure to represent a point in 2D space with x and y coordinates (both integers). Write a function to check if two points are equal (have the same x and y coordinates)
```
#include <stdio.h>
struct point{
        int x;
        int y;
};
int isequal(struct point p1,struct point p2){
        if(p1.x==p2.x && p1.y==p2.y){
                return 1;
        }
        else{
                return 0;
        }
}
int main(){
struct point p1,p2;
printf("Enter the coordinates of point1");
scanf("%d %d",&p1.x,&p1.y);
if(isequal(p1,p2)) {
   printf("Both are equal");
   }
   else{
   printf("Both are not equal");
   }
   }
output
Enter the coordinates of point11 2
Enter the coordinates of point 21 2 
Both are equal
```
## 4 Create a structure to represent a book with the following members: title (string), author (string),ISBN (long int), and number of pages (int). Write a function to accept details of a book from the user and store them in a structure variable.
```
#include <stdio.h>
struct book{
        char title[20];
        char author[20];
        long int isbn;
        int pages;
};
void acceptbook(struct book *b){
        printf("Enter title\n");
        scanf("%s",(*b).title);
        printf("Enter author\n");
        scanf("%s",(*b).author);
        printf("Enter isbn\n");
        scanf("%ld",&(*b).isbn);
        printf("Enter pages\n");
        scanf("%d",&(*b).pages);
}
int main(){
        struct book mybook;
        acceptbook(&mybook);
        printf("Book details\n");
        printf("title:%s\n",mybook.title);
        printf("author:%s\n",mybook.author);
        printf("isbn:%ldi\n",mybook.isbn);
        printf("pages:%d\n",mybook.pages);
}
output
Enter title
c_programming
Enter author
Denni
Enter isbn
123455678
Enter pages
580
Book details
title:c_programming
author:Denni
isbn:123455678i
pages:580
```
## 5.Define a union to represent the size of a product, which can be specified in centimeters, inches, or feet. Write a function to convert the size from one unit to another (e.g., centimeters to inches). 
```
#include <stdio.h>
union size{
        float cm;
        float inch;
        float feet;
};
float convert(float value,char from,char to){
        float cm;
        if(from=='c')
                cm=value;
        else if(from=='i')
                cm=value*2.54;
        else if(from=='f')
                cm=value*30.54;
        if(to=='c')
                return cm;
        if(to=='i')
return cm/2.54;
        if(to=='f')
                return cm/30.48;
        return -1;
        }
int main(){
        union size s;
        char from,to;
        printf("Enter the size value");
        scanf("%f",&s.cm);
        printf("Enter from unit");
        scanf(" %c",&from);
        printf("Enter to unit(c,i,f)");
        scanf(" %c",&to);
        float result=convert(s.cm,from,to);
        printf("Converted value=%.2f\n",result);
}
output
Enter the size value12
Enter from unitc
Enter to unit(c,i,f)i
Converted value=4.72
```
## Define a structure to represent a date with day, month, and year (all integers). Write a function to check if a given year is a leap year
```
#include <stdio.h>
struct date{
        int day;
        int month;
        int year;
};
int isleapyear(int year){
        if(year %400==0)
                return 1;
        else if(year %100==0)
                return 0;
        else if(year %4==0)
                return 1;
        else return 0;
}
int main(){
        struct date d;
printf("Enter day month year:");
        scanf("%d %d %d",&d.day,&d.month,&d.year);
        if(isleapyear(d.year))
                printf("%d is a leap year",d.year);
        else
                printf("%d is not a leap year",d.year);
}
output
Enter day month year:4 12 1990
1990 is not a leap year
```
##  4. Define a structure to represent a complex number with real and imaginary parts (both floats). Write a function to add two complex numbers represented by structures
```
#include <stdio.h>
struct complex{
        float real;
        float imag;
};
struct complex addcomplex(struct complex c1,struct complex c2){
        struct complex sum;
        sum.real=c1.real+c2.real;
        sum.imag=c1.imag+c2.imag;
        return sum;
}
int main(){
        struct complex num1,num2,result;
        printf("Enter first complex number");
        scanf("%f %f",&num1.real,&num1.imag);
        printf("Enter second complex number");
        scanf("%f %f",&num2.real,&num2.imag);
        result=addcomplex(num1,num2);
        printf("sum=%.2f+%.2fi\n",result.real,result.imag);
}
output
Enter first complex number2 4
Enter second complex number3 6
sum=5.00+10.00i
```
## 



