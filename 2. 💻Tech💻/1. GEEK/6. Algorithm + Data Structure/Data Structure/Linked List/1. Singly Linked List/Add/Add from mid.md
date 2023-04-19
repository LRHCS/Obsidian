![[Pasted image 20220723100130.png]]
```CPP
void insertAfter(Node *prev_node, int data){
	if (prev_node == NULL){
		cout << "it cant be null";
	}
	Node* new_node = new Node();

	new_node -> data = data;
	new_node->next = prev_node->next;
	prev_node->next = new_node;
}
```