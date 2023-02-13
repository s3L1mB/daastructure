# Activities

## Task 1:

- Refer to the following link. Discuss how Queues based on linked lists works:
  https://www.cs.usfca.edu/~galles/visualization/QueueLL.html

  A queue is a useful data structure in programming. It is similar to the ticket queue outside a cinema hall, where the first person entering the queue is the first person who gets the ticket.

Queue follows the First In First Out (FIFO) rule - the item that goes in first is the item that comes out first.

In programming terms, putting items in the queue is called enqueue, and removing items from the queue is called dequeue.

Basic Operations of Queue

A queue is an object (an abstract data structure - ADT) that allows the following operations:

    Enqueue: Add an element to the end of the queue
    Dequeue: Remove an element from the front of the queue
    IsEmpty: Check if the queue is empty
    IsFull: Check if the queue is full
    Peek: Get the value of the front of the queue without removing it


Working of Queue

Queue operations work as follows:

    two pointers FRONT and REAR
    FRONT track the first element of the queue
    REAR track the last element of the queue
    initially, set value of FRONT and REAR to -1

Enqueue Operation

    check if the queue is full
    for the first element, set the value of FRONT to 0
    increase the REAR index by 1
    add the new element in the position pointed to by REAR

Dequeue Operation

    check if the queue is empty
    return the value pointed by FRONT
    increase the FRONT index by 1
    for the last element, reset the values of FRONT and REAR to -1



## Task 2:

- The following snippet is from `./src/queue.cpp` lines 8-10. What happens if `front`, `rear` and `temp` were not global variables?

```cpp
struct node *front = NULL;
struct node *rear = NULL;
struct node *temp;
```

## Task 3:

- The following snippet is from `./src/queue.cpp` lines 11-28. Discuss in groups how the code works:

```cpp
void Insert(int val)
{
    if (rear == NULL)
    {
        rear = new node;
        rear->next = NULL;
        rear->data = val;
        front = rear;
    }
    else
    {
        temp = new node;
        rear->next = temp;
        temp->data = val;
        temp->next = NULL;
        rear = temp;
    }
}
```

## Task 4: Individual, at home

- Discuss the various operations that can be performed on a linked list. Refer to the following link:
  https://www.softwaretestinghelp.com/linked-list/


A linked list is a linear data structure that includes a series of connected nodes. Here, each node stores the data and the address of the next node. For example,


You have to start somewhere, so we give the address of the first node a special name called HEAD. Also, the last node in the linked list can be identified because its next portion points to NULL.

Linked lists can be of multiple types: singly, doubly, and circular linked list. In this article, we will focus on the singly linked list. 

## Links

- https://cpp.sh/
