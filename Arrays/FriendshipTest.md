# Friendship Test

Michael is celebrating his 10th birthday and he wished to arrange a party to all his class mates. But there are n tough guys amongst his class who are weird. They thought that this is the best occasion for testing their friendship with him. They put up conditions before Michael that they will break the friendship unless he gives them a grand party on their chosen day. Formally, ith friend will break his friendship if he does not receive a grand party on dith day.

Michael is not a lavish spender and can give at most one grand party daily. Also, he wants to invite only one person in a party. So he just wonders what the maximum number of friendships he can save.

Please help Michael in this difficult task.

#### Input format :
First line will contain a single integer denoting n. Assume that the maximum value for n as 50.
<br>
Second line will contain n space separated integers where ith integer corresponds to the day dith as given in the problem.

#### Output format :
Print a single line corresponding to the maximum number of friendships Michael can save.

**Sample test cases :<br>
Input 1 :<br>**
2<br>
3 2<br>
**Output 1 :<br>**
2

**Input 2 :<br>**
5<br>
4 1 3 7 5<br>
**Output 2 :<br>**
5

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j=0,k;
    cin>>n;
    int a[n];
    for(i=0;i<n;i++)
    {
        cin>>a[i];
    }
    for(i=0;i<n;i++)
    {
        if(a[i]>0){j++;
        for(k=i+1;k<n;k++)
        {
            if(a[i]==a[k]){a[k]=0;}
        }
        }
    }
    cout<<j;
    return 0;
}

```
