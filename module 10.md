EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.

Date:30.04.2026

Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
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

void insert(int value)
{
    struct Node *newNode, *temp;
    newNode = (struct Node *)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if(head == NULL){
        head = newNode;
    }else{
        temp = head;
        while(temp->next != NULL){
            temp = temp->next;
        }
        temp->next = newNode;
    }
}
void search(int key)
{
    struct Node *temp;
    int position = 1, found = 0;
    temp = head;

    while(temp != NULL){
        if(temp->data == key){
            printf("Element found at position %d\n", position);
            found = 1;
            break;
        }
        temp = temp->next;
        position++;
    }
    if(found == 0){
        printf("Element not found\n");
    }
}
int main(){
    int key;

    insert(10);
    insert(20);
    insert(30);
    insert(40);
    printf("Enter element to search: ");
    scanf("%d", &key);

    search(key);

    return 0;
}
```
Output:

<img width="1687" height="957" alt="image" src="https://github.com/user-attachments/assets/9135f97c-4baf-4ce1-a809-bfa6b2d9ae9a" />



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.

Date:30.04.2026

Aim:
To write a C program to insert a node in a linked list.

Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
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

void insert(int value)
{
    struct Node *newNode, *temp;

    newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = value;
    newNode->next = NULL;

    if(head == NULL){
        head = newNode;
    }else{
        temp = head;

        while(temp->next != NULL){
            temp = temp->next;
        }
        temp->next = newNode;
    }
}
void display()
{
    struct Node *temp;

    temp = head;

    printf("Linked list elements are:\n");

    while(temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
int main()
{
    insert(10);
    insert(20);
    insert(30);

    display();

    return 0;
}
```
Output:

<img width="1705" height="1033" alt="Screenshot 2026-05-28 170650" src="https://github.com/user-attachments/assets/0b53f2e1-ddaa-4a69-9a2e-0a5cf237ae05" />

Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST

Date:30.04.2026

Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *prev;
    struct Node *next;
};

struct Node *head = NULL;

void insert(int value)
{
    struct Node *newNode, *temp;

    newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = value;
    newNode->prev = NULL;
    newNode->next = NULL;

    if(head == NULL){
        head = newNode;
    }else{
        temp = head;
        while(temp->next != NULL){
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->prev = temp;
    }
}
void traverse()
{
    struct Node *temp;
    temp = head;
    printf("Doubly linked list elements are:\n");

    while(temp != NULL){
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
int main()
{
    insert(10);
    insert(20);
    insert(30);

    traverse();

    return 0;
}
```

Output:

<img width="1692" height="1020" alt="image" src="https://github.com/user-attachments/assets/d446bcb8-47a0-4e1f-8850-fa08dbf67554" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST

Date:30.04.2026

Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *prev;
    struct Node *next;
};

struct Node *head = NULL;

void insert(int value)
{
    struct Node *newNode, *temp;

    newNode = (struct Node *)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->prev = NULL;
    newNode->next = NULL;

    if(head == NULL){
        head = newNode;
    }else{
        temp = head;
        while(temp->next != NULL){
            temp = temp->next;
        }
        temp->next = newNode;
        newNode->prev = temp;
    }
}
void display()
{
    struct Node *temp;
    temp = head;
    printf("Doubly linked list elements are:\n");

    while(temp != NULL){
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
int main()
{
    insert(10);
    insert(20);
    insert(30);

    display();

    return 0;
}
```

Output:

<img width="1683" height="1039" alt="image" src="https://github.com/user-attachments/assets/20859316-a04f-48e5-b10e-14f4953768b4" />



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

Date:30.04.2026

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
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *head = NULL;

void insert(int value)
{
    struct Node *newNode, *temp;

    newNode = (struct Node *)malloc(sizeof(struct Node));

    newNode->data = value;
    newNode->next = NULL;

    if(head == NULL){
        head = newNode;
    }else{
        temp = head;
        while(temp->next != NULL){
            temp = temp->next;
        }
        temp->next = newNode;
    }
}
void deleteElement(int key)
{
    struct Node *temp, *prev;
    temp = head;
    prev = NULL;

    if(head == NULL){
        printf("Linked list is empty\n");
        return;
    }
    while(temp != NULL && temp->data != key){
        prev = temp;
        temp = temp->next;
    }
    if(temp == NULL){
        printf("Element not found\n");
        return;
    }
    if(temp == head){
        head = head->next;
    }else{
        prev->next = temp->next;
    }
    free(temp);
    printf("Element deleted successfully\n");
}
void display()
{
    struct Node *temp;
    temp = head;
    printf("Remaining linked list elements are:\n");

    while(temp != NULL){
        printf("%d ", temp->data);
        temp = temp->next;
    }
}
int main()
{
    insert(10);
    insert(20);
    insert(30);
    insert(40);

    deleteElement(20);

    display();

    return 0;
}
```

Output:

<img width="1532" height="980" alt="image" src="https://github.com/user-attachments/assets/24ddc235-914f-4cc6-8460-9e7ba03776a3" />



Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





