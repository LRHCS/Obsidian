![[Pasted image 20220724100121.png]]
```CPP
void insert(Node *last, int data)
{
    Node *temp = (Node *)malloc(sizeof(Node));

    temp->data = data;

    temp->next = last->next;
    last->next = temp;
}
```