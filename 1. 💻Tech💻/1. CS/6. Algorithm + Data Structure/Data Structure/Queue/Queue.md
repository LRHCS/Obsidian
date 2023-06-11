First In First Out

![[Pasted image 20221224191027.png]]
![[Pasted image 20221224191038.png]]

```cpp
    queue<int> q;

    queue<int> q1;

    q.push(10);

    q.push(20);

    print_queue(q);

    cout << q.size() << endl;

    q.pop();

    print_queue(q);

    cout << q.size() << endl;

    q.push(20);

    print_queue(q);

  

    q1.push(10);

    q1.push(30);

    q.swap(q1);

    print_queue(q);

    print_queue(q1);
```