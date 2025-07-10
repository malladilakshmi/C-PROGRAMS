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
/******************************************************************************************************/
7.WRITE A C PROGRAM TO FIND THE LARGEST OF THREE NUMBERS?
#include<stdio.h>
int largestofthreenumbers(int a,int b,int c)
{
        int max=a;
        if(b>max)
        {
                max=b;
        }
        if(c>max)
        {
                max=c;
        }
        return max;
}
int main()
{
        int num1,num2,num3,result;
        printf("enter three numbers:\n");
        scanf("%d%d%d",&num1,&num2,&num3);
        result=largestofthreenumbers(num1,num2,num3);
        printf("the largest number is %d\n",result);
        return 0;
}
                                  (or)
#include <stdio.h>
int findLargest(int a, int b, int c) {
    if (a >= b && a >= c) {
        return a;
    } else if (b >= a && b >= c) {
        return b;
    } else {
        return c;
    }
}

int main() {
    int num1, num2, num3, largest;
   printf("Enter three numbers:\n");
    scanf("%d %d %d", &num1, &num2, &num3);
   largest = findLargest(num1, num2, num3);
   printf("The largest number is %d\n", largest);
   return 0;
}
                                           (or)

#include <stdio.h>
int findLargest(int a, int b, int c) {
    return (a > b) ? ((a > c) ? a : c) : ((b > c) ? b : c);
}
int main() {
    int num1, num2, num3, largest;
    printf("Enter three numbers:\n");
    scanf("%d %d %d", &num1, &num2, &num3);
    largest = findLargest(num1, num2, num3);
    printf("The largest number is %d\n", largest);
return 0;
}
 Ternary Operator Syntax:
(condition) ? (if true) : (if false);
return (a > b) 
       ?          ((a > c) ? a : c) 
       :          ((b > c) ? b : c);
/***************************************************************************************************************************/
8.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS A VOWEL OR CONSONANT?
#include<stdio.h>
#include<ctype.h>
int isvowel(char ch)
{
        ch=tolower(ch);
        if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u')
        {
                return 1;
        }
        else
        {
                return 0;
        }
}
int main()
{
        char ch;
        printf("enter a character:");
        scanf("%c",&ch);
        if((ch>='A' && ch<='Z')||(ch>='a'||ch<='z'))
        {
                if(isvowel(ch))
                {
                        printf("%c is a vowel.\n",ch);
                }
                else
                {
                        printf("is a consonant.\n");
                }
        }
                else
                {
                        printf("is not an alphabet.\n");
                }
                return 0;
        }
/**************************************************************************************************************/
/****************************************************************************************************************************/
12.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS UPPERCASE OR LOWERCASE?
#include<stdio.h>
#include<ctype.h>
int loweruppercase(char ch)
{
        if(isupper(ch))
                        {
                        printf("is an uppercase letter");
                        }
        else if(islower(ch))
        {
                printf("is a lowercase letter");
        }
        else
        {
                printf("is not a letter");
        }
}
int main()
{
        char ch;
        printf("enter the letter\n");
        scanf("%c",&ch);
        loweruppercase(ch);
        return 0;
}
/*********************************************************************************************************************************/
10.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS AN ALPHABET OR NOT?
#include<stdio.h>
#include<ctype.h>
void alphabet(char ch)
{
        if(isalpha(ch))
                        {
                                printf("is a alphabet\n");
                        }
        else
        {
                printf("is not a alphabet\n");
        }
}
int main()
{
        char ch;
        printf("enter the letter\n");
        scanf("%c",&ch);
        alphabet(ch);
        return 0;
}
/***********************************************************************************************************/

```                         





