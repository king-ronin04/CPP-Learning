# Mid Aged

The Pan Am 73 flight from Bombay to New York en route Karachi and Frankfurt was hijacked by a few Palestinian terrorists at the Karachi International Airport. The senior flight purser Neerja Banhot withered her fear and helped evacuating the passengers on board.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/bcbce319-3d18-4604-bb83-9c7d7273819c)


Neerja very well knew that she would not be able to evacuate all passengers dodging the hijackers. So she wanted to hand over the responsibility of evacuating in the senior citizens(above 60 years of age) and children(below 18 years of age) in the flight to the mid-aged passengers seated in the diagonals

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/7ed71c0e-456a-4648-930f-82746a1ac45f)


Given n the number of rows of seats and the number of seats in a row and the ages of passengers in each seat can you find the number of mid-aged passengers seated in the diagonals.



#### Input format :
The first line input consists of an integer n, corresponding to the number of rows of seats and the number of seats in the aircraft.
<br>
The next n lines of input consist of n integers that correspond to the ages of passengers

#### Output format :
The output consists of an integer corresponding to the number of mid-aged passengers seated in the diagonals.

**Sample test cases :<br>
Input 1 :<br>**
3 <br>
25 17 20<br>
33 26 30<br>
4 7 3<br>
**Output 1 :<br>**
2


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int r,c,i,j,age,count=0;
	cin>>r;
	int a[r][r];
	for(i=0;i<r;i++)
	{
		for(j=0;j<r;j++)
		{
			cin>>a[i][j];
		}
	}
	for(i=0;i<r;i++)
	{
		for(j=0;j<r;j++)
		{
		    if(i==j)
		    {
		        if(a[i][j]>=18 && a[i][j]<=60)
		        {
		            count++;
		        }
		    }
		}
	}
	cout<<count;
}


```
