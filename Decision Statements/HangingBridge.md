# Hanging Bridge
At the annual "KrackerJack Karnival", there was a newest attraction ever in the City, the "Hanging Bridge". Visitors will be able to walk 200ft on the bridge, hanging around 50ft above the ground, and enjoy a wide-angle view of the breathtaking greenery.

The Hanging Bridge was inaugurated successfully in co-ordination with the Event Manager Rahul. There is a limit on the maximum number of people on the bridge and Rahul has to now ensure the count of people on the bridge currently should not exceed the limit. He then approximately estimated that C adults and D kids who came to the show, were on the hanging bridge. He also noticed that there are L legs of the people touching the bridge.

Rahul knows that kids love to ride on the adults and they might ride on the adults, and their legs won't touch the ground and hence he would miss counting their legs. Also Rahul knew that the adults would be strong enough to ride at max two kids on their back.

Rahul is now wondering whether he counted the legs properly or not. Specifically, he is wondering is there some possibility of his counting being correct. Please help Rahul in finding it.
#### Input format :
The only line of input contains three space separated integers C, D, L denoting number of the adults, number of the kids and number of legs of people counted by Rahul, respectively

#### Output format :
Output a single line containing a string "yes" or "no" (both without quotes) according to the situation

**Sample test cases : <br>
Input 1 :** <br>
1 1 4<br>
**Output 1 :** <br>
yes



----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int a,b,c;
    cin>>a>>b>>c;
    a=(a+b)*2;
    (a==c)?cout<<"yes":cout<<"no";
    return 0;
}

```
