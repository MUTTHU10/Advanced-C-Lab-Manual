EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

~~~
struct Node{
    float data; 
    struct Node *next;
};
struct Node *head=NULL;

void search(float data)
{
    struct Node *temp=head;
    int location=1;
    while(temp!=0){
        if (temp->data==data){
            printf("item %.2f found at location %d",data,location);
            return;
        }
        temp=temp->next;
        location++;
    }
    printf("Item not found");
}
~~~

Output:

<img width="972" height="502" alt="image" src="https://github.com/user-attachments/assets/12bbebc4-40d6-4fb1-b665-f01e54835057" />



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
~~~
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    float data;
    struct Node *next;
};

struct Node *head = NULL;

void insert(float value)
{
    struct Node *newnode;
    struct Node *temp;

    newnode = (struct Node *)malloc(sizeof(struct Node));

    newnode->data = value;
    newnode->next = NULL;

    if (head == NULL)
    {
        head = newnode;
    }
    else
    {
        temp = head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newnode;
    }
}
~~~

Output:

<img width="837" height="567" alt="image" src="https://github.com/user-attachments/assets/8b65586e-3a5d-4eec-9d5e-19b8f22f7d18" />


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

~~~
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *prev;
    struct Node *next;
};

struct Node *head = NULL;

void display()
{
    struct Node *temp = head;

    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
~~~

Output:

<img width="897" height="547" alt="image" src="https://github.com/user-attachments/assets/752430b3-f0ef-4b7b-9f90-c352c939173b" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
~~~
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    double data;
    struct Node *prev;
    struct Node *next;
};

struct Node *head = NULL;

void insert(double data)
{
    struct Node *ptr;
    struct Node *temp;

    ptr = (struct Node *)malloc(sizeof(struct Node));

    ptr->data = data;
    ptr->prev = NULL;
    ptr->next = NULL;

    if (head == NULL)
    {
        head = ptr;
    }
    else
    {
        temp = head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = ptr;
        ptr->prev = temp;
    }
}


~~~

Output:

<img width="892" height="532" alt="image" src="https://github.com/user-attachments/assets/1254bc9e-65d2-4438-a8c8-51887d07bc36" />



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

~~~
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    char data;
    struct Node *prev;
    struct Node *next;
};

struct Node *head = NULL;

void delete()
{
    struct Node *temp;

    if (head == NULL)
    {
        printf("UNDERFLOW\n");
        return;
    }

    temp = head;
    head = head->next;

    if (head != NULL)
    {
        head->prev = NULL;
    }

    free(temp);

    printf("Node deleted\n");
}
~~~
Output:

<img width="1100" height="687" alt="image" src="https://github.com/user-attachments/assets/e9dc0a5d-f555-4ad4-9a0e-8fa25061bb5e" />






Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





