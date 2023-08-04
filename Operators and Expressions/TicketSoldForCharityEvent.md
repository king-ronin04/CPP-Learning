# Tickets sold for Charity Event
HelpIndia, a famous NGO has been selective in identifying events to raise funds for charity. Suzanne is a volunteer from the NGO who was selling tickets to the public for the charity event. She sold 'X' more adult tickets than children tickets and she sold twice as many senior tickets as children tickets. Assume that an adult ticket costs 
2 and senior ticket costs $3.

Suzanne made 'Y' dollars from ticket sales. Find the number of adult tickets, children tickets, and senior tickets sold.

#### Input format :
The first input is an integer value X that corresponds to the number of adult tickets more than children tickets.
<br>
The second input is an integer value Y that corresponds to the money in dollars made by Suzanne from ticket sales.

#### Output format :
The first line of the output should display the number of children tickets sold.
<br>
The second line of the output should display the number of adult tickets sold.
<br>
The third line of the output should display the number of senior tickets sold.

**Sample test cases :<br>
Input 1 :<br>**
10<br>
700<br>
**Output 1 :<br>**
Number of children tickets sold : 50<br>
Number of adult tickets sold : 60<br>
Number of senior tickets sold : 100


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
   int x,y,child_tickets,adult_tickets,senior_tickets;
 cin >> x;
 cin >> y;
  child_tickets=(y-(5*x))/13;
  adult_tickets=child_tickets+x;
  senior_tickets=2*child_tickets;
cout<<"Number of children tickets sold : "<<child_tickets;
cout<<"\nNumber of adult tickets sold : "<<adult_tickets;
cout<<"\nNumber of senior tickets sold : "<<senior_tickets;
return 0;
}



```
