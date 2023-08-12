# Multilevel inheritance



We can implement multi-level inheritance in our application. Let's consider the domain 'Stall' and its types. There exists a multilevel inheritance.


**Create a class SilverStall with following protected attributes**

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/da5485b5-af1a-451e-94fa-a4d6fae4180c)


Create default constructor and a parameterized constructor.
<br>
**Include appropriate accessors and mutators.
<br>
Total cost computes only the stall cost.**



**Create a class GoldStall which extends SilverStall with following private attributes**

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/560768ed-d9dc-42d4-bcc7-106f95ac6f8e)


Create default constructor and a parameterized constructors
<br>
Include appropriate accessors and mutators.
<br>
Total cost computed by stall cost and TV set cost. Each TV set costs 100Rs.
<br>
**Create a class PlatinumStall which extends GoldStall (i.e Multilevel Inheritance) with following private attributes**

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/f7bc31bc-5153-4f41-a6f2-db1e22ca20a1)


Create default constructor and a parameterized constructor
<br>
Include appropriate **accessors and mutators.**
<br>
Total cost computed by stall cost,TV set cost and projector cost where each TV set and projector costs 100Rs and 500Rs respectively.
<br>
Create a driver class named **Main** to test the above class.

**Note:** Strictly adhere to the Object-Oriented Specifications given in the problem statement.All class names, attribute names and method names should be the same as specified in the problem statement.

#### Input format :
Choice of input
<br>
Stall details

#### Output format :
Total cost based on the stallType

Refer sample output

**Sample test cases :<br>
Input 1 :<br>**
1<br>
FoodStall<br>
Food<br>
Ankit<br>
1000<br>
**Output 1 :<br>**
1000

**Input 2 :<br>**
2<br>
FoodStall<br>
Food<br>
Ankit<br>
1000<br>
5<br>
**Output 2 :<br>**
1500

**Input 3 :<br>**
3<br>
FoodStall<br>
Food<br>
Ankit<br>
1000<br>
5<br>
2<br>
**Output 3 :<br>**
2500



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<cstring>
using namespace std;
class SilverStall {
	protected: string name;
	protected: string detail;
	protected: string owner;
	protected: int cost;
	public:
	SilverStall(string name1, string detail1, string owner1, int cost1) {
		name = name1;
		detail = detail1;
		owner = owner1;
		cost = cost1;
	}
	public :
	SilverStall() {};
	public :
	string getName() {
		return name;
	}
	public :
	void setName(string na) {
		name = na;
	}
	public: string getDetail() {
		return detail;
	}
	public :
	void setDetail(string de) {
		detail = de;
	}
	public: string getOwner() {
		return owner;
	}
	public :
	void setOwner(string ow) {
		owner = ow;
	}
	public :
	int getCost() {
		return cost;
	}
	public:
	void setCost(int co) {
		cost = co;
	}
	
};
class GoldStall : public SilverStall {
	private: int tvSet;

	public :
	GoldStall(string name2, string detail2, string owner2, int cost2, int tvSet2) {
		name = name2;
		detail = detail2;
		owner = owner2;
		cost = cost2;
		tvSet = tvSet2;
	}
	public:
	GoldStall() {};

	public:
	int getTvSet() {
		return tvSet;
	}

	public:
	void setTvSet(int tS) {
		tvSet = tS;
	}
	
};
class PlatinumStall :public GoldStall {
	private: int projector;

	public :
	PlatinumStall(string name3, string detail3, string owner3, int cost3, int tvSet3, int projector3) {
		name = name3;
		detail = detail3;
		owner = owner3;
		cost = cost3;
		
		//setTvSet(tvSet);
		projector = projector3;
}
	public:
	PlatinumStall() {};

	public :int getProjector() {
		return projector;
	}

	public: void setProjector(int pr) {
		projector = pr;
	}
};
int main() {
	int n,projector,tvSet,cost;
	string name,detail,owner;
	cin>>n;
	SilverStall s; 
	GoldStall g;
	PlatinumStall p;
	if(n == 1) {
	    cin>>name>>detail>>owner>>cost;
		s.setName(name);
		s.setDetail(detail);
		s.setOwner(owner);
		s.setCost(cost);
		SilverStall s1 = SilverStall(s.getName(),s.getDetail(),s.getOwner(),s.getCost());
		cout<<s.getCost();
	}
	if(n == 2) {
	    cin>>name>>detail>>owner>>cost>>tvSet;
		g.setName(name);
		g.setDetail(detail);
		g.setOwner(owner);
		g.setCost(cost);
		g.setTvSet(tvSet);
		GoldStall g1 = GoldStall(g.getName(),g.getDetail(),g.getOwner(),g.getCost(),g.getTvSet());
		cout<<g.getCost()+(g.getTvSet()*100);
	}
	if(n == 3) {
	    cin>>name>>detail>>owner>>cost>>tvSet>>projector;
		p.setName(name);
		p.setDetail(detail);
		p.setOwner(owner);
		p.setCost(cost);
		p.setTvSet(tvSet);
		p.setProjector(projector);
		PlatinumStall p1 = PlatinumStall(p.getName(),p.getDetail(),p.getOwner(),p.getCost(),p.getTvSet(),p.getProjector());
		cout<<p.getCost()+(p.getTvSet()*100)+(p.getProjector()*500);
	}
	if(n>3) {
		cout<<"Invalid Input";
	}
  
}

````
