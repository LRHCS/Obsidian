```cpp
void selection_sort(int arr[], int size){
    for (int i = 0; i < size;i++){
        int min = arr[i];
        for (int j = 0;j < size;j++){
            if(arr[j] > min){
               min = arr[j];        
                int tmp = arr[i];
                arr[i] = min;
                arr[j] = tmp;
            }
        }
    }
}
```

- Find the **smallest** number in the array
- swap it with the i-th element
- O（n2）
![[Pasted image 20221224210656.png]]
![[Pasted image 20221224210702.png]]