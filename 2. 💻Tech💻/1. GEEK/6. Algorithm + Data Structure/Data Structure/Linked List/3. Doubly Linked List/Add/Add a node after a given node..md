![[Pasted image 20220724111010.png]]
```CPP
/* Given a node as prev_node, insert
a new node after the given node */
void insertAfter(Node* prev_node, int new_data)
{
	/*1. check if the given prev_node is NULL */
	if (prev_node == NULL)
	{
		cout<<"the given previous node cannot be NULL";
		return;
	}

	/* 2. allocate new node */
	Node* new_node = new Node();

	/* 3. put in the data */
	new_node->data = new_data;

	/* 4. Make next of new node as next of prev_node */
	new_node->next = prev_node->next;

	/* 5. Make the next of prev_node as new_node */
	prev_node->next = new_node;

	/* 6. Make prev_node as previous of new_node */
	new_node->prev = prev_node;

	/* 7. Change previous of new_node's next node */
	if (new_node->next != NULL)
		new_node->next->prev = new_node;
}

// This code is contributed by shivanisinghss2110.

```