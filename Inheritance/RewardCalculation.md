# Reward calculation

A new announcement has been made by the Mayor, the Fair will be on for more than a month. For rewarding customers who actively purchase in the fair, the developers are asked to compute reward points for credit card purchasing. For a small demo implementation, we now compute reward points for VISA card and HP VISA card. The reward points for VISA card is 1% of the spending for all kinds of purchases. For HP Visa card, 10 additional points are given for fuel purchases. Also, include method Overriding for the method computeRewardPoints() which computes the reward points for both types. write a program using the above specification for computing the reward points.

Create a class named VISACard with the following private attributes

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/70ccc63a-2acd-4082-8b82-4e4085ec029f)


the VISACard class has the following methods

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/cfffb99f-1347-4508-86d0-a73a42ab7190)




Create a class named HPVISACard that extends VISACard with the following methods

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/cd343b66-d8c3-412b-b2c3-fdfd16e2b77a)


Create a driver class called Main. In the Main method, obtain inputs from the user and compute the reward points by calling appropriate methods. If choice other than specified is chosen, print "Invalid choice"

**Note:** Display two digit after the decimal point for Double values.

**[Strictly adhere to the Object-Oriented Specifications given in the problem statement.
<br>
All class names, attribute names and method names should be the same as specified in the problem statement.]**

#### Input format :
Account holder Name
<br>
CCV
<br>
Amount
<br>
Purchase type
<br>
Choice

#### Output format :
Displays the reward points

**Sample test cases :<br>
Input 1 :<br>**
Sharma<br>
7908-2937-1820-0012<br>
1000<br>
fuel<br>
1<br>
**Output 1 :<br>**
10.00

**Input 2 :<br>**
Sharma<br>
7908-2937-1820-0012<br>
1000<br>
fuel<br>
2<br>
**Output 2 :<br>**
20.00

**Input 3 :<br>**
Sharma<br>
7908-2937-1820-0012<br>
1000<br>
fuel<br>
3<br>
**Output 3 :<br>**
Invalid Choice


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<cstring>
#include<iomanip>
using namespace std;
class VISACard {
	private: string holderName;
	private: string ccv;
	public :double computeRewardPoints(string purchaseType, double amount) {
		double dis = 0.01*amount;
		return dis;
	}
	public: string getHolderName() {
		return holderName;
	}
	public:void setHolderName(string holder) {
		holderName = holder;
	}
	public: string getCcv() {
		return ccv;
	}
	public: void setCcv(string cv) {
	     ccv = cv;
	}
	
};
class HPVISACard : public VISACard {
	public: double computeRewardPoints(string purchaseType, double amount) {
      double dis=VISACard::computeRewardPoints(purchaseType, amount);
		if(purchaseType.compare("fuel") == 0) {
			return dis+10;
		}
		else {
			return dis;
		}
		
	}
};

int main() {
		VISACard v ;
		HPVISACard h ;
		string holderName;
		string ccv;
		v.setHolderName(holderName);
		v.setCcv(ccv);
		double amount;
		string type ;
		int n;
		cin>>holderName>>ccv>>amount>>type;
		cin>>n;
		if(n == 1) {
		    
			double res = v.computeRewardPoints(type, amount);
			cout<<fixed<<setprecision(2)<<res;
		}
		if(n == 2) {
		    
			double res = h.computeRewardPoints(type, amount);
			cout<<fixed<<setprecision(2)<<res;
		}
		if(n>2) {
			cout<<"Invalid Choice";
		}
		
	  return 0;
}

````
