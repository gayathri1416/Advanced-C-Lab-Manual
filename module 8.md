EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
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
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    switch (n)
    {
        case 71:printf("seventy one");break;
        case 72:printf("seventy two");break; 

        case 73:printf("seventy three");break; 

        case 74:printf("seventy four");break; 
        case 75:printf("seventy five");break; 
        case 76:printf("seventy six");break; 

        case 77:printf("seventy seven");break; 

        case 78:printf("seventy eight");break;
        case 79:printf("seventy nine");break; 
default:printf("Greater than 79");

    }
}




Output:

<img width="651" height="305" alt="image" src="https://github.com/user-attachments/assets/fbe791a1-8175-4bab-b240-271a47de0577" />







Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
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
#include<stdio.h>
int main()
{
    char str[100];
    int freq[10]={0};
    scanf("%s",str);
    for(int i=0;str[i]!='\0';i++)
    {
        switch(str[i])
        {
            case '0':freq[0]++;break;
            case '1':freq[1]++;break; 
            case '2':freq[2]++;break; 
            case '3':freq[3]++;break; 
            case '4':freq[4]++;break; 
            case '5':freq[5]++;break; 
            case '6':freq[6]++;break; 
            case '7':freq[7]++;break; 
            case '8':freq[8]++;break;
            case '9':freq[9]++;break; 
    
        }
    }
    for(int i=0;i<10;i++)
    {
        printf("%d ",freq[i]);
    }
}

```

Output:

<img width="923" height="282" alt="image" src="https://github.com/user-attachments/assets/7b658639-a4e1-44ed-978a-2875659f166b" />





Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
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

#include<stdio.h>
#include<string.h>
int main()
{
    int n;
    scanf("%d",&n);
    char str[10][10];
    int i,j,k;
    for(i=0;i<n;i++)
    {
        scanf("%s",str[i]);
    }
    if(n==2)
    {
        printf("%s %s \n%s %s",str[0],str[1],str[1],str[0]);
        
    }
    
    else
    {
        for(i=0;i<n;i++)
        {
            for(j=0;j<n;j++)
            {
                for(k=0;k<n;k++)
                {
                    
                    if(i!=j&&j!=k&&k!=i)
                    {
                        if((i>j&&strcmp(str[i],str[j])==0)||
                        (i>k&&strcmp(str[i],str[k])==0)
                        ||
                        (j>k&&strcmp(str[j],str[k])==0))
                        continue;
                        printf("%s %s %s\n",str[i],str[j],str[k]);
                    }
                }
            }
        }
    }
}

```
Output:

<img width="598" height="425" alt="image" src="https://github.com/user-attachments/assets/ce397a2f-376c-4e3f-a512-17a468019228" />


Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
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

#include<stdio.h>
int main()
{
    int n,i,j,s,m;
    scanf("%d",&n);
    s=2*n-1;
    for(i=0;i<s;i++)
    {
        for(j=0;j<s;j++)
        {
            m=i;
            if(j<m)
            {
                m=j;
            }
            if(s-1-i<m)
            {
                m=s-1-i;
            }
            if(s-1-j<m)
            {
                m=s-1-j;
                }printf("%d ",n-m);  
        }printf("\n"); 
        
    } 
    
}
```

Output:
![Uploading image.png…]()





Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

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
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}

int main() {
    int result;
    result = square(); 
    printf("Square of the number is: %d\n", result);
    return 0;
}
```

Output:

<img width="512" height="160" alt="image" src="https://github.com/user-attachments/assets/5146fee1-6a17-40b3-b43d-c40cc6843a09" />




Result:
Thus, the program is verified successfully

