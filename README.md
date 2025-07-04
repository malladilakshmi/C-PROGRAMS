### C-PROGRAMS:
### OPERATORS:

```C
1.write a function to check if a given string is empty or not?
int is_empty(char* str) {
    if(str[0]=='\0')
    {
        return 1;
    }
    else
    {
        return 0;
    }

    char input[100];
    printf("enter a string");
    scanf("%s\n",input);
    printf("%d\n",is_empty(""));
    printf("%d\n",is_empty("test"));
    }
/*******************************************************************/
2.write a c program to covert the string into integer?
#include<stdio.h>
#include<stdlib.h>
int main()
{
char str[]="12345";
for(int i=0;str[i];i++)
{
result=result*10+str[i]-48;
}
printf("%d\n",result);
}
/***********************************************************************/
3.write a c program to print the pattern?
*****
****
***
**
*
#include <stdio.h>

int main() {
    int i, j, rows;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (i = 1; i <= rows; i++) {
        for (j = 1; j <=rows-i; j++) {
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
/****************************************************************************/
4.write a c program to print the pattern?
*
**
***
****
*****
#include<stdio.h>
int main()
{
        int i,j,rows;
        printf("enter number of rows");
        scanf("%d",&rows);
        for(i=0;i<rows;i++)
        {
                for(j=0;j<i;j++)
                {
                        printf("*");
                }
                printf("\n");
        }
}
/*******************************************************************************/
5.write a c program to find odd occurring number when all are even?
#include <stdio.h>

int findOddOccurring(int arr[], int size) {
    int result = 0;

    for (int i = 0; i < size; i++) {
        result ^= arr[i];  // XOR operation
    }

    return result;
}

int main() {
    int arr[] = {2, 3, 2, 4, 4, 3, 5};  // 5 occurs odd number of times
    int size = sizeof(arr) / sizeof(arr[0]);

    int odd = findOddOccurring(arr, size);
    printf("The odd occurring number is: %d\n", odd);

    return 0;
}
/*******************************************************************************/
6.write a c program to find max and min elements in array using pointer?
#include <stdio.h>

void findMaxMin(int *arr, int size, int *max, int *min) {
    *max = *min = *arr;  // Initialize with the first element

    for (int i = 1; i < size; i++) {
        if (*(arr + i) > *max) {
            *max = *(arr + i);
        }
        if (*(arr + i) < *min) {
            *min = *(arr + i);
        }
    }
}

int main() {
    int arr[] = {7, 2, 9, 4, 5};
    int size = sizeof(arr) / sizeof(arr[0]);
    int max, min;

    findMaxMin(arr, size, &max, &min);

    printf("Maximum element: %d\n", max);
    printf("Minimum element: %d\n", min);

    return 0;
}
/****************************************************************************************/
7.write a c program swap all even and odd bits?
#include <stdio.h>

unsigned int swapEvenOddBits(unsigned int x) {
    unsigned int even_mask = 0xAAAAAAAA; // Mask for even bits: 101010...10 (binary)
    unsigned int odd_mask  = 0x55555555; // Mask for odd bits:  010101...01 (binary)

    unsigned int even_bits = x & even_mask;
    unsigned int odd_bits  = x & odd_mask;

    even_bits >>= 1;
    odd_bits  <<= 1;

    return (even_bits | odd_bits);
}

int main() {
    unsigned int num = 23; // Binary: 00010111
    unsigned int result = swapEvenOddBits(num);
    printf("Original: %u\nSwapped:  %u\n", num, result);
    return 0;
}
/*********************************************************************************************/
8.write a c program for check if the number is a power of 2?
#include<stdio.h>
int ispoweroftwo(int n)
{
        return n>0&&(n&n-1)==0;
}
int main()
{
        int num;
        printf("enter number");
        scanf("%d",&num);
        if(ispoweroftwo(num))
                        {
        printf("%d is a power of 2 .\n",num);
}
else
{
        printf("%d is a not power of 2.\n",num);
        }

return 0;
}
/*******************************************************************************************/
9.write c program that enters temperature in celsius and converts that into fahrenheit?
#include <stdio.h>

// Function to convert Celsius to Fahrenheit
float convertToFahrenheit(float celsius) {
    return (celsius * 9.0 / 5.0) + 32.0;
}

int main() {
    float celsius, fahrenheit;

    // Ask user for temperature in Celsius
    printf("Enter temperature in Celsius: ");
    scanf("%f", &celsius);

    // Call function to convert
    fahrenheit = convertToFahrenheit(celsius);

    // Display result
    printf("%.2f Celsius = %.2f Fahrenheit\n", celsius, fahrenheit);

    return 0;
}
/***********************************************************************************************/
10.Write a program that accepts the radius of a circle and calculates the area and perimeter of
that circle in c in function formate?
#include <stdio.h>
#define PI 3.14159

// Function to calculate area
float calculateArea(float r) {
    return PI * r * r;
}

// Function to calculate perimeter (circumference)
float calculatePerimeter(float r) {
    return 2 * PI * r;
}

int main() {
    float radius, area, perimeter;

    // Input radius
    printf("Enter the radius of the circle: ");
    scanf("%f", &radius);

    // Function calls
    area = calculateArea(radius);
    perimeter = calculatePerimeter(radius);

    // Output results
    printf("Area of the circle: %.2f\n", area);
    printf("Perimeter (Circumference) of the circle: %.2f\n", perimeter);

    return 0;
}
/*****************************************************************************************************************/
11.Write a program to accept a number in decimal and print the number in octal and
hexadecimal.
#include <stdio.h>

// Function to print number in octal
void printOctal(int num) {
    printf("Octal: %o\n", num);
}

// Function to print number in hexadecimal
void printHexadecimal(int num) {
    printf("Hexadecimal: %X\n", num);  // Use %x for lowercase
}

int main() {
    int decimal;

    // Input from user
    printf("Enter a decimal number: ");
    scanf("%d", &decimal);

    // Function calls
    printOctal(decimal);
    printHexadecimal(decimal);

    return 0;
}
/**************************************************************************************************************/
12.43. Write a program to accept any number and print the value of remainder after dividing it by
3.
#include <stdio.h>

int main() {
    int number, remainder;

    // Input number from user
    printf("Enter a number: ");
    scanf("%d", &number);

    // Calculate remainder
    remainder = number % 3;

    // Display result
    printf("Remainder after dividing %d by 3 is: %d\n", number, remainder);

    return 0;
}
/***********************************************************************************************************/
13. Accept any two numbers, if the first number is greater than second then print the difference
of these two numbers, otherwise print their sum. Write this program using a ternary operator.
#include <stdio.h>

// Function to calculate result using ternary operator
int calculateResult(int a, int b) {
    return (a > b) ? (a - b) : (a + b);
}

int main() {
    int num1, num2, result;

    // Input two numbers
    printf("Enter first number: ");
    scanf("%d", &num1);
    
    printf("Enter second number: ");
    scanf("%d", &num2);

    // Call function
    result = calculateResult(num1, num2);

    // Display result
    printf("Result: %d\n", result);

    return 0;
}
/**********************************************************************************************************/
14. Write a program that accepts marks in five subjects and calculates the total percentage
marks.
#include <stdio.h>

// Function to calculate total marks
float calculateTotal(float s1, float s2, float s3, float s4, float s5) {
    return s1 + s2 + s3 + s4 + s5;
}

// Function to calculate percentage
float calculatePercentage(float total) {
    return (total / 500.0) * 100.0;  // assuming each subject is out of 100
}

int main() {
    float sub1, sub2, sub3, sub4, sub5;
    float total, percentage;

    // Accept marks for five subjects
    printf("Enter marks for subject 1: ");
    scanf("%f", &sub1);
    printf("Enter marks for subject 2: ");
    scanf("%f", &sub2);
    printf("Enter marks for subject 3: ");
    scanf("%f", &sub3);
    printf("Enter marks for subject 4: ");
    scanf("%f", &sub4);
    printf("Enter marks for subject 5: ");
    scanf("%f", &sub5);

    // Function calls
    total = calculateTotal(sub1, sub2, sub3, sub4, sub5);
    percentage = calculatePercentage(total);

    // Output
    printf("\nTotal Marks: %.2f\n", total);
    printf("Percentage: %.2f%%\n", percentage);

    return 0;
}
/*******************************************************************************************************/
15.Can you swap two variables without using a temporary variable? Show the code.
#include <stdio.h>

// Swap using arithmetic
void swap_arithmetic(int *a, int *b) {
    *a = *a + *b;
    *b = *a - *b;
    *a = *a - *b;
}

// Swap using XOR
void swap_xor(int *a, int *b) {
    *a = *a ^ *b;
    *b = *a ^ *b;
    *a = *a ^ *b;
}

int main() {
    int a = 5, b = 10;

    printf("Original values:\na = %d, b = %d\n", a, b);

    // Swap using arithmetic
    swap_arithmetic(&a, &b);
    printf("\nAfter swap_arithmetic:\na = %d, b = %d\n", a, b);

    // Swap back for XOR example
    swap_arithmetic(&a, &b);

    // Swap using XOR
    swap_xor(&a, &b);
    printf("\nAfter swap_xor:\na = %d, b = %d\n", a, b);

    return 0;
}
(or)
#include <stdio.h>

// Function to swap two integers using arithmetic, returning the result as a struct
struct Pair {
    int first;
    int second;
};

struct Pair swap(int a, int b) {
    a = a + b;
    b = a - b;
    a = a - b;

    struct Pair result;
    result.first = a;
    result.second = b;
    return result;
}

int main() {
    int a = 5, b = 10;
    printf("Original values:\na = %d, b = %d\n", a, b);

    // Call swap function
    struct Pair swapped = swap(a, b);

    printf("\nAfter swap (no temp, no pointers):\na = %d, b = %d\n", swapped.first, swapped.second);

    return 0;
}
/**********************************************************************************************************************/
16.Implement a program to check if a number is even or odd using the modulus operator.
#include <stdio.h>

// Function to check if a number is even
int modulus(int number)
{
    if (number % 2 == 0)
    {
        return 1; // Return 1 if even
    }
    else
    {
        return 0; // Return 0 if odd
    }
}

int main()
{
    int number;
    printf("Enter the number: ");
    scanf("%d", &number);

    if (modulus(number))
    {
        printf("%d is an even number\n", number);
    }
    else
    {
        printf("%d is an odd number\n", number);
    }

    return 0;
}
o/p:
enter the number :6
6 is even number
/***************************************************************************************/
17.Write a C program that uses the bitwise operators to check if a given positive integer is
divisible by both 6 and 9?
#include <stdio.h>
int isDivisibleBy6And9(int num) {
    // Check divisibility by 2 using bitwise AND
    if ((num & 1) != 0) {
        return 0; // Not divisible by 2
    }
    // Check divisibility by 9 using modulus
    if (num % 9 != 0) {
        return 0; // Not divisible by 9
    }
    return 1; // Divisible by both 6 and 9 (i.e., divisible by 18)
}

int main() {
    int num;
    printf("Enter a positive integer: ");
    scanf("%d", &num);
    if (isDivisibleBy6And9(num)) {
        printf("%d is divisible by both 6 and 9.\n", num);
    } else {
     
        printf("%d is NOT divisible by both 6 and 9.\n", num);
    }

    return 0;
}
output:
Enter a positive integer: 36
36 is divisible by both 6 and 9.

Enter a positive integer: 54
54 is divisible by both 6 and 9.

Enter a positive integer: 20
20 is NOT divisible by both 6 and 9.
/****************************************************************************/
18.Develop a program to find the maximum of three numbers using the conditional operator
#include<stdio.h>
int maxthreenumber(int a,int b,int c)
{
        return (a>b?((a>c)?a:c):((b>c)?b:c));
                        }
                        int main()
                        {
                        int num1,num2,num3,max;
                        printf("enter three number:");
                        scanf("%d%d%d",&num1,&num2,&num3);
                                max=maxthreenumber(num1,num2,num3);
                        printf("the maximum is:%d\n",max);
                        return 0;
                        }
/******************************************************************************************/
19.Implement a program that checks if a number is less than 50 without using the less than
operator.
#include<stdio.h>
int islessthan50(int num)
{
        return !(num>=50);
        }
int main()
{
        int num;
        printf("enter the number:");
        scanf("%d",&num);
        if(islessthan50(num))
        {
                printf("number is lessthan 50");
        }
        else
        {
                printf("number is not lessthan 50");
        }
        return 0;
/********************************************************************************************/
20.What would be the value of 'a':
a. int a = 10/45*23%45/(45%4*21)
int a = 10 / 45 * 23 % 45 / (45 % 4 * 21);
  Start with 10 / 45:
          Integer division: 10 / 45 = 0
    Next: 0 * 23 =0
    Next: 0 % 45 = 0
    Now the expression becomes:
0 / (45 % 4 * 21)
Evaluate the denominator:
    45 % 4 = 1
    1 * 21 = 21
So, final expression:
    a = 0 / 21
    Integer division: 0 / 21 = 0
✅ Final Answer:
a = 0;
int a = 10 / 45 * 23 % 45 / (45 % 4 * 21);
We're working with integer arithmetic in C, so:
    / is integer division (e.g., 5 / 2 = 2)
    * is multiplication
    % is modulo (remainder after division)
    All these operators have the same precedence and are evaluated left to right
✅ Step 1: Evaluate left to right
Part 1: 10 / 45
    10 divided by 45 = 0 (because it's integer division)
Now the expression becomes:
int a = 0 * 23 % 45 / (45 % 4 * 21);
✅ Step 2: Continue left to right
Part 2: 0 * 23
    0 × 23 = 0
Now:
int a = 0 % 45 / (45 % 4 * 21);
✅ Step 3: Continue
Part 3: 0 % 45
    0 % 45 = 0
Now:
int a = 0 / (45 % 4 * 21);
✅ Step 4: Evaluate the denominator
First: 45 % 4
    45 divided by 4 = 11 remainder 1
    So, 45 % 4 = 1
Then multiply: 1 * 21 = 21
Now the expression is:
int a = 0 / 21;
✅ Step 5: Final division
0 / 21 = 0
🎉 Final Result:
a = 0;
The value of a is 0
/*****************************************************************************************/
b.float a = 10+45.0*23-45+(4*21.0)?
float a=10+45.0*23-45+(84.0)
float a=10+1035.0-45+84.0
float a=1045.0-45+84.0
float a=1000.0+84.0
float a=1084.0
/***************************************************************************************/
21.mplement a C program to check if the given number is a palindrome in binary
representation using bitwise operators
#include <stdio.h>

int isBinaryPalindrome(unsigned int n) {
    int left = 31;  // Most significant bit position (for 32-bit integers)
    int right = 0;  // Least significant bit position

    while (left > right) {
        int leftBit = (n >> left) & 1;   // Extract left bit
        int rightBit = (n >> right) & 1; // Extract right bit

        // Skip leading zeros on the left
        if (leftBit == 0) {
            left--;
            continue;
        }

        // If bits at both ends don't match, not a palindrome
        if (leftBit != rightBit) {
            return 0;
        }

        left--;
        right++;
    }

    return 1;  // It's a binary palindrome
}

int main() {
    unsigned int num;
    printf("Enter a number: ");
    scanf("%u", &num);

    if (isBinaryPalindrome(num)) {
        printf("%u is a binary palindrome.\n", num);
    } else {
        printf("%u is NOT a binary palindrome.\n", num);
    }

    return 0;
}
/********************************************************************************/
```
