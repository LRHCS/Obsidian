```cpp
void binary_search(int arr[], int target, int l, int r){

    int mid = l + (r - l) / 2;

    if (arr[mid] > target){

        binary_search(arr, target, l, mid-1);

    }

    else if (arr[mid] == target){

        cout << "This number is found at index " << mid;

    }

    else if(arr[mid] < target){

        binary_search(arr, target, mid+1, r);

    }

}
```

![[Pasted image 20221228200011.png]]

- the array must be sorted
- O(log n)