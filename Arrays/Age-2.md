# Age - 2

The Pan Am 73 flight from Bombay to New York en route Karachi and Frankfurt was hijacked by a few Palestinian terrorists at the Karachi International Airport. The senior flight purser Neerja Banhot withered her fear and helped evacuating the passengers on board.

Neerja planned to evacuated the passengers in rows that have an average age greater than x. Given r the number of rows, c the number of columns, a list of integers representing the ages of passengers, can you find the number of rows with an average age greater than x?

#### Input format :
The first line of input consists of an integer r, corresponding to the number of rows of seats in the aircraft.
<br>
The second line of input consists of an integer c, corresponding to the number of seats in a row.
<br>
The next r lines of input consist of c integers that correspond to the ages of passengers.
<br>
The next line of input is an integer x corresponding to the cut-off age.

#### Output format :
The output consists of an integer corresponding to t the number of rows with an average age greater than x.

**Sample test cases :<br>
Input 1 :<br>**
4<br>
5<br>
23 34 45 56 67<br>
98 78 65 78 90<br>
85 76 98 1 2<br>
5 6 7 8 9<br>
25<br>
**Output 1 :<br>**
3


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int r,c,i,j,age,sum=0,count=0,avg=0;
		cin>>r;
		cin>>c;
		int a[r][c];
		for(i=0;i<r;i++) {
			for(j=0;j<c;j++) {
				cin>>a[i][j];
			}
		}
		cin>>age;
		for(i=0;i<r;i++) {
			for(j=0;j<c;j++) {
				sum += a[i][j];
			}
			avg = sum/c;
			if(avg > age) {
				count++;
			}
			sum =0;
			avg =0;
		}
		cout<<count;
	}

```
