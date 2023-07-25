# Triangle Game 

The Westland Game Fair is the premier event of its kind for kids interested in some intellectual and cognitive brain games. Exciting games were organized for kids between age group of 8 and 10. One such game was called the "Triangle game", where different number boards in the range 1 to 180 are available. Each kid needs to select three number boards, where the numbers on the boards correspond to the angles of a triangle. 

If the angles selected by a kid forms a triangle, he/she would receive Prize 1. If the angles selected by a kid forms a right triangle, he/she would receive Prize 2. If the angles selected by the kids form an equilateral triangle, he/she would receive Prize 3. If the angles selected by a kid do not form even a triangle, then he/she will not receive any prizes. Write a program for the organizers to fetch the result based on the number boards selected by the kids.

#### Input format :
There are 3 lines in the input, each of which corresponds to the numbers on the boards that the kids select.

#### Output format :
Output should display "Prize 1" or "Prize 2" or "Prize 3" or "No Prize" based on the conditions given.

**Sample test cases : <br>
Input 1 :** <br>
60<br>
50<br>
70<br>
**Output 1 :** <br>
Prize 1

**Input 2 :** <br>
60<br>
60<br>
70<br>
**Output 2 :** <br>
No prize

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
using namespace std;
int main()
{
    int angle1,angle2,angle3;
    cin>>angle1>>angle2>>angle3;
    if((angle1+angle2+angle3) == 180)
  {
        
    if(angle1==angle2 && angle2==angle3 && angle1==angle3)
    {
        cout<<"Prize 3";
    }
    else if(angle1==90 || angle2==90 || angle3==90)
    {
        cout<<"Prize 2";
    }
    else 
    {
        cout<<"Prize 1";
    }
 }
    else {
			cout<<"No Prize";
		}
    return 0;
}


```
