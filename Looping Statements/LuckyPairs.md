# Lucky Pairs
Richie and Riya are participating in a game called "Lucky pairs" at the Annual Game Fair in their Company. As per the rules of the contest, two members form a team and Richie initially has the number A and Riya has the number B.

There are a total of N turns in the game, and Richie and Riya alternatively take turns. In each turn the player whose turn it is, multiplies his or her number by 2. Richie has the first turn. Suppose after the entire N turns, Richie’s number has become C and Riya’s number has become D. The final score of the team will be the sum of the scores (C+D) of both the players after N turns.

Write a program to facilitate the quiz organizers to find the final scores of the teams

#### Input format :
The only line of input contains 3 integers A, B, and N.

#### Output format :
Output a single line which contains the integer that gives the final score of the team which will be the sum of the scores of both the players after N turns

**Sample test cases :<br>
Input 1 :<br>**
1 2 1<br>
**Output 1 :<br>**
4


----------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int main()
{
    int a,b,n;
    cin>>a>>b>>n;
    for(a=a;n>0;n--)
    {
        a=a*2;
        n--;
        if(n>0){b=b*2;}
    }
    cout<<a+b;
    return 0;
}



```
