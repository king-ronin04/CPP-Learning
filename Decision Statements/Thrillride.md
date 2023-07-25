# Thrill ride
"Fantasy Kingdom" is a brand new Amusement park that is going to be inaugurated shortly in the City and is promoted as the place for breath-taking charm. The theme park has more than 30 exhilarating and thrilling rides and as a special feature of the park, the park Authorities have placed many Booking Kiosks at the entrance which would facilitate the public to purchase their entrance tickets and ride tickets.

There are few rides in the park which are not suitable for Children and aged people, hence the park Authorities wanted to program the kiosks to issue the tickets based on people’s age. If the age given is less than 15 (Children) or greater than 60 (Aged), then the system should display as "Not Allowed", otherwise it should display as "Allowed". Write a block of code to help the Authorities program this functionality

#### Input format :
First line of the input is an integer that corresponds to the age of the person opting for the ride

#### Output format :
Output should display "Allowed" or "Not Allowed" based on the conditions given.

**Sample test cases : <br>
Input 1 :** <br>
22<br> 
**Output 1 :** <br>
Allowed 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
using namespace std;
int main()
{
    int age;
    cin>>age;
    if(age<15 || age>60)
       {
         cout<<"Not Allowed";
		}
	else
	{
	    cout<<"Allowed";

	}
    return 0;
}

```
