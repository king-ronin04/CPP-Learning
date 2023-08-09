# Abstraction

Access specifiers are the main pillar of implementing abstraction in C++. Say, the members that defines the internal implementation can be marked as private in a class. And the important information needed to be given to the outside world can be marked as public. And these public members can access the private members as they are inside the class. Write a program to add two integers using abstract method display() to obtain the results.

#### Input format :
Two integers in a separate line

#### Output format :
Sum of two integers

**Sample test cases :<br>
Input 1 :<br>**
5<br>
6<br>
**Output 1 :<br>**
11


-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream> 
using namespace std; 
class implementAbstraction 
{ 
	private: 
		int a, b; 

	public: 
		void set(int x, int y) 
		{ 
			a = x; 
			b = y; 
		} 
		
		void display() 
		{ 
		    int sum=a+b;
			cout<<sum<< endl; 
			
		} 
}; 

int main() 
{ 
	implementAbstraction obj; 
	int a,b;
	cin>>a>>b;
	obj.set(a,b); 
	obj.display(); 
	return 0; 
} 

```
