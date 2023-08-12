# Overloading makePayment()

 

Consider doing an extra feature for the stage show organisers. Bring up an interactive console application for Billing so that our application looks unique from other competitors. Customers pay using cash, online wallets, and credit card. For each category obtain necessary information from the user. You also require a receipt for all the transactions which should be printed at the end of the transaction. Let's increase our coding proficiency by implement Function overloading for the payments. Hence write a program meeting all the above specification.

Create a class named TicketBooking with the following private attributes.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/fbfed2df-abd3-4fc2-ad33-41cdbc21fd68)


Include accessors and mutators for the class.
<br>
Include default and parameterized constructors.
<br>
The TicketBooking class has the following methods.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/1d190f9a-bb74-4d0b-9bc8-f123bd050dfc)



Create a driver class called Main. In the Main method, obtain input from the user and call appropriate methods for transactions. If choice other than specified is chosen, print "Invalid choice".
<br>
**Note:** display two digit after decimal point for double values.
<br>
Format for TicketBooking Input is stageEvent,customer,noOfSeats

**[Strictly adhere to the Object-Oriented Specifications given in the problem statement.
<br>
All class names, attribute names and method names should be the same as specified in the problem statement.]**



Create an object for TicketBooking class t.

**Function call:**
<br>
makePayment(amount)
<br>
makePayment(walletNumber, amount)
<br>
makePayment(type, ccv, name, amount)

#### Input format :
Ticket booking details

#### Output format :
Output prints the booking details

**Sample test cases :<br>
Input 1 :<br>**
Dance Abishek 5 <br>
1<br>
500<br>
**Output 1 :<br>**
Dance Abishek 5 500.00

**Input 2 :<br>**
Dance Abishek 5 <br>
2<br>
500<br>
AFG-456<br>
**Output 2 :<br>**
Dance Abishek 5 500.00 AFG-456

**Input 3 :<br>**
Dance Abishek 5 <br>
3<br>
Sheriff<br>
500<br>
Master<br>
899-834-273<br>
**Output 3 :<br>**
Dance Abishek 5 Sheriff 500.00 Master 899-834-273

**Input 4 :<br>**
Dance Abishek 5<br> 
4<br>
**Output 4 :<br>**
Invalid Choice


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<cstring>
#include<iomanip>
using namespace std;
class TicketBooking {
	private :string stageEvent;
	private: string customer;
	private :int noOfSeats;
	
	public: TicketBooking(string stageEvent1, string customer1, int  noOfSeats1) {
		stageEvent = stageEvent1;
		customer = customer1;
		noOfSeats = noOfSeats1;
	}
	public: void makePayment(string creditCard,string ccv,string name,double amount) {
		cout<<stageEvent<<" "<<customer<<" "<<noOfSeats<<" "<<name<<" "<<fixed<<setprecision(2)<<amount<<" "<<creditCard<<" "<<ccv;
	}
	public :void makePayment(string walletNumber ,double amount) {
		cout<<stageEvent<<" "<<customer<<" "<<noOfSeats<<" "<<fixed<<setprecision(2)<<amount<<" "<<walletNumber;
	}
	public: void makePayment(double amount) {
		cout<<stageEvent<<" "<<customer<<" "<<noOfSeats<<" "<<fixed<<setprecision(2)<<amount;
	}
	public: string getStageEvent() {
		return stageEvent;
	}
	public: void setStageEvent(string stageEv) {
		stageEvent = stageEv;
	}
	public :string getCustomer() {
		return customer;
	}
	public: void setCustomer(string cust) {
		customer = cust;
	}
	public: int getNoOfSeats() {
		return noOfSeats;
	}
	public :void setNoOfSeats(int noOfS) {
		noOfSeats = noOfS;
	}
};
int main() {
		string details;
		string stageEvent,customer;
		int noOfSeats;
		cin>>stageEvent>>customer>>noOfSeats;
		TicketBooking t = TicketBooking(stageEvent,customer,noOfSeats);
		int n;
		cin>>n;
		if(n == 1) {
			double amount;
			cin>>amount;
			t.makePayment(amount);
		}
		if(n == 2) {
			double amount ;
			cin>>amount;
			string walletNumber;
			cin>>walletNumber;
			t.makePayment(walletNumber, amount);
		}
		if(n == 3) {
			string name;
			cin>>name;
			double amount;
			cin>>amount;
			string type;
			cin>>type;
			string ccv ;
			cin>>ccv;
			t.makePayment(type, ccv, name, amount);
		}
		if(n>3) {
			cout<<"Invalid Choice";
		}
	return 0;
}
````
