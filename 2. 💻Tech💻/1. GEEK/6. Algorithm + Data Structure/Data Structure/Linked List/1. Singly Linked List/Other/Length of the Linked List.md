```CPP
void lengthLinkedList(Node **head_ref){
	int length = 0;
	Node *temp = head_ref;
	while (temp != NULL){
		length +=1;
		temp = temp->next
	}
	cout << length;
}
```