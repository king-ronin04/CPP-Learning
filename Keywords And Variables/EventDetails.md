# Event Details
Be it a last minute get together, a birthday party or corporate events, the "Pine Tree" Event Management Company helps you plan and execute it better and faster. Nikhil, the founder of the company wanted the Examly Event Management System to get and display the event details from his Customers for every new order of the Company.

Write a program that will get the input of the event details like name of the event, type of the event, number of people expected, a string value (Y/N) telling whether the event is going to be a paid entry and the projected expenses (in lakhs) for the event. The program should then display the input values as a formatted output.

#### Input format :
First input is a string that corresponds to the name of the event.
<br>
Second input is a string that corresponds to the type of the event.
<br>
Third input is an integer that corresponds to the number of people expected for the event.
<br>
Fourth input is a character that corresponds to Y/N telling whether the event is going to be a paid entry or not.
<br>
Fifth input is a double value that corresponds to the projected expenses (in lakhs) for the event.

#### Output format :
Output should display the event details as given in the sample output.

**Sample test cases : <br>
Input 1 :** <br> 
Food fest 2019 <br>
Public<br>
500<br>
N<br>
3.4<br>

**Output 1 :<br>**
Event Name :Food fest 2019<br>
Event Type :Public<br>
Expected Count :500<br>
Paid Entry : N<br>
Projected Expense :3.4L

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int main()
{
   char str[50],type[50];
   char choice;
   int num_of_people;
   float expenses;
 cin.getline(str,50);
 cin >> type;
 cin >> num_of_people;
 cin >> choice ;
 cin >> expenses;
cout << "Event Name :" << str;
cout <<"\nEvent Type :" <<type;
cout <<"\nExpected Count :"<<num_of_people;
cout <<"\nPaid Entry : "<<choice;
cout <<"\nProjected Expense :"<< expenses<<"L";
return 0;
}

```
