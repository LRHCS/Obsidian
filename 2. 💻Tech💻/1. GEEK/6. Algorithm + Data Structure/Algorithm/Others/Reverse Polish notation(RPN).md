![[Pasted image 20230419184925.png]]
- while 有输入
    -   读入下一个符号X
    -   IF X是一个操作数
        -   入栈
    -   ELSE IF X是一个操作符
        -   有一个先验的表格给出该操作符需要n个参数
        -   IF堆栈中少于n个操作数
            -   **（错误）** 用户没有输入足够的操作数
        -   Else，n个操作数出栈
        -   计算操作符。
        -   将计算所得的值入栈
-   IF栈内只有一个值
    -   这个值就是整个计算式的结果
-   ELSE多于一个值
    -   **（错误）** 用户输入了多余的操作数

```cpp
#include <iostream>
#include<queue>
#include<stack>
#define ERROR 0
#define OK 1

using namespace std;

typedef int Staus;
typedef double ElemType;

bool Get_ops(stack<ElemType>* st, ElemType* op1, ElemType* op2)
{
	if (st->size() < 2)
		return ERROR;
	*op1 = st->top();
	st->pop();
	*op2 = st->top();
	st->pop();

	return OK;
}

Staus Solve(stack<ElemType>* st, char oper)
{
	bool flag = 0;
	ElemType oper1, oper2;
	flag = Get_ops(st, &oper1, &oper2);
	if (flag)
	{
		switch (oper)
		{
		case('+'):st->push(oper2 + oper1); break;
		case('-'):st->push(oper2 - oper1); break;
		case('*'):st->push(oper2 * oper1); break;
		case('/'):if (!oper1)
		{
			cout << "Divide by 0！" << endl;
			return ERROR;
		}
				 else st->push(oper2 / oper1);
			break;
		case('^'):st->push(pow(oper2, oper1)); break;
		}
	}
	else return ERROR;

	return OK;
}

int main()
{
	stack<ElemType> suffix;
	char c;
	ElemType t;
	c = getchar();
	while (c != '#')
	{
		switch (c)
		{
		case(' '):break;
		case('+'):;
		case('-'):;
		case('*'):;
		case('/'):;
		case('^'):Solve(&suffix, c); break;
		default:ungetc(c, stdin);
			cin >> t;
			suffix.push(t);
		}
		c = getchar();
	}
	cout << suffix.top() << endl;
	return 0;
}
```