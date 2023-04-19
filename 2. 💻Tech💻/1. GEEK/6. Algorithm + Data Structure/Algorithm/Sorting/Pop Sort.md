```cpp
void pop_sort(int arr[], int size){
    for(int i = 2; i < size+1;i++)
        for(int j = 1; j <size;j++){
            if (arr[size-j] < arr[size-i]){
                int tmp = arr[size-j];
                arr[size-j] = arr[size-i];
                arr[size-i] = tmp;
            }
        }
}
```

- compare the last element and the second last element
	- if the last is smaller, it will be moved one to left
- O（n2）