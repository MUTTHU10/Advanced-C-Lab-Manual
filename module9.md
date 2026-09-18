<img width="1042" height="702" alt="image" src="https://github.com/user-attachments/assets/be1247ff-12f9-4d3b-bbed-6c9e62696700" /><img width="985" height="546" alt="image" src="https://github.com/user-attachments/assets/4bc0f328-f18f-4afb-86d6-3ea5d90be98f" /><img width="985" height="546" alt="image" src="https://github.com/user-attachments/assets/e8be69cc-1bce-44b6-ac66-aeff2213a25c" />EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

~~~
float stack[100];
int top = -1;

void display()
{
    if (top == -1)
    {
        printf("stack is empty\n");
    }
    else
    {
        for (int i = top; i >= 0; i--)
        {
            printf("%.1f\n", stack[i]);
        }
    }
}
~~~

Output:

<img width="1072" height="550" alt="image" src="https://github.com/user-attachments/assets/85eff5bd-4788-4d7d-9156-e89e6795905a" />


Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

~~~
#include <stdio.h>

extern int top;
extern char stack[];

void push(char data)
{
    if (top == 2)
    {
        printf("stack is full\n");
    }
    else
    {
        top++;
        stack[top] = data;
    }
}
~~~
Output:

<img width="916" height="642" alt="image" src="https://github.com/user-attachments/assets/34514c46-ebdd-4462-a084-770750e3d5a9" />




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

~~~
#include <stdio.h>

int front = -1;
int rear = -1;
float queue[50];

void display()
{
    int i;

    if (front == -1)
    {
        printf("No elements to display");
    }
    else
    {
        for (i = front; i <= rear; i++)
        {
            printf("%.1f\n", queue[i]);
        }
    }
}
~~~
Output:

<img width="985" height="546" alt="image" src="https://github.com/user-attachments/assets/848a4c31-db92-4485-b962-ebad71c3fd92" />



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
~~~
int size=10, rear=-1, front=-1;
char queue[50];
void enqueue(char data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
    }
}

~~~

Output:

<img width="1012" height="471" alt="image" src="https://github.com/user-attachments/assets/83cd81d3-1840-4153-9654-6ce5662e9020" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
~~~
extern int front;
extern int rear;

void dequeue()
{
    if (front == -1)
    {
        return;
    }

    front++;

    if (front > rear)
    {
        front = -1;
        rear = -1;
    }
}
~~~
Output:

<img width="1042" height="702" alt="image" src="https://github.com/user-attachments/assets/7abeaebb-51be-4337-a6a4-0dde0f3c526c" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
