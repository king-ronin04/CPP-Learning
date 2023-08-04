# Trade Fair
 
Trade Fairs are important for companies to present their products and to get in touch with its customers and business parties. One such grandeur Trade Fair Event was organized by the Confederation of National Large Scale Industry.
Number of people who attended the event on the first day was x. But as days progressed, the event gained good response and the number of people who attended the event on the second day was twice the number of people who attended on the first day. Unfortunately due to heavy rains on the third day, the number of people who attended the event was exactly half the number of people who attended on the first day.
 
Given the total number of people who have attended the event in the first 3 days, find the number of people who have attended the event on day 1, day 2 and day 3.

**Input format :**
<br>
First line of the input is an integer value that corresponds to the total number of people.

**Output format :**
<br>
First line of the output should display the number of attendees on day 1.
<br>
Second line of the output should display the number of attendees on day 2.
<br>
Third line of the output should display the number of attendees on day 3.
<br>

**Sample test cases :**

**Input 1 :** <br>
10500

**Output 1 :** <br>
Number of attendees on day 1 : 3000
<br>
Number of attendees on day 2 : 6000
<br>
Number of attendees on day 3 : 1500

--------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
   int tot,day1,day2,day3;
 cin >> tot;
day1=(tot*2)/7;
day2=day1*2;
day3=day1/2;
cout<<"Number of attendees on day 1 : "<<day1;
cout<<"\nNumber of attendees on day 2 : "<<day2;
cout<<"\nNumber of attendees on day 3 : "<<day3;
return 0;
}


```


