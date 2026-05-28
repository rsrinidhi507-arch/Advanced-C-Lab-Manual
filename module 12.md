
EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

Date:25.05.2026

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
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *head = NULL;

void push(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = head;
    head = newnode;
}

void display()
{
    struct Node *p;
    p = head;

    printf("Stack elements are:\n");

    while(p != NULL){
        printf("%d\n", p->data);
        p = p->next;
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    display();

    return 0;
}
```

Output:

<img width="1685" height="1017" alt="image" src="https://github.com/user-attachments/assets/1f429659-f3bd-4630-8009-6dc40c1ecf98" />


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

Date:25.05.2026

Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *head = NULL;

void push(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = head;
    head = newnode;
}
void pop()
{
    struct Node *temp;
    if(head == NULL){
        printf("Stack is empty\n");
    }else{
        temp = head;
        printf("Deleted element = %d\n", head->data);
        head = head->next;
        free(temp);
    }
}
void display()
{
    struct Node *p = head;
    printf("Stack elements are:\n");

    while(p != NULL){
        printf("%d\n", p->data);
        p = p->next;
    }
}
int main()
{
    push(10);
    push(20);
    push(30);

    pop();
    display();

    return 0;
}
```

Output:

<img width="1637" height="1022" alt="image" src="https://github.com/user-attachments/assets/2f117c7c-8dcd-4b7b-94c4-262589ab7fa8" />



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Date:25.05.2026

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
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *front = NULL;
struct Node *rear = NULL;

void enqueue(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = NULL;

    if(rear == NULL){
        front = rear = newnode;
    }else{
        rear->next = newnode;
        rear = newnode;
    }
}
void display()
{
    struct Node *temp;
    if(front == NULL){
        printf("Queue is empty\n");
    }else{
        temp = front;
        printf("Queue elements are:\n");
        while(temp != NULL){
            printf("%d\n", temp->data);
            temp = temp->next;
        }
    }
}
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    return 0;
}
```

Output:

<img width="1641" height="1001" alt="image" src="https://github.com/user-attachments/assets/4a105cd4-22c1-4118-9b18-f6aa2008437d" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Date:25.05.2026

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
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *front = NULL;
struct Node *rear = NULL;

void enqueue(int value)
{
    struct Node *p;
    p = (struct Node *)malloc(sizeof(struct Node));
    p->data = value;
    p->next = NULL;
    
    if(front == NULL && rear == NULL){
        front = rear = p;
    }else{
        rear->next = p;
        rear = p;
    }
}
void display()
{
    struct Node *temp;
    temp = front;
    printf("Queue elements are:\n");

    while(temp != NULL){
        printf("%d\n", temp->data);
        temp = temp->next;
    }
}
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    return 0;
}
```

Output:
<img width="1667" height="952" alt="image" src="https://github.com/user-attachments/assets/f8ed3457-668d-4431-ba09-bf17174fdec6" />

Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

Date:25.05.2026

Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *front = NULL;
struct Node *rear = NULL;

void enqueue(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = NULL;

    if(front == NULL && rear == NULL){
        front = rear = newnode;
    }else{
        rear->next = newnode;
        rear = newnode;
    }
}
void peek()
{
    if(front == NULL){
        printf("Queue is empty\n");
    }else{
        printf("Front element = %d\n", front->data);
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    peek();

    return 0;
}
```

Output:

<img width="1657" height="921" alt="image" src="https://github.com/user-attachments/assets/21e61b08-0ade-4f05-9da4-7487394f1cd0" />




Result:
Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


