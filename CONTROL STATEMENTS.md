### CONTROL STATEMENTS:

```C

1.WRITE A C PROGRAM TO ACCEPT TWO INTEGERS AND CHECK WHETHER THEY ARE EQUAL OR NOT?
#include<stdio.h>
void checkequality(int a,int b)
{
        if(a==b)
        {
                printf("the numbers are equal.\n");
        }
        else
        {
                printf("the numbers are not equal.\n");
        }
}
int main()
{
        int num1,num2;
        printf("enter num1,num2 values\n");
        scanf("%d%d",&num1,&num2);
        checkequality(num1,num2);
        return 0;
}
/************************************************************************************************************************************/
//2.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS EVEN OR ODD?
#include<stdio.h>
int evenodd(int num)
{
        if(num%2==0)
        {
                printf("even number\n");
        }
        else
        {
                printf("odd number\n");
        }
}
int main()
{
        int n;
        printf("enter n value\n");
        scanf("%d",&n);
        evenodd(n);
        return 0;
}
/******************************************************************************************************************************/
//3.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS POSITIVE OR NEGATIVE?
#include<stdio.h>
int checksign(int num)
{
        if(num>0)
        {
                printf("positive number\n");
        }
        else
        {
                printf("negative number\n");
        }
}
int main()
{
        int n;
        printf("enter the n value\n");
        scanf("%d",&n);
        checksign(n);
        return 0;
}
/*****************************************************************************************************************/
//3a.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS POSITIVE OR NEGATIVE?
#include<stdio.h>
int checksign(int num)
{
        if(num>0)
        {
                printf("positive number\n");
        }
        else if(num<0)
        {
                printf("negative number\n");
        }
else
{
printf("zero number");
}
}
int main()
{
        int n;
        printf("enter the n value\n");
        scanf("%d",&n);
        checksign(n);
        return 0;
}
/*******************************************************************************************************************/
//4.WRITE A C PROGRAM TO READ THE AGE OF A CANDIDATE AND DETERMINE WHETHER HE IS ELIGIBLE TO CAST HIS/HER OWN VOTE?
#include<stdio.h>
int checkeligible(int age)
{
        if(age>=18)
        {
                printf("you are eligible votes\n");
        }
        else
        {
                printf("you are not eligible votes\n");
        }
}
int main()
{
        int age;
        printf("enter the age\n");
       scanf("%d",&age);
       checkeligible(age);
       return 0;
}
/*********************************************************************************************************************/

//5.WRITE A C PROGRAM TO FIND WHETHER A GIVEN YEAR IS A LEAP YEAR OR NOT?
#include<stdio.h>
void checkleapyear(int year)
{
        if((year%4==0)&&(year%100!=0)||(year%400==0))
        {
                printf("leap year \n");
        }
        else
        {
                printf("not a leap year\n");
        }
}
int main()
{
        int year;
        printf("enter the year\n");
        scanf("%d",&year);
        checkleapyear(year);
        return 0;
}
/****************************************************************************************************************/
//6.WRITE A C PROGRAM TO READ THE VALUE OF AN INTEGER M AND DISPLAY THE VALUE OF N IS 1 WHEN M IS LARGER THAN 0, 0 WHEN M IS 0 AND -1 WHEN M IS LESS THAN 0
#include<stdio.h>
int displayvalues(int m)
{
        int n;
        if(m>0)
{
        n=1;
}
else if(m==0)
{
        n=0;
}
else
{
        n=-1;
}
printf("the value n is :%d\n",n);
}
int main()
{
        int m;
        printf("enter the m value\n");
        scanf("%d",&m);
        displayvalues(m);
        return 0;
}

```                         





