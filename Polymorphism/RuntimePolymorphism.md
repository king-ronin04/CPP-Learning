# Runtime polymorphism

A virtual function can be defined as the member function within a base class which you expect to redefine in derived classes.Write a program to compute the area of rectangle.Override the virtual function calculateArea() in the derived class to compute the area.Obtain the input from user and display output on the console.

#### Input format :
Length and breadth

#### Output format :
Area of rectangle

**Sample test cases :<br>
Input 1 :<br>**
10 20<br>
**Output 1 :<br>**
200


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <bits/stdc++.h> 
using namespace std; 
class ComputeArea 
{ 
    public:double area;
public: 
	virtual void calculateArea() 
	{ 
	    area=0;
	} 
}; 
class Rectangle:public ComputeArea 
{ 
    public:int length;
    public:int breadth;
    public:
    int getLength(){
        return length;
    }
    public:
    void setLength(int l){
        length = l;
    }
    public:
    int getBreadth(){
        return breadth;
    }
    public:
    void setBreadth(int b){
        breadth = b;
    }
public: 
	void calculateArea () 
	{ 
	    area=length*breadth;
	    cout<<area;
	} 

}; 
int main() 
{ 
	ComputeArea bptr; 
	Rectangle d; 
	
int length,breadth;
cin>>length>>breadth;
d.setLength(length);
d.setBreadth(breadth);
	bptr.calculateArea(); 
	d.calculateArea();
	return 0; 
} 

````
