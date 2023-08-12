# Overloading-basic

 Whenever you need to perform the same operation for different types of data, using different method names for each type can be cumbersome. In these cases we use overloading. Method overloading is the ability to create multiple methods with same name and different types of parameters. Calls to an overloaded function will run a specific implementation of that method appropriate to the type of arguments.Create a class Stall with following attributes,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/e106336b-c1d5-49f6-944f-653acfbbd3b1)


So now let's try out a simple example in our application. Consider stalls, they can be "gold", "Diamond","Platinum" types. And they may or may not have a TV in them. So we are gonna overload a method to find the cost of the stall.

Mark them as protected and add appropriate getters/setters.Override the following method in it,

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/2a73e7d2-f1ce-4f20-a922-a97d5481b741)


**Note:** The price for various types of stalls is, Platinum = Rs.200 per sqft; Diamond = Rs.150 per sqft; Gold = Rs.100 per sqft. And price for each tv is Rs.10000.

Create an object for the class Stall st.

**Function Call:**
<br>
﻿computeCost(type,size)
<br>
computeCost(type, size,noOfTV)


#### Input format :
Stall details
<br>
Refer sample input

#### Output format :
Cost of the stall

**Sample test cases :<br>
Input 1 :<br>**
Foodstall<br>
Food<br>
George<br>
Platinum<br>
1000<br>
4<br>
**Output 1 :<br>**
240000.00

**Input 2 :<br>**
Foodstall<br>
Food<br>
George<br>
Gold<br>
1000<br>
4<br>
**Output 2 :<br>**
140000.00

**Input 3 :<br>**
Foodstall<br>
Food<br>
George<br>
Diamond<br>
1000<br>
4<br>
**Output 3 :<br>**
190000.00



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<iomanip>
#include<cstring>
using namespace std;
class Stall {
protected: string name;
protected :string detail;
protected :string ownerName;
public :string getName() {
	return name;
}
public :void setName(string na) {
	name = na;
}
public: string getDetail() {
	return detail;
}
public :void setDetail(string det) {
	detail = det;
}
public :string getOwnerName() {
	return ownerName;
}
public: void setOwnerName(string ownerNa) {
	ownerName = ownerNa;
}
public: double computeCost(string stallType, int squareFeet) {
	double result=0;
	if(stallType.compare("Platinum") == 0) {
		result = squareFeet*200;
	}
	else if(stallType.compare("Diamond") == 0) {
		result = squareFeet*150;
	}
	else if(stallType.compare("Gold") == 0) {
		result = squareFeet*100;
	}
	return result;
}
public: double computeCost(string stallType, int squareFeet, int numberOfTV) {
	double res = numberOfTV*10000;
	return res;
}
};
int main(){
	Stall st;
	string name,detail,ownerName;
	cin>>name;
	cin>>detail;
	cin>>ownerName;
	st.setName(name);
	st.setDetail(detail);
	st.setOwnerName(ownerName);
	string type;
	int size,noOfTV;
	cin>>type;
	cin>>size ;
	cin>>noOfTV ;
	double a1 = st.computeCost(type,size);
	double a2 = st.computeCost(type, size,noOfTV);
	cout<<fixed<<setprecision(2)<<a1+a2;
}

#include<iostream>
#include<iomanip>
#include<cstring>
using namespace std;
class Stall {
protected: string name;
protected :string detail;
protected :string ownerName;
public :string getName() {
	return name;
}
public :void setName(string na) {
	name = na;
}
public: string getDetail() {
	return detail;
}
public :void setDetail(string det) {
	detail = det;
}
public :string getOwnerName() {
	return ownerName;
}
public: void setOwnerName(string ownerNa) {
	ownerName = ownerNa;
}
public: double computeCost(string stallType, int squareFeet) {
	double result=0;
	if(stallType.compare("Platinum") == 0) {
		result = squareFeet*200;
	}
	else if(stallType.compare("Diamond") == 0) {
		result = squareFeet*150;
	}
	else if(stallType.compare("Gold") == 0) {
		result = squareFeet*100;
	}
	return result;
}
public: double computeCost(string stallType, int squareFeet, int numberOfTV) {
	double res = numberOfTV*10000;
	return res;
}
};
int main(){
	Stall st;
	string name,detail,ownerName;
	cin>>name;
	cin>>detail;
	cin>>ownerName;
	st.setName(name);
	st.setDetail(detail);
	st.setOwnerName(ownerName);
	string type;
	int size,noOfTV;
	cin>>type;
	cin>>size ;
	cin>>noOfTV ;
	double a1 = st.computeCost(type,size);
	double a2 = st.computeCost(type, size,noOfTV);
	cout<<fixed<<setprecision(2)<<a1+a2;
  return 0;
}

````
