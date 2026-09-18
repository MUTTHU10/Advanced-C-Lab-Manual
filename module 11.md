

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
~~~
#include <stdio.h>
int max_of_four(int a, int b, int c, int d)
{
    int max = a;

    if (b > max)
        max = b;
    if (c > max)
        max = c;
    if (d > max)
        max = d;

    return max;
}
int main(){
    int a,b,c,d;
    scanf("%d %d %d %d",&a,&b,&c,&d);
    printf("%d",max_of_four(a,b,c,d));
}
~~~

Output:

<img width="685" height="447" alt="image" src="https://github.com/user-attachments/assets/4bcef61e-da1b-438d-b966-7321a7ef8a11" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:

~~~
#include <stdio.h>

void calculate_the_maximum(int n, int k)
{
    int max_and = 0, max_or = 0, max_xor = 0;

    for (int i = 1; i <= n; i++)
    {
        for (int j = i + 1; j <= n; j++)
        {
            int a = i & j;
            int b = i | j;
            int c = i ^ j;

            if (a < k && a > max_and)
                max_and = a;

            if (b < k && b > max_or)
                max_or = b;

            if (c < k && c > max_xor)
                max_xor = c;
        }
    }

    printf("%d\n", max_and);
    printf("%d\n", max_or);
    printf("%d\n", max_xor);
}

int main()
{
    int n, k;

    scanf("%d %d", &n, &k);

    calculate_the_maximum(n, k);

    return 0;
}
~~~

Output:

<img width="627" height="427" alt="image" src="https://github.com/user-attachments/assets/8f29d6b5-8fc8-44c3-870c-20920febf5b0" />


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:

~~~
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int total_number_of_shelves;
    scanf("%d", &total_number_of_shelves);

    int total_number_of_queries;
    scanf("%d", &total_number_of_queries);

    // Array to store number of books in each shelf
    int *total_number_of_books = (int *)calloc(total_number_of_shelves, sizeof(int));

    // Array of pointers for shelves
    int **total_number_of_pages = (int **)malloc(total_number_of_shelves * sizeof(int *));

    for (int i = 0; i < total_number_of_shelves; i++)
    {
        total_number_of_pages[i] = NULL;
    }

    while (total_number_of_queries--)
    {
        int type;
        scanf("%d", &type);

        if (type == 1)
        {
            int x, y;
            scanf("%d %d", &x, &y);

            total_number_of_books[x]++;

            total_number_of_pages[x] = (int *)realloc(
                total_number_of_pages[x],
                total_number_of_books[x] * sizeof(int));

            total_number_of_pages[x][total_number_of_books[x] - 1] = y;
        }
        else if (type == 2)
        {
            int x, y;
            scanf("%d %d", &x, &y);

            printf("%d\n", total_number_of_pages[x][y]);
        }
        else if (type == 3)
        {
            int x;
            scanf("%d", &x);

            printf("%d\n", total_number_of_books[x]);
        }
    }

    for (int i = 0; i < total_number_of_shelves; i++)
    {
        free(total_number_of_pages[i]);
    }

    free(total_number_of_pages);
    free(total_number_of_books);

    return 0;
}
~~~

Output:

<img width="1066" height="407" alt="image" src="https://github.com/user-attachments/assets/f91dd08b-a5d5-45b4-8e03-1408146247cd" />



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:

~~~
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n;
    scanf("%d", &n);

    int *arr = (int *)malloc(n * sizeof(int));

    int sum = 0;

    for (int i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
        sum += arr[i];
    }

    printf("%d", sum);

    free(arr);

    return 0;
}
~~~

Output:

<img width="1192" height="402" alt="image" src="https://github.com/user-attachments/assets/35cd527f-b3e8-450f-a00f-a034c1a3ae60" />


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
~~~
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
    char *s;

    s = (char *)malloc(1024 * sizeof(char));

    scanf("%[^\n]", s);

    s = (char *)realloc(s, strlen(s) + 1);

    int len = strlen(s);

    for (int i = 0; i < len; i++)
    {
        if (s[i] == ' ')
        {
            printf("\n");
        }
        else
        {
            printf("%c", s[i]);
        }
    }

    free(s);

    return 0;
}
~~~

Output:

<img width="640" height="357" alt="image" src="https://github.com/user-attachments/assets/4714939b-071a-4fad-94aa-0338eb19d71f" />





Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
