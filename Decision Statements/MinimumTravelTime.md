# Minimum Travel Time
The renowned book fair of the season "Publishers Federation Book Expo" is back, it promises to be bigger and better with a spread of about a million books on display. It is organized in a wide space this year on the topmost floor N of Hotel Grand Regency.

Williams, an ardent book lover visits the fair and wants to minimize the time it takes him to go from the N-th floor to ground floor. He can either take the elevator or the stairs.

The stairs are at an angle of 45 degrees and Williams's velocity is V1 m/s when taking the stairs down. The elevator on the other hand moves with a velocity V2 m/s. Whenever an elevator is called, it always starts from ground floor and goes to N-th floor where it collects Williams (collecting takes no time), it then makes its way down to the ground floor with Williams in it.

The elevator cross a total distance equal to N meters when going from N-th floor to ground floor or vice versa, while the length of the stairs is sqrt(2) * N because the stairs is at angle 45 degrees. Williams has requested your help to decide whether he should use stairs or the elevator to minimize his travel time. Can you help him out?

#### Input format :
First line of the input contains three space-separated integers N, V1, V2.

#### Output format :
Output a single line with string Elevator or Stairs, denoting the answer to the problem

**Sample test cases :** <br>
**Input 1 :** <br>
5 10 15<br>
**Output 1 :** <br>
Elevator

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,v1,v2;
    float t1,t2;
    cin>>n>>v1>>v2;
    t1=1.41421356237*n*100/v1;
    t2=2*n*100;
    t2=t2/v2;
    t1<t2?cout<<"Stairs":cout<<"Elevator";
    return 0;
}

```
