![[Pasted image 20220724100106.png]]
```CPP
void addToEmpty(Node *last, int data)
{
    if (last != NULL)
    {
        return;
    }

    Node *temp = (Node *)malloc(sizeof(struct Node));

    temp->data = data;
    last = temp;
    temp->next = last;
}
```