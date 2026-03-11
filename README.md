 Queue ADT using
Single Linked List
People Waiting in Ticket
Queue
Concept: First person enters,
first person leaves (FIFO –
First In First Out).
PROGRAM
#include <stdio.h>
#include <stdlib.h>
Struct Node{
Int data;
Struct Node* next;
};
Struct Node
*front=NULL,*rear=NULL;
Void enqueue(int value){
Struct Node*
newNode=(struct
Node*)malloc(sizeof(struct
Node));
newNode->data=value;
newNode->next=NULL;
if(rear==NULL){
front=rear=newNode;
return;
}
Rear->next=newNode;
Rear=newNode;
}
Void display(){
Struct Node* temp=front;
While(temp!=NULL){
Printf(“%d -> “,temp-
>data);
Temp=temp->next;
}
Printf(“NULL”);
}
Int main(){
Enqueue(10);
Enqueue(20);
Enqueue(30);
Printf(“Ticket Queue:\n”);
Display();
Return 0;
}
OUTPUT
Ticket Queue:
10 -> 20 -> 30 -> NULL
