EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

~~~
#include <stdio.h>

int main()
{
    int n;
    scanf("%d", &n);

    switch(n)
    {
        case 71:
            printf("seventy one");
            break;

        case 72:
            printf("seventy two");
            break;

        case 73:
            printf("seventy three");
            break;

        case 74:
            printf("seventy four");
            break;

        case 75:
            printf("seventy five");
            break;

        case 76:
            printf("seventy six");
            break;

        case 77:
            printf("seventy seven");
            break;

        case 78:
            printf("seventy eight");
            break;

        case 79:
            printf("seventy nine");
            break;

        default:
            if (n > 79)
                printf("Greater than 79");
            break;
    }

    return 0;
}
~~~




Output:
<img width="570" height="357" alt="image" src="https://github.com/user-attachments/assets/1a5d9404-08ce-4b4c-9109-6bdc4212b2ad" />





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
~~~
#include <stdio.h>

int main()
{
    char str[1000];
    int freq[10] = {0};

    scanf("%s", str);

    for (int i = 0; str[i] != '\0'; i++)
    {
        if (str[i] >= '0' && str[i] <= '9')
        {
            freq[str[i] - '0']++;
        }
    }

    for (int i = 0; i < 10; i++)
    {
        printf("%d ", freq[i]);
    }

    return 0;
}
~~~




Output:
<img width="845" height="307" alt="image" src="https://github.com/user-attachments/assets/a63c8f96-f164-4b26-8822-a1d5971e7092" />







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

~~~
#include <stdio.h>
#include <string.h>

void swap(char *a, char *b)
{
    char temp[100];

    strcpy(temp, a);
    strcpy(a, b);
    strcpy(b, temp);
}

int next_permutation(int n, char **s)
{
    int i = n - 2;

    // Step 1: Find the first element from right
    // which is smaller than the next element
    while (i >= 0 && strcmp(s[i], s[i + 1]) >= 0)
        i--;

    // If no such element exists, this is the last permutation
    if (i < 0)
        return 0;

    // Step 2: Find the smallest element greater than s[i]
    int j = n - 1;

    while (strcmp(s[j], s[i]) <= 0)
        j--;

    // Step 3: Swap s[i] and s[j]
    swap(s[i], s[j]);

    // Step 4: Reverse the remaining elements
    int left = i + 1;
    int right = n - 1;

    while (left < right)
    {
        swap(s[left], s[right]);
        left++;
        right--;
    }

    return 1;
}

int main()
{
    int n;
    scanf("%d", &n);

    char *s[n];
    char words[n][100];

    for (int i = 0; i < n; i++)
    {
        s[i] = words[i];
        scanf("%s", s[i]);
    }

    do
    {
        for (int i = 0; i < n; i++)
        {
            printf("%s", s[i]);

            if (i != n - 1)
                printf(" ");
        }

        printf("\n");

    } while (next_permutation(n, s));

    return 0;
}
~~~


Output:


<img width="732" height="462" alt="image" src="https://github.com/user-attachments/assets/9f34dbf9-82b0-419b-95f8-4eab0e026b38" />




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

~~~
#include <stdio.h>

int main()
{
    int n;
    scanf("%d", &n);

    for (int i = 0; i < 2 * n - 1; i++)
    {
        for (int j = 0; j < 2 * n - 1; j++)
        {
            int min = i;

            if (j < min)
                min = j;

            if (2 * n - 2 - i < min)
                min = 2 * n - 2 - i;

            if (2 * n - 2 - j < min)
                min = 2 * n - 2 - j;

            printf("%d ", n - min);
        }

        printf("\n");
    }

    return 0;
}

~~~


Output:


<img width="907" height="682" alt="image" src="https://github.com/user-attachments/assets/0780613d-8be5-4c25-a6a5-78dcb922323e" />





Result:
Thus, the program is verified successfully




























