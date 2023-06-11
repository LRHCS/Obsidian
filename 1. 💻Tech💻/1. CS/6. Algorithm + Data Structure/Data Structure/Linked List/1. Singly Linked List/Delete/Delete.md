```CPP
void deleteNode(Node **head_ref, int key){
	Node* temp = *head_ref;
	Node* prev = NULL;
	if (temp != NULL && temp->data == key){
		*head_ref = temp->next;
		delete temp;
		return;
	}

	else{
		while(temp -> data != key && temp != NULL){
			prev =temp;
			temp = temp->next
		}
		if (temp == NULL){
			return
		}
		prev->next = temp->next
		delete temp;
	}
}
```