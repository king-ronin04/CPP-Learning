# Bank Account

A class which inherits another class obtains all the latter's attributes and methods is called inheritance. The former is called Child class whilst the latter is called Parent class. This phenomenon would be very promising in applications dealing with multiple classes that are constituted by similar or more likely same attributes. You 'll get to know the importance of inheritance from the following problem. All type of accounts in a bank have common attributes which can be inherited from an Account class.

 

**Create a class Account with the following protected attributes**

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/ec7ff30f-ab1a-47f8-acba-968b17d45268)


Include appropriate getters and setters.
<br>
Include the following protected methods.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/ee420f64-fb5c-4535-9ccb-0c5332b2679c)


**Create a class CurrentAccount with following private attributes which extends Account class**

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/b061230a-b198-4850-a835-2ea45ecbea2e)


Create default constructor and a parameterized constructor

Include appropriate Accessors and Mutators.
<br>
Include the following public methods.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/803757f9-6919-494b-8994-34e04c821b82)


**Create a class SavingsAccount with following private attributes which extends Account class**

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/12c247d5-7e46-45a2-9e6e-a081e40dc680)


Create default constructor and a parameterized constructor.

Include appropriate Accessors and Mutators
<br>
Include the following public methods.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/1ad1d744-122b-4060-8846-0085e396f74b)


Create a driver class named Main to test the above class.

**Note:** Strictly adhere to the Object-Oriented Specifications given in the problem statement.All class names, attribute names and method names should be the same as specified in the problem statement.


#### Input format :
Choice of input
<br>
Bank details

#### Output format :
Prints the bank details

**Sample test cases :<br>
Input 1 :<br>**
1<br>
Ankit 8789766554 IndianBank Coimbatore<br>
**Output 1 :<br>**
Ankit<br>
8789766554<br>
IndianBank<br>
Coimbatore

**Input 2 :<br>**
2<br>
Ankit 785638576 IndianBank 475345<br>
**Output 2 :<br>**
Ankit<br>
785638576<br>
IndianBank<br>
475345


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
#include <cstring>
using namespace std;
class Account {
	protected: string accName;
	protected: string accNo;
	protected: string bankName;
	public:
	string getAccName() {
		return accName;
	}
	public:
	void setAccName(string aN) {
		accName = aN;
	}
	public:
	string getAccNo() {
		return accNo;
	}
	public:
	void setAccNo(string acNo) {
		accNo = acNo;
	}
	public:
	string getBankName() {
		return bankName;
	}
	public:
	void setBankName(string bN) {
		bankName = bN;
	}
	protected:
	void display() {
		cout<<accName;
	    cout<<accNo;
	    cout<<bankName;
	}
};
class CurrentAccount :public Account {
private: string tinNumber;

public: 
string getTinNumber() {
	return tinNumber;
}

public:
void setTinNumber(string tN) {
	tinNumber = tN;
}
public:
CurrentAccount() {};
public :
CurrentAccount(string accName1,string accNo1,string bankName1,string tinNumber1) {
	accName = accName1;
	accNo = accNo1;
	bankName = bankName1;
	tinNumber = tinNumber1;
}
public:
void display() {
	cout<<accName<<"\n";
	cout<<accNo<<"\n";
	cout<<bankName<<"\n";
	cout<<tinNumber;
}
};
class SavingsAccount:public Account {
	private:
	string orgName;
	public:
	SavingsAccount() {};
	public :
	SavingsAccount(string accName2,string accNo2,string bankName2,string orgName2) {
		accName = accName2;
		accNo = accNo2;
		bankName = bankName2;
		orgName = orgName2;
	}
	public:
	string getOrgName() {
		return orgName;
	}
	public:
	void setOrgName(string oN) {
		orgName = oN;
	}
	public:
	void display() {
		cout<<accName<<"\n";
		cout<<accNo<<"\n";
		cout<<bankName<<"\n";
		cout<<orgName;
	}
};
int main() {
	int n;
	string accName,accNo,bankName,tinNumber,orgName;
	cin>>n;
	SavingsAccount s;
	CurrentAccount c;
	if(n == 1) {
	    cin>>accName;
	    cin>>accNo;
	    cin>>bankName;
	    cin>>orgName;
		s.setAccName(accName);
		s.setAccNo(accNo);
		s.setBankName(bankName);
		s.setOrgName(orgName);
		SavingsAccount s1 = SavingsAccount(s.getAccName(),s.getAccNo(),s.getBankName(),s.getOrgName());
		
		s1.display();
	}
	if(n == 2) {
	    cin>>accName;
	    cin>>accNo;
	    cin>>bankName;
	    cin>>tinNumber;
		c.setAccName(accName);
		c.setAccNo(accNo);
		c.setBankName(bankName);
		c.setTinNumber(tinNumber);
		CurrentAccount c1 =  CurrentAccount(c.getAccName(),c.getAccNo(),c.getBankName(),c.getTinNumber());
		c1.display();
	}

}

````

