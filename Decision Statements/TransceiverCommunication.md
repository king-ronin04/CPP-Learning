# Transceiver Communication
The ExCon Fair is the region's largest trade fair on Construction Equipments & Technology. The Event is targeted to be attended by approx. 30 million visitors. To ensure the smooth functioning of the event and the safety of the visitors, the Event Coordinator, Security Chief and Crowd Control Chief were instructed to carry two-way transceivers so they can stay in constant contact. Of course, these transceivers have a limited range so if two are too far apart, they cannot communicate directly.

The Event Coordinator invested in top-of-the-line transceivers which have a few advanced features. One is that even if two people cannot talk directly because they are out of range, if there is another transceiver that is close enough to both, then the two transceivers can still communicate with each other using the third transceiver as an intermediate device.

There has been a minor emergency at the Event and the Event Coordinator needs to communicate with both the Security Chief and Crowd Control Chief right away. Help the Event Coordinator determine if it is possible for all three people to communicate with each other, even if two must communicate through the third because they are too far apart.
#### Input format :
The first line of the input contains a positive integer R ≤ 1,000 indicating that two transceivers can communicate directly without an intermediate transceiver if they are at most R meters away from each other.
<br>
The remaining three lines of the input describe the current locations of the the Event Coordinator, Security Chief and Crowd Control Chief, respectively. Each such line contains two integers X,Y (at most 10,000 in absolute value) indicating that the respective person is located at position X,Y.
#### Output format :
Output a single line containing a single string. If it is possible for all three to communicate then you should output "Yes". Otherwise, you should output "No".
<br>
To be clear, we say that two transceivers are close enough to communicate directly if the length of the straight line connecting their X,Y coordinates is at most R.

**Sample test cases :** <br>
**Input 1 :** <br>
1<br>
0 1 <br>
0 0 <br>
1 0<br>
**Output 1 :** <br>
Yes


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include <cmath>
using namespace std;
int main()
{
    int a,b,c,d,e,f,g;
    int sq=0,count=0;
    float d1,d2,d3;
    cin>>a;
    cin>>b>>c;
    cin>>d>>e;
    cin>>f>>g;
    sq=((b-d)*(b-d))+((c-e)*(c-e));
    d1=sqrt(sq);
    sq=((f-d)*(f-d))+((g-e)*(g-e));
    d2=sqrt(sq);
    sq=((b-f)*(b-f))+((c-g)*(c-g));
    d3=sqrt(sq);
    if(d1>a){count++;}
    if(d2>a){count++;}
    if(d3>a){count++;}
    if(count>1){cout<<"No";}
    else
    cout<<"Yes";
    return 0;
}

```
