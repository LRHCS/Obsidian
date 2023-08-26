get the gcd(**greatest common divisor**) of two numbers

```cpp
void euklid_algorithm(int num1, int num2){

    int gcd;

    if (num2 > num1){

        int tmp = num1;

        num1 = num2;

        num2 = tmp;

    }

    while (num1%num2!=0){

        gcd = num1%num2;

        num1 = num2;

        num2 = gcd;

    }

  

    cout << gcd;

}
```

- repeat
	- bigger num % smaller num
	- ![[Pasted image 20221226165439.png]]