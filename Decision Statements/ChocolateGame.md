# Chocolate Game
 It was Christmas Eve and the celebrations remembering the birth of Jesus were going on in full swing at the Catheral Chapel. The Event Management Team had arranged for some exciting games after the mass worship and feast, where adults and kids of all ages participated very actively. "Chocolate Game" was organized for the kids which involved a standard chocolate of n by m pieces. More formally, chocolate is a rectangular plate consisting of n rows and m columns.

Two kids at a moment will play with the chocolate. First kid takes the chocolate and cuts it into two parts by making either a horizontal or vertical cut. Then, the second kid takes one of the available pieces and divides into two parts by either making a horizontal or vertical cut. Then the turn of first kid comes and he can pick any block of the available chocolates and do the same thing again. The player who cannot make a turn loses.

Write a program to find which of the kids will win if both of them play optimally. Output "Yes", if the kid who plays first will win, otherwise print "No".
#### Input format :
The only line of the input contains two space separated integers n and m - the sizes of the chocolate

#### Output format :
Output a single line containing one word "Yes" (without quotes) if there is a sequence of moves leading to the winning of the person who moves first and "No" (without quotes) otherwise

**Sample test cases : <br>
Input 1 :** <br>
1 2<br>
**Output 1 :** <br>
Yes

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,m,count=0;
    cin>>n>>m;
    while(1)
    {
    if(m%2==0)
    {
        count++;
        m=m/2;

    }
    else if(n%2==0)
    {
        count++;
        n=n/2;

    }
    else
    break;
    }
    if(count%2==0)
    cout<<"No";
    else
    cout<<"Yes";
    return 0;
}


```
