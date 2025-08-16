## Structute pointers
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
