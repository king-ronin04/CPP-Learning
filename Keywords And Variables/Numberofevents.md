# Number of events
"Pine Tree" Company has signed up a big time Event Management deal from the Rotary Youth Club for a Trade Fair organized at Codissia Complex, wherein all startup companies in the Software industry are demonstrating their latest products and services and meet with industry partners and Customers.

Examly Event Management System has to be modified to write a piece of code that will get the input of the number of events to be hosted for the Fair at Codissia from its users and display the same. Help the company to accomplish the requirement.

#### Input format :
First line of the input is an integer that corresponds to the number of events to be hosted at Codissia

#### Output format :
Output should display the number of events to be hosted at Codissia

**Sample test cases : <br>
Input 1 :** <br>
10<br>
**Output 1 :** <br>
Number of events hosted in Codissia is 10<br>

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int main()
{
   int num_of_events;
 cin >> num_of_events;
 cout << "Number of events hosted in Codissia is "<<num_of_events ;
return 0;
}


```
