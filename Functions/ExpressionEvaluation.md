# Expression Evaluation



In the Mini project 7th module is to evaluate the expression y = x + x^2+........+x^n. Rita allotted this function to Malini. Collect and display the values returned by the called function. Test your program and report the results obtained.
<br>
Help Malini to write a program to evaluate the expression?
<br>
Get the value of x and n from the user as input

**Use the following function:<br>**
int calculate(int x,int n)

where the first argument corresponds to the value of x and second corresponds to n respectively.

#### Input format :
The input consists of 2 integers

#### Output format :
The output prints the sum

**Sample test cases :<br>
Input 1 :<br>**
2 3<br>
**Output 1 :<br>**
14


-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
#include<cmath>
using namespace std;

int calculate(int x,int n) {
		int i,sum=0;
		for(i=1;i<=n;i++) {
			sum += pow(x, i);
		}
		return sum;
	}
	int main()
	{
		int x,n;
	    cin>>x>>n;
	cout<<calculate(x,n);
	}


```



