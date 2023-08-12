# Operator Overloading

Write a program to overload the operator('+') to compute the sum of complex numbers

#### Input format :
Two sets of real and imaginary numbers

#### Output format :
Sum of real and imaginary numbers

**Sample test cases :<br>
Input 1 :<br>**
10 5<br>
2 4<br>
**Output 1 :<br>**
12 + i9


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream> 
using namespace std; 
class Complex { 
private: 
	int real, imag; 
public: 
	Complex(int r = 0, int i =0) {
	    real = r; imag = i;
	    
	} 
	Complex operator + (Complex const &obj) { 
		Complex res; 
		res.real = real + obj.real; 
		res.imag = imag + obj.imag; 
		return res; 
	} 
	void print() { 
	    cout << real << " + i" << imag << endl; 
	    
	} 
}; 

int main() 
{ 
    int r1,i1,r2,i2;
    cin>>r1>>i1>>r2>>i2;
	Complex c1(r1, i1), c2(r2, i2); 
	Complex c3 = c1 + c2; 
	c3.print(); 
} 

````
