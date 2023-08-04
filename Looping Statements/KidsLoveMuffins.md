# Kids Love Muffins
Louis was celebrating his 10th Birthday and his parents have promised to make the best party ever for him. He will be very happy if he can invite all his friends to this party (he has many friends), but unfortunately his parents can't invite everyone because they have a limited number of muffins, and they want everyone to be happy.

As we all know, kids love to eat a lot of muffins of the same type, let's say a kid will be happy only if he can eat at least K muffins of the same type.

Given K, and the number of available muffins of each type, calculate the maximum number of kids where Louis’s parents can make all of them happy by giving each one at least K muffins of the same type.

#### Input format :
The first line of the input contains two space-separated integers N, the number of different muffins (1 ≤ N ≤ 100), and K, the minimum number of muffins which will make a kid happy as described above (1 ≤ K ≤ 100).
<br>
The second line of input contains N integers, separated by a single space, which are the available number of muffins of each type. There will be at least 1 muffin and at most 100 muffins of each type.

#### Output format :
Output on a single line one integer, the maximum number of kids Louis’ parents can make happy by giving each one at least K muffins of the same type.

**Sample test cases :<br>
Input 1 :<br>**
3 2 <br>
4 5 7<br>
**Output 1 :<br>**
7


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;

int main(){
    int n,k;
    cin>>n>>k;
    int muffins[n];
    for(int i=0;i<n;i++)
        cin>>muffins[i];
    int maxKids=0;
    for(int i=0;i<n;i++){
        int kids=muffins[i]/k;
        maxKids+=kids;
    }
    cout<<maxKids;
    return 0;
}
```
