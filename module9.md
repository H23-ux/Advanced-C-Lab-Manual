**EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.**

**Aim:**
To write a C program to display stack elements using an array.
**Algorithm:**
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
**Program:**
```
#include<stdio.h>
float stack[100];
int top,i;
void display()
{
    for(i=top;i>=0;i--){
        printf("%.1f\n",stack[i]);
    }
}
```



**Output:**


<img width="515" height="487" alt="image" src="https://github.com/user-attachments/assets/5fd2a204-4a6d-4e2e-9d94-6ceb55cd2e4d" />



**Result:**

Thus, the program to display stack elements using an array is verified successfully.
 

**EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.**

**Aim:**
To create a C program to push the given element in to a stack using array.
**Algorithm:**
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
**Program:**

```
#include<stdio.h>
int size=3,top=-1,stack[100];
void push (int data)
{
    if(top==size-1) printf("stack is full\n");
    else{
        top++;
        stack[top]=data;
    }
}
```

**Output:**



<img width="454" height="485" alt="image" src="https://github.com/user-attachments/assets/1272ad01-41fc-4a8d-b378-bb6d24f9f8f5" />



**Result:**

Thus, the program to push the given element in to a stack using array is verified successfully


 
**EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.**

**Aim:**
To write a C program to display queue elements using array

**Algorithm:**
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
**Program:**
```
#include<stdio.h>
int queue[50], rear=-1, front=-1,i;
void display()
{
    if((front==-1)||(rear==-1)||(front>rear)) printf("No elements to display\n");
    else{
        for(i=front;i<=rear;i++){
            printf("%d ",queue[i]);
        }
    }
}


```

**Output:**

<img width="640" height="461" alt="image" src="https://github.com/user-attachments/assets/c0a05bdf-26b7-4dd5-bc15-dc8f546c6627" />



**Result:**

Thus, the program to display queue elements using array is verified successfully.


 
**EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.**

**Aim:**
To write a C program to insert elements in queue using array.

**Algorithm:**
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

**Program:**

```
#include<stdio.h>
float queue[];
int front, rear;
void enqueue(float data)
{
    if (front==-1)
        front++;
    rear++;
    queue[rear]=data;
}
```

**Output:**

<img width="652" height="400" alt="image" src="https://github.com/user-attachments/assets/3f087036-93b2-40dc-abf2-00acb6e81f45" />


**Result:**

Thus, the program to insert elements in queue using array is verified successfully.



 
**EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY**



**Aim:**

To create a function in C that deletes an element from a queue implemented using an array.

**Algorithm:**

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



**Program:**

```
#include<stdio.h>
float queue[];
int front, rear;
void dequeue()
{
    if((front==-1)||(rear==-1)||(front>rear))
    {
        printf("Queue Underflow.\n");
    }
    else
    {
        front++;
    }
}
```

**Output:**

<img width="683" height="633" alt="image" src="https://github.com/user-attachments/assets/aee22a90-b3bd-4a66-8594-112c99acf723" />


**Result:**

Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
