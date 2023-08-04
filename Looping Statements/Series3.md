# Series 3
The Event Organizing Company "Buzzcraft" focuses event management in a way that creates a win-win situation for all involved stakeholders. Buzzcraft don't look at building one time associations with clients, instead, aim at creating long-lasting collaborations that will span years to come. This goal of the company has helped them evolve and expand big with organizing many events till date.

The number of events that the company organizes every month is recorded sensibly and is seemed to have followed a specific series like: 30, 35, 38, 41, 54, 53 ...

Write a program which takes an integer N as the input and will output the series till the Nth term.

#### Input format :
First line of the input is an integer N.

#### Output format :
Output a single line the series till Nth term, each separated by a comma.

**Sample test cases :<br>
Input 1 :** <br>
5 <br>
**Output 1 :** <br>
30 35 38 41 54 

**Input 2 :<br>**
10<br>
**Output 2 :<br>**
30 35 38 41 54 53 78 71 110 95 


-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j=0,k=0,r=30,s=35;
    cin>>n;
    for(i=0;i<n;i++)
    {
        if(i%2==0){r=r+j;cout<<r<<" ";j=j+8;}
        else{s=s+k;cout<<s<<" ";k=k+6;}
    }
    return 0;
}


```
