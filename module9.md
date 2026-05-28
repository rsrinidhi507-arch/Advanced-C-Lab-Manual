EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Date:25.04.2026

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
```
#include <stdio.h>
#define MAX 5

int stack[MAX];
int top = -1;

void push(int value)
{
    if(top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }else{
        top++;
        stack[top] = value;
    }
}

void display()
{
    int i;

    if(top == -1)
    {
        printf("Stack is Empty\n");
    }
    else
    {
        printf("Stack Elements are:\n");

        for(i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }
}

int main()
{
    int n, i, value;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter stack elements:\n");

    for(i = 0; i < n; i++)
    {
        scanf("%d", &value);
        push(value);
    }

    display();

    return 0;
}

```

Output:

<img width="1682" height="1030" alt="image" src="https://github.com/user-attachments/assets/16afc6f2-161f-42af-b2a8-3784811c9eb8" />




Result:
Thus, the program to display stack elements using an array is verified successfully.
 


EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

Date:25.04.2026

Aim:
To create a C program to push the given element in to a stack using array.

Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
#include <stdio.h>

#define MAX 5

int stack[MAX];
int top = -1;

void push(int value)
{
    if(top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }
    else
    {
        top++;
        stack[top] = value;
        printf("%d pushed into stack\n", value);
    }
}

void display()
{
    int i;

    if(top == -1)
    {
        printf("Stack is Empty\n");
    }
    else
    {
        printf("Stack elements are:\n");

        for(i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }
}

int main()
{
    int value;

    printf("Enter the element to push: ");
    scanf("%d", &value);

    push(value);

    display();

    return 0;
}
```
Output:

<img width="1637" height="1002" alt="image" src="https://github.com/user-attachments/assets/b2d7a23b-7d14-44e7-b7c5-0c846b56a415" />





Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

Date:25.04.2026

Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void insert(int value)
{
    if(rear == MAX - 1){
        printf("Queue Overflow\n");
    }else{
        if(front == -1){
            front = 0;
        }

        rear++;
        queue[rear] = value;
    }
}

void display()
{
    int i;

    if(front == -1 || front > rear){
        printf("Queue is Empty\n");
    }else{
        printf("Queue elements are:\n");

        for(i = front; i <= rear; i++){
            printf("%d\n", queue[i]);
        }
    }
}

int main()
{
    int n, i, value;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter queue elements:\n");

    for(i = 0; i < n; i++){
        scanf("%d", &value);
        insert(value);
    }

    display();

    return 0;
}
```

Output:

<img width="1625" height="1012" alt="image" src="https://github.com/user-attachments/assets/6afb9ace-a5be-4f73-91b6-16706d86b1e6" />



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.

Date:25.04.2026

Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void enqueue(int value)
{
    if(rear == MAX - 1){
        printf("Queue Overflow\n");
    }else{
        if(front == -1){
            front = 0;
        }

        rear++;
        queue[rear] = value;

        printf("%d inserted into queue\n", value);
    }
}

void display()
{
    int i;

    if(front == -1){
        printf("Queue is Empty\n");
    }else{
        printf("Queue elements are:\n");

        for(i = front; i <= rear; i++){
            printf("%d\n", queue[i]);
        }
    }
}

int main()
{
    int value;

    printf("Enter the element to insert: ");
    scanf("%d", &value);

    enqueue(value);

    display();

    return 0;
}
```

Output:

<img width="1652" height="966" alt="image" src="https://github.com/user-attachments/assets/0fc61348-a9df-4425-b7d2-937da6b2fa97" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

Date:25.04.2026

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
```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void enqueue(int value)
{
    if(rear == MAX - 1){
        printf("Queue Overflow\n");
    }else{
        if(front == -1){
            front = 0;
        }

        rear++;
        queue[rear] = value;
    }
}
void dequeue()
{
    if(front == -1){
        printf("Queue Underflow\n");
    }else{
        printf("Deleted element is %d\n", queue[front]);
        front++;

        if(front > rear){
            front = rear = -1;
        }
    }
}
void display()
{
    int i;

    if(front == -1){
        printf("Queue is Empty\n");
    }else{
        printf("Remaining queue elements are:\n");

        for(i = front; i <= rear; i++){
            printf("%d\n", queue[i]);
        }
    }
}
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    dequeue();

    display();

    return 0;
}
```

Output:

<img width="1647" height="940" alt="image" src="https://github.com/user-attachments/assets/9c625e2a-c364-4827-9fcc-ef51280fc317" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
