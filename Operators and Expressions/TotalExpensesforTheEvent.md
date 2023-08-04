# Total Expenses for the Event

The prime functionality of an Event Management System is budgeting. An Event Management System should estimate the total expenses incurred by an event and the percentage rate of each of the expenses involved in planning and executing an event. Nikhil, the founder of "Pine Tree" wanted to include this functionality in his company’s Amphi Event Management System and requested your help in writing a program for the same.
The program should get the branding expenses, travel expenses, food expenses and logistics expenses as input from the user and calculate the total expenses for an event and the percentage rate of each of these expenses.

**Input format :** <br>
First input is a double value that corresponds to the branding expenses.
Second input is a double value that corresponds to the travel expenses.
Third input is a double value that corresponds to the food expenses.
Fourth input is a double value that corresponds to the logistics expenses.

**Output format :** <br>
First line of the output should display the double value that corresponds to the total expenses for the Event.
Next four lines should display the percentage rate of each of the expenses.
Round off the output to two decimal digits.

**Sample test cases :**<br>
**Input 1 :**<br>
20000<br>
40000<br>
15000<br>
25000<br>
**Output 1 :**<br>
Total expenses : Rs.100000.00<br>
Branding expenses percentage : 20.00%<br>
Travel expenses percentage : 40.00%<br>
Food expenses percentage : 15.00%<br>
Logistics expenses percentage : 25.00%

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<bits/stdc++.h>
using namespace std;
int main()
{
   int brand,food,travel,logistics;double tot_exp=0.00;
   double branding_exp_per=0.00,travel_exp_per=0.00,food_exp_per=0.00,logistics_exp_per=0.00;
 cin >> brand;
 cin >> travel;
 cin >> food;
 cin >> logistics;
tot_exp= brand + travel + food + logistics;
branding_exp_per=(brand/tot_exp)*100;
travel_exp_per=(travel/tot_exp)*100;
food_exp_per=(food/tot_exp)*100;
logistics_exp_per=(logistics/tot_exp)*100;
cout << fixed << setprecision(2)<<"Total expenses : Rs."<< tot_exp;
cout <<fixed << setprecision(2)<<"\nBranding expenses percentage : "<<branding_exp_per<<"%";
cout <<fixed << setprecision(2)<<"\nTravel expenses percentage : "<<travel_exp_per<<"%";
cout <<fixed << setprecision(2)<<"\nFood expenses percentage : "<<food_exp_per<<"%";
cout <<fixed << setprecision(2)<<"\nLogistics expenses percentage : "<<logistics_exp_per<<"%";
return 0;
}



```
