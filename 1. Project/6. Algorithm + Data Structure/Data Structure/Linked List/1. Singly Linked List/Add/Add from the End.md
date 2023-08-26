![[Pasted image 20220723103134.png]]
```CPP
void append(Node **head_ref, int data){
	Node *new_node = new Node();
	Node *last = *head_ref;
	new_node->data = data;
	new_node->next = NULL;
	if (*head_ref == NULL){
		*head_ref = new_node;
		return
	}
    while (last->next != NULL)
    {
        last = last->next;
    }
    last->next = new_node;
    return;
}
```