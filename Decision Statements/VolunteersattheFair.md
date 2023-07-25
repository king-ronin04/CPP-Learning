# Volunteers at the Fair
Wisconsin State Fair is one of the largest midsummer celebrations in the Midwest Allis, showcasing the agriculture skills and prowess of the state. Amelia, the Event Coordinator of the event wanted to hire student volunteers to serve for the event, so as to promote it to an extensive audience.

Students from 2 colleges have come forward for the same and Amelia has to now select the volunteers. There were N students from the first college and M students from second college. Amelia wanted to have the minimum possible difference between the number of students from the first college and second college. To do so, she can select one student from first college or one student from second college by knowing the value of K which tells her how many more volunteers who are yet to be included, to make the difference the minimum possible.

Can you help her by finding the minimum possible difference she can achieve between the number of students from the first college and second college?
#### Input format :
The first and only line of input contains 3 space separated integers — N, M and K — denoting the number of students from first college, number of students from second college, and number of volunteers who are yet to be included for the event

#### Output format :
Output the minimum possible difference between the number of students from the first college and second college

**Sample test cases : <br>
Input 1 :** <br>
5 2 1<br>
**Output 1 :** <br>
2

----------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,m,k;
    cin>>n>>m>>k;
    if(n<m)
    n=n+k;
    else
    m=m+k;
    if(n>m)
    k=n-m;
    else
    k=m-n;
    cout<<k;
    return 0;
}




```
