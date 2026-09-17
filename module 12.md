

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
#include <stdio.h>

struct Node
{
    int data;
    struct Node *next;
}*head;

void display()
{
    struct Node *temp;

    

    if(head == NULL)
    {
        return;
    }
    temp=head;

    while(temp != NULL)
    {
        printf("%d\n", temp->data);
        temp = temp->next;
    }
}
```
Output:

<img width="510" height="497" alt="image" src="https://github.com/user-attachments/assets/ce0dd606-26c0-42e1-8155-d581858b20c1" />



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void pop()  
{ 
    if(head==NULL)
    {
    printf("stack is empty\n");
    return;
    }
    struct Node *temp;
    
        temp=head;
        head=temp->next;
        free(temp);
    
}
```

Output:

<img width="1012" height="652" alt="image" src="https://github.com/user-attachments/assets/b647b228-1ce9-453f-bedc-ba4eedd4985e" />




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *temp=front;
    if(front==NULL)
    printf("queue is empty");
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}
```
Output:

<img width="637" height="557" alt="image" src="https://github.com/user-attachments/assets/0ae0f9d3-def7-4c6f-ae3f-9eec23ce2fe1" />

Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node *n=(struct Node *)malloc(sizeof(struct Node));
    n->data=data;
    n->next=NULL;
    if(front==NULL)
    front=rear=n;
 else
 {
     rear->next=n;
     rear=n;
 }
}
```

Output:

<img width="762" height="578" alt="image" src="https://github.com/user-attachments/assets/3643d21a-9fbe-4ad8-bc71-9a7bcf68715d" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    if(front==NULL){
    return;
    }
    else
    {
        printf("%.2f",front->data);
    }
}
```

Output:

<img width="542" height="567" alt="image" src="https://github.com/user-attachments/assets/0a3608af-fce9-4b95-9a46-4451195392bf" />




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


