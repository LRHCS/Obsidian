![[Pasted image 20220724100128.png]]
```CPP
void append(Node *last, int data)
{
    Node *temp = (Node *)malloc(sizeof(Node));

    temp->data = data;

    temp->next = last->next;
    last->next = temp;
    last = temp;
}
```