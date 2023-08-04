# Series 1

The Event Organizing Company "Buzzcraft" focuses event management in a way that creates a win-win situation for all involved stakeholders. Buzzcraft don't look at building one time associations with clients, instead, aim at creating long-lasting collaborations that will span years to come. This goal of the company has helped them evolve and gain more clients within notable time.
The number of clients of the company from the start day of their journey till now is recorded sensibly and is seemed to have followed a specific series like: 2,3,5,7,11,13,17,19, 23 ... 

Write a program which takes an integer N as the input and will output the series till the Nth term.

#### Input format :
First line of the input is an integer N.

#### Output format :
Output a single line the series till Nth term, each separated by a comma.

**Sample test cases :<br>
Input 1 :** <br>
5<br>
**Output 1 :**  <br>
2 3 5 7 11 <br>

**Input 2 :** <br>
10 <br>
**Output 2 :** <br>
2 3 5 7 11 13 17 19 23 29

------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j,k=2,s=0;
    cin>>n;
    for(i=0;i<n;i++)
    {
        for(j=2;j<=k/2;j++)
        {
            if(k%j==0){s=1;break;}
        }
        if(s==0){cout<<k<<" ";}
        else{i--;}
        k++;s=0;
    }
    return 0;
}

```
