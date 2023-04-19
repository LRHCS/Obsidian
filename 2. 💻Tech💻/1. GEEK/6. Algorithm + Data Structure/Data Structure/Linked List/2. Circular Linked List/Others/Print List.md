```CPP
void printList(Node *head)
{
    while (head->next != NULL)
    {
        cout << head->data << " ";
        head = head->next;
    }
}
```