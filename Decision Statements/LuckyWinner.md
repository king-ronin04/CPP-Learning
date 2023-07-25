# Lucky Winner
It was the inaugural ceremony of "Fantasy Kingdom" Amusement park and the park Management has announced some lucky prizes for the visitors on the first day. Based on this, the visitors whose ticket number has the last digit as 3 or 8, are declared as lucky winners and attracting prizes are awaiting to be presented for them.

Write a program to find if the last digit of the ticket number of visitors is 3 or 8.
#### Input format :
First line of the input is an integer that corresponds to the ticket number.

#### Output format :
Output should display as "Lucky Winner" if the last digit of the ticket number is 3 or 8. Otherwise print "Not a Lucky Winner".

**Sample test cases :<br>
Input 1 :** <br>
43<br>
**Output 1 :** <br>
Lucky Winner


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
using namespace std;
int main()
{
    int number;
    cin>>number;
    if(number%10==3 || number%10==8)
    {
        cout<<"Lucky Winner";
    }
    else
    {
        cout<<"Not a Lucky Winner";
    }
    return 0;
}

```
