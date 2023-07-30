```CPP
void deleteNode(Node** head_ref, Node* del)
{
	/* base case */
	if (*head_ref == NULL || del == NULL)
		return;

	/* If node to be deleted is head node */
	if (*head_ref == del)
		*head_ref = del->next;

	/* Change next only if node to be
	deleted is NOT the last node */
	if (del->next != NULL)
		del->next->prev = del->prev;

	/* Change prev only if node to be
	deleted is NOT the first node */
	if (del->prev != NULL)
		del->prev->next = del->next;

	/* Finally, free the memory occupied by del*/
	free(del);
	return;
}
```