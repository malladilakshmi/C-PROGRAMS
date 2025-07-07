```C


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
/****************************************************************************************************************************/

```
