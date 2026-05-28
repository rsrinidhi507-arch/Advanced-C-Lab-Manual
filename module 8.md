EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

Date:12.03.2026

Aim:
To write a C program print the lowercase English word corresponding to the number

Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
```
#include <stdio.h>

int main()
{
    int n;

    printf("Enter a number from 1 to 9: ");
    scanf("%d", &n);

    switch(n)
    {
        case 1:
            printf("seventy one");
            break;

        case 2:
            printf("seventy two");
            break;

        case 3:
            printf("seventy three");
            break;

        case 4:
            printf("seventy four");
            break;

        case 5:
            printf("seventy five");
            break;

        case 6:
            printf("seventy six");
            break;

        case 7:
            printf("seventy seven");
            break;

        case 8:
            printf("seventy eight");
            break;

        case 9:
            printf("seventy nine");
            break;

        default:
            printf("Greater than 9");
    }

    return 0;
}
```



Output:


<img width="1662" height="1032" alt="image" src="https://github.com/user-attachments/assets/cde4dc2d-e150-4145-9c43-5eb6d7ccdca9" />







Result:
Thus, the C program to print the lowercase English word corresponding to the number was verified successfully.

 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

Date: 12.03.2026

Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include <stdio.h>

int main()
{
    char a[50];
    int i, h, c;

    printf("Enter the string of digits: ");
    scanf("%s", a);

    for(h = 0; h <= 3; h++)
    {
        c = 0;

        for(i = 0; a[i] != '\0'; i++)
        {
            if(a[i] == h + '0')
            {
                c++;
            }
        }

        printf("%d ", c);
    }

    return 0;
}
```




Output:


<img width="972" height="912" alt="image" src="https://github.com/user-attachments/assets/f96f0b48-434f-48ac-beb3-0e8c1669c03e" />







Result:
Thus, the program to print the frequency of digits from 0 to 3 was verified successfully.


EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.

Date: 12.03.2026

Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include <stdio.h>
#include <string.h>

void swap(char *a, char *b)
{
    char temp;
    temp = *a;
    *a = *b;
    *b = temp;
}
void permute(char s[], int l, int r)
{
    int i;

    if(l == r)
    {
        printf("%s\n", s);
    }
    else
    {
        for(i = l; i <= r; i++)
        {
            swap(&s[l], &s[i]);
            permute(s, l + 1, r);
            swap(&s[l], &s[i]);
        }
    }
}
int main()
{
    char s[20];
    int n;

    printf("Enter the string: ");
    scanf("%s", s);

    n = strlen(s);

    permute(s, 0, n - 1);

    return 0;
}
```



Output:

<img width="1727" height="1010" alt="image" src="https://github.com/user-attachments/assets/6e3544d0-742c-4632-a785-07e2adec7616" />





Result:
Thus, the program to print all permutations of a string was verified successfully.
 

EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW.

Date: 12.03.2026

Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.

Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include <stdio.h>

int main()
{
    int n, i, j, min;
    int len;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    len = n * 2 - 1;

    for(i = 0; i < len; i++)
    {
        for(j = 0; j < len; j++)
        {
            min = i;

            if(j < min)
                min = j;

            if(len - 1 - i < min)
                min = len - 1 - i;

            if(len - 1 - j < min)
                min = len - 1 - j;

            printf("%d ", n - min);
        }

        printf("\n");
    }

    return 0;
}
```




Output:


<img width="1692" height="852" alt="image" src="https://github.com/user-attachments/assets/c8bb867e-7eb4-471e-9bb9-c5abc75a2da8" />






Result:
Thus, the program to print the pattern of numbers from 1 to n was verified successfully.


EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Date: 12.03.2026

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:
```
#include <stdio.h>

int square()
{
    int n, sq;

    printf("Enter a number: ");
    scanf("%d", &n);

    sq = n * n;

    return sq;
}

int main()
{
    int result;

    result = square();

    printf("Square of the number = %d", result);

    return 0;
}
```



Output:

<img width="967" height="931" alt="image" src="https://github.com/user-attachments/assets/fbcaf983-1270-4a4d-80cc-e680f82b78a9" />






Result:
Thus, the program to find the square of a number using a function without arguments and with return type was verified successfully.



























