## Decimal to roman
```
int decimal(int n,int k,char ch){
        while(n>=k){
                printf("%c",ch);
                n=n-k;
        }
        return n;
}
int main(){
 int number;
 printf("Enter a number");
 scanf("%d",&number);
 if(number>=1000)
         number=decimal(number,1000,'M');
 if(number>=500)
         number=decimal(number,500,'D');
 if(number>=100)
         number=decimal(number,100,'C');
 if(number>=50)
         number=decimal(number,50,'L');
 if(number>=10)
         number=decimal(number,10,'X');
if(number>=5)
         number=decimal(number,5,'V');
if(number>=1)
        number=decimal(number,1,'I');
   printf("\n");
   return 0;
}
output
Enter a number6
VI
```
       
