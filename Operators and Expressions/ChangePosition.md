# Change Position

The room that Patrick and Johnny were staying was very big. They felt lazy to walk inside the room from the bed's location to another location. So they wanted to change the position of the bed. The shape of the room is a Square. They decided to place the bed at the exact center of the room so that their walking distance would be minimised. Can you please help them in placing the bed at the exact centre?

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/cf4f30ae-b5ef-4455-9d62-4d80a2ef088f)

Given the coordinates of the left bottom vertex of the square room and the length of the side, you need to write a program to determine the coordinates of the centre of the room.

### [Assumption --- Length of the side is always even]

**Input format :** <br>
Input consists of 3 integers. The first integer corresponds to the x-coordinate of the left bottom vertex. The second integer corresponds to the y-coordinate of the left bottom vertex. The third integer corresponds to the length of the square.

**Output format :** <br>
The output prints the x and y coordinates of the center separated by a space.

**Sample test cases :** <br>
**Input 1 :** <br>
10<br>
30<br>
16<br>
**Output 1 :** <br>
18.00 38.00


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<iomanip>
using namespace std;
int main()
{
		int x,y,length;
		double cx,cy;
		cin>>x;
		cin>>y;
		cin>>length;
		cx = x+(double)(length/(double)2.0);
		cy = y+(double)(length/(double)2.0);
		cout<<fixed<<setprecision(2)<<cx<<" "<<cy;
}


```
