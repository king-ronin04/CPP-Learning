# Lucky Cards
The Hatfield Game Fair is the premier event of its kind for adults interested in some intellectual and cognitive brain games. Exciting games were organized for kids between age group of 8 and 10. One such game was the "Lucky Cards", a simple two-player game, played with a deck of cards. The cards in the deck have these possible names: two, three, four, five, six, seven, eight, nine, ten, jack, queen, king, ace. The cards labeled jack, queen, king, ace are collectively known as high cards.

The numerical equivalent of the high cards is as given below:
<br>
Jack – 11
<br>
Queen – 12
<br>
King – 13
<br>
Ace - 1
<br>
Please note here, though Ace has a numerical equivalent value as 1, it is always considered as the top rated card. So it is also included in the list of high cards.

The game organizer selects N cards and places it in the deck faced-down on the table. Player A turns over the top card and places it on a pile; then player B turns over the top card and places it on the same pile. A and B alternate turns until the N cards are exhausted. The game is scored as follows:
<br>
- if a player turns over an ace that is 1, with at least 4 cards remain to be turned over, and none of the next 4 cards is a high card, that player scores 4 points
- if a player turns over a king that is 13, with at least 3 cards remain to be turned over, and none of the next 3 cards is a high card, that player scores 3 points
- if a player turns over a queen that is 12, with at least 2 cards remain to be turned over, and none of the next 2 cards is a high card, that player scores 2 points
- if a player turns over a jack that is 11, with at least 1 card remains to be turned over, and the next card is not a high card, that player scores 1 point

Write a program to calculate the scores of the two players.



#### Input format :
The first line of the input contain an integer N, which corresponds to the number of cards in the deck.
<br>
Each of the following N lines will contain an integer that corresponds to the numerical value of the cards that the players turn over. The first line denotes the first card to be turned over; the next line the next card; and so on.

#### Output format :
Print the individual scores of the players whenever a player scores in separate new lines.
<br>
Print the total score for each player in the last two lines of the output at the end of the game

**Sample test cases :<br>
Input 1 :<br>**
15<br>
3<br>
2<br>
1<br>
5<br>
6<br>
4<br>
8<br>
11<br>
2<br>
3<br>
2<br>
13<br>
6<br>
10<br>
6<br>
**Output 1 :<br>**
Player A scores4point(s)<br>
Player B scores1point(s)<br>
Player B scores3point(s)<br>
Player A:4point(s)<br>
Player B:4point(s)


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j,c1=0,c2=0,c3=0,k;
    cin>>n;
    int a[n];
    for(i=0;i<n;i++)
    {
        cin>>a[i];
        if(a[i]==1){a[i]=14;}
    }
    for(i=0;i<n;i++)
    {
        k=a[i]%10;
        if((a[i]>10)&&(i+k<n))
        {
            for(j=1;j<=k;j++)
            {
                if(a[i+j]<11)
                {
                    c1++;
                }
            }
            if(c1==k)
            {
                if(i%2==0)
                {
                    cout<<"Player A scores"<<c1<<"point(s)\n";
                    c2=c2+k;
                }
                else
                {
                    cout<<"Player B scores"<<c1<<"point(s)\n";
                    c3=c3+k;
                }
            }
            c1=0;
        }
    }
    cout<<"Player A:"<<c2<<"point(s)\nPlayer B:"<<c3<<"point(s)";
    return 0;
}


```

