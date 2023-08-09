# Area of shape

Write a program to calculate the area of the circle and rectangle using overriding concept in java.

Create a class Shape with the following protected attributes,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/80e25999-efb1-4172-9b7a-678c02bb61cf)


Create the following method in the Shape class,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/82a69169-99b9-4689-8869-efa857108da6)


Create a class Circle which extends Shape with the following private attributes,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/07021f10-a658-4f0a-aa1a-11b0a7009105)


Override the following method in the Circle class,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/f434f3df-d721-4814-90c8-e278d96902bd)


Create a class Rectangle which extends Shape with the following private attributes,

  
![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/1cbfe6e9-e8d8-4e14-ac77-c7613122726a)



Override the following method in the Rectangle class,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/5d7c91d3-d943-475f-b0a9-6914440bf5e2)


Create a class Triangle which extends Shape with the following private attributes,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/35dd37db-0025-4b0b-96cb-77cd30063158)


Override the following method in the Triangle class,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/9f7e40eb-2414-4c56-8368-7c4523f8bc7d)


Get the option for the shape to compute area and get the attribute according to the shape option. Calculate the area and print the area.



Create a driver class Main to test the above classes.

**[Note: Strictly adhere to the object-oriented specifications given as a part of the problem statement.Use the same class names, attribute names and method names]**

#### Input format :
Choice of shape
<br>
Shape details

#### Output format :
Area of the shape

**Sample test cases :<br>
Input 1 :<br>**
1<br>
11<br>
**Output 1 :<br>**
379.94

**Input 2 :<br>**
2<br>
10<br>
25<br>
**Output 2 :<br>**
250.00

**Input 3 :<br>**
3<br>
15<br>
19<br>
**Output 3 :<br>**
142.50

**Input 4 :<br>**
4<br>
**Output 4 :<br>**
Invalid Input

-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include<iostream>
#include<iomanip>
using namespace std;
class Shape {
	protected:
	double area;
	
	public:
	void computeArea() {
		area =0 ;
	}

	public:
	double getArea() {
		return area;
	}

	public:
	void setArea(double area) {
		area = area;
	}
};
class Circle : public Shape {
	private:
	double radius;

	public:
	double getRadius() {
		return radius;
	}

	public:
	void setRadius(double r) {
		radius = r;
	}
	public:
	void computeArea() {
		
		area = 3.14*(radius*radius);
	cout<<fixed<<setprecision(2)<<area;
	}
};
class Rectangle:public Shape {
	private:
	double length;
	private:
	double breadth;
	public:
	double getLength() {
		return length;
	}
	public:
	void setLength(double l) {
		length = l;
	}
	public:
	double getBreadth() {
		return breadth;
	}
	public:
	void setBreadth(double b) {
		breadth = b;
	}
	public:
	void computeArea() {
		
		area = length*breadth;
			cout<<fixed<<setprecision(2)<<area;
	}
};
class Triangle : public Shape {
	private:
	double base;
	private:
	double height;
	public:
	double getBase() {
		return base;
	}
	public:
	void setBase(double ba) {
		base = ba;
	}
	public:
	double getHeight() {
		return height;
	}
	public:
	void setHeight(double he) {
		height = he;
	}
	public:
	void computeArea() {
		area = 0.5*base*height;
			cout<<fixed<<setprecision(2)<<area;
	}
};
int main() {

	int n;
    double radius,length,breadth,base,height;
	cin>>n;
	Circle c ;
	Rectangle r;
	Triangle t;
	if(n == 1) {
		cin>>radius;
		c.setRadius(radius);
		//cout<< c.getRadius();
		c.computeArea();
	}
	if(n == 2) {
		cin>>length;
		cin>>breadth;
		r.setLength(length);
		r.setBreadth(breadth);
		r.computeArea();
	}
	if(n == 3) {
		cin>>base;
		cin>>height;
		t.setBase(base);
		t.setHeight(height);
		t.computeArea();
	}
	if(n>3) {
		cout<<"Invalid Input";
	}

}

```
