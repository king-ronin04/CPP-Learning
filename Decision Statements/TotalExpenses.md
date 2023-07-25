# Total Expenses

The much awaited event at the entertainment industry every year is the "Screen Awards". This year the event is going to be organized on December 25 to honour the Artists for their professional excellence in Cinema. The Organizers has this time decided to launch an online portal to facilitate easy booking of the Award show’s tickets.

They specifically wanted to provide an option for bulk booking in the portal, wherein there are many discounts announced. Write a program to help the Organizers to create the portal as per the requirement given below.

Given the ticket cost as 'X'.
<br>
If the number of tickets purchased is less than 50, there is no discount.
<br>
If the number of tickets purchased is between 50 and 100 (both inclusive), then 10% discount is offered.
<br>
If the number of tickets purchased is between 101 and 200(both inclusive), 20% discount is offered.
<br>
If the number of tickets purchased is between 201 and 400(both inclusive), 30% discount is offered.
<br>
If the number of tickets purchased is between 401 and 500(both inclusive), 40% discount is offered.
<br>
If the number of tickets purchased is greater than 500, then 50% discount is offered.

#### Input format :
First line of the input is an integer that corresponds to the cost of the ticket ‘X’.
<br>
Second line of the input is an integer that corresponds to the number of tickets purchased.

#### Output format :
Output should display a double value, which gives the total expenses in purchasing the tickets after discounts.

**Sample test cases :** <br>
**Input 1 :** <br>
100<br>
5<br>
**Output 1 :** <br>
500

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
using namespace std;
int main()
{
    int ticket_cost,num_of_tickets;
    double tot,sub_tot,discount;
    cin>>ticket_cost;
    cin>>num_of_tickets;
    tot= ticket_cost*num_of_tickets;
if(num_of_tickets<50)
    {
        cout<<tot;
    }
else if(num_of_tickets>=50&&num_of_tickets<=100)
    {
   sub_tot=tot*(0.1);
   discount=tot-sub_tot;
   cout<<discount;
    }
else if(num_of_tickets>=101&&num_of_tickets<=200)
    {
   sub_tot=tot*(0.2);
   discount=tot-sub_tot;
   cout<<discount;
    }
else if(num_of_tickets>=201&&num_of_tickets<=400)
    {
   sub_tot=tot*(0.3);
   discount=tot-sub_tot;
   cout<<discount;
    }
else if(num_of_tickets>=401&&num_of_tickets<=500)
    {
   sub_tot=tot*(0.4);
   discount=tot-sub_tot;
   cout<<discount;
    }
else if(num_of_tickets>500)
    {
   sub_tot=tot*(0.5);
   discount=tot-sub_tot;
   cout<<discount;
    }
    return 0;
}


```
