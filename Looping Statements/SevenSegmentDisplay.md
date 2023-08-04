# Seven Segment Display
The Event Organizing Company "Buzzcraft" wanted to procure seven segment displays to display any numeric information display boards, scrolling ad banners, etc., to place it in their Events. The Company contracted out their order to MDC team at Orange labs who designs embedded sensing nodes and provides connectivity to tie them to the internet of things.

They are working on building seven segment displays. But the Company wanted to know how many seven segment displays will they need to represent an Integer x. They use one seven segment display to represent one digit of an Integer. For example: Integer "100" needs "3" seven segment boards to be represented.

Help them find out how many displays are needed?



#### Input format :
First and only line consists of one positive integer that needs to be represented using seven segment displays.

#### Output format :
Output a single line containing the number of digits of that integer.

**Sample test cases :<br>
Input 1 :<br>**
1<br>
**Output 1 :<br>**
1


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,d=0;
    cin>>n;
    if(n==0){d=1;}
    while(n!=0)
    {
        n=n/10;
        d=d+1;
    }
    cout<<d;
    return 0;
}
```
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
#include<math.h>
using namespace std;

int main(){
    int n;
    cin>>n;
    int count;
    count =(int) log10(n);
    cout<<count+1;
    return 0; 
}

```
