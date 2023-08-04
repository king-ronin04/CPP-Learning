# Youngest and Oldest

The Pan Am 73 flight from Bombay to New York en route Karachi and Frankfurt was hijacked by a few Palestinian terrorists at the Karachi International Airport.

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/f9ac119a-636c-4ee7-830a-c17c1902005c)

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/65db1081-421a-49cb-a64d-419ab6e257c6)

The senior flight purser Neerja Banhot had to wither her fear and start evacuating the passengers on board. She pleaded the hijackers to release the oldest and the youngest person in the aircraft. Heeding to her plea the chief of the hijacker agreed to let go the oldest and the youngest. Given the ages of the passengers find the oldest and the youngest.

#### Input format :
The first line of input consists of an integer n, corresponding to the number of passengers in the aircraft.
<br>
The next line consists of the age of passengers separated by a space.

#### Output format :
The output prints the youngest and oldest separated by a space.
<br>
Print Invalid Input if n or any one of the ages is negative.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
1 2 3 9 4<br>
**Output 1 :<br>**
1 9

**Input 2 :<br>**
-6<br>
**Output 2 :<br>**
Invalid Input

**Input 3 :<br>**
6<br>
68 -45<br>
**Output 3 :<br>**
Invalid Input

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int i,n,sum=0,count=0,min=0,max=0;
		cin>>n;
		if(n<0) {
			cout<<"Invalid Input";
		}
		else {
			int a[n];
			for(i=0;i<n;i++) {
				cin>>a[i];
				if(a[i] <0) {
					cout<<"Invalid Input";
					break;
				}
			}
			min = a[0];
			for(i=1;i<n;i++) {
				if(a[i] >0) {
				count++;
				if(a[i] < min) {
					min = a[i];
				}
				}
			}
			max = a[0];
			for(i=1;i<n;i++) {
				if(a[i] > max) {
					max = a[i];
				}
			}
		}
		if(count+1 == n) {
		cout<<min<<" "<<max;
		}
	}
```
