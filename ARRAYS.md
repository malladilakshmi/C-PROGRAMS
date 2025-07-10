### ARRAYS:

```c

1. Write a program in C to store elements in an array and print them.
#include<stdio.h>
void arrayelements(int arr[],int n)
{
        for(int i=0;i<n;i++)
        {
                printf("enter the element %d:",i+1);
                scanf("%d",&arr[i]);
                printf("%d\n",arr[i]);
}
}
int main()
{
        int m;
        int arr[m];
        printf("enter the elements\n");
        scanf("%d",&m);
        arrayelements(arr,m);
        return 0;
}
                                                      (or)
#include<stdio.h>
void arrayelements(int arr[],int n)
{
        int i;
        for(i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        printf("print the array elements\n");
        for(i=0;i<n;i++)
        {
                printf("%d\n",arr[i]);
        }
}
int main()
{
        int m;
        int arr[m];
        printf("enter the number of elements\n");
        scanf("%d",&m);
        arrayelements(arr,m);
        return 0;
}
/*******************************************************************************************/
2.write a program to c print the array elements in single line?
#include<stdio.h>
void singlearray(int arr[],int n)
{
        int i;
        printf("enter elements\n");
        for(i=0;i<n;i++)
        {
        scanf("%d",&arr[i]);
        }
        printf("array elements in single line:\n");
           for(i=0;i<n;i++)
           {
                   printf("%d",arr[i]);
           }
}
int main()
{
        int m;
        int arr[m];
        printf("enter the array elements\n");
        scanf("%d",&m);
        singlearray(arr,m);
        return 0;
}
/***********************************************************************************************/

```
