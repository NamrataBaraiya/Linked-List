# Linked list
Linked list implimentation in c

#include<stdlib.h>
#include<stdio.h>
#include<conio.h>

struct node
{
    int node;
    struct node *next;
};
int main()
{
    int i,n,item;
    struct node *p,*q,*head;
    
    printf("Enter the no of node n:");
    scanf("%d",&n);

    printf("Enter the value of the head node:");
    scanf("%d",&item);

    q= (struct node *)malloc(sizeof(struct node));
    q->node = item;
    q->next = NULL;

    head = q;
    p = head ;

    for( i = 1; i<n ;i++)
    {

    printf("Enter the value of the next node:");
    scanf("%d",&item);

    q = (struct node *)malloc(sizeof(struct node));
    q->node = item;
    q->next = NULL;

    p->next = q;
    p = p->next;

    }
    printf("\n");
    p = head;

    while(p!= NULL)
    {
        printf("%d",p->node);
        p = p->next;
    }
    return 0;
}
