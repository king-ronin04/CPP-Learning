# Grades of Rides
“AquaticaCarnival” is the most successful event dedicated to children and families. The Event has more than 20 rides for children and adults and the organizers always ensure not to compromise on the safety of the visitors.
<br>
To ensure the safety of the rides, the organizers have graded the rides in the fair according to the following conditions:
<br>
Hurl Factor must be greater than 50.
<br>
Spin Factor must be greater than 60.
<br>
Speed factor must be greater than 100.

The grades are as follows:
<br>
Grade is 10 if all three conditions are met.
<br>
Grade is 9 if conditions (i) and (ii) are met.
<br>
Grade is 8 if conditions (ii) and (iii) are met.
<br>
Grade is 7 if conditions (i) and (iii) are met.
<br>
Garde is 6 if only one condition is met.
<br>
Grade is 5 if none of three conditions are met.
<br>
Write a program display the grade of the rides, given the values of hurl factor, spin factor and speed factor of the ride under consideration.

#### Input format :
First line of the input consists of 3 integers that gives the Hurl Factor, Spin Factor and Speed Factor of the ride, each separated by a space.

#### Output format :
Output should display the grade of the ride depending on Conditions.

**Sample test cases :<br>
Input 1 :** <br> 
45 78 106 <br>
**Output 1 :**<br>
8


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int main()
{
    int hurl_factor,spin_factor,speed_factor;
    cin>>hurl_factor>>spin_factor>>speed_factor;
    if(hurl_factor>50 && spin_factor>60 && speed_factor>100)
    {
        cout<<"10";
    }
  else if(hurl_factor>50 && spin_factor>60)
    {
        cout<<"9";
    }
  else if(spin_factor>60 && speed_factor>100)
    {
        cout<<"8";
    }
    else if(hurl_factor>50 && speed_factor>100)
    {
        cout<<"7";
    }
    else if(hurl_factor>50 || spin_factor>60 || speed_factor>100)
    {
        cout<<"6";
    }
    else
    {
        cout<<"5";
    }
    return 0;
}


```
