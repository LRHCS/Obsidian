![[Pasted image 20220723100143.png]]
```CPP
void push(Node **head_ref, int data){
	Node *new_node = new Node();
	new_node->next = (*head_ref);
	new_node->data = data;
	(*head_ref) = new_node;
}
```
