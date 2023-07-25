# Card Game
The Westland Game Fair is the premier event of its kind for kids interested in some intellectual and cognitive brain games. Alan, a middle school boy is visiting the fair where he is very much drawn by the Card game.

The game’s rules are:<br>
A player needs to pick 3 cards from a big lot of cards. There are 4 types of Cards namely Spade(S), Heart(H), Club(C) and Diamond (D). If all the 3 cards that the player picks are of the same type and same number, they get a Double Bonanza. If all the 3 cards are of the same type or if they all have the same number, they get a Bonanza. Otherwise they do not get a Bonanza. Alan has now picked 3 cards and is awaiting to know if he has got a bonanza. Please help him to know if he has won the Bonanza or not.
#### Input format :
There are 3 lines of input.
<br>
Each of the line consists of character and integer input, which corresponds to the type of the card and the number in it that Alan picked. The type of card and the number are separated by a single spa
#### Output format :
Output should display "Double Bonanza" or "Bonanza" or "No Bonanza" based on the conditions given.

**Sample test cases : <br>
Input 1 :** <br>
S 5 <br>
S 5 <br>
S 5 <br>
**Output 1 :** <br>
Double Bonanza


---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int a,b,c;
    char x,y,z;
    cin>>x;
    cin>>a;
    cin>>y;
    cin>>b;
    cin>>z;
    cin>>c;
    if(((x==y)&&(y==z))&&((a==b)&&(a==c)))
    {
        cout<<"Double Bonanza";
    }
    else if(((x==y)&&(x==z))||((a==b)&&(a==c)))
    {
       cout<<"Bonanza";
    }
    else
    {
        cout<<"No Bonanza";
    }
    return 0;
}


```
