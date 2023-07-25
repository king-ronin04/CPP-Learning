# Carrom
If Cricket is the most popular outdoor game in India, Carrom is not too behind as one of most played indoor games.

Let's now make use of our knowlege in operators & conditional statements to compute the points scored at the end of a round in Carrom Game.

Carrom is a board game where two participants (teams) play. It consists of 9 white coins, 9 black coins and a red coin. The first team that finishes all their coins wins (given that red has been pocketed by one of the teams). The points are awarded based on the number of left-over coins of the opposition (loser) in the board. If the winning team has pocketed the red, they get an additional 5 points. Write a program to compute the score of winner at the end of a round.

If the number of coins left on the board is either less than 1 or greater than 9 display "Invalid Input".

#### Input format :
Input consists of a single integer which corresponds to number of coins left on board and a character which corresponds to whether the winning team has pocketed red or not. 

#### Output format :
Output corresponds to the total points won.
<br>
Print Invalid Input in case the no of coins is less than one or greater than nine.

**Sample test cases :** <br>
**Input 1 :** <br>
5<br>
y<br>
**Output 1 :** <br>
10<br>

**Input 2 :** <br>
2<br>
n<br>
**Output 2 :** <br>
2<br>

**Input 3 :** <br>
-1<br>
**Output 3 :** <br>
Invalid Input


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<cstring>
using namespace std;
int main()
{
		int number;
		char c;
		cin>>number;
		if(number < 1 || number>9) {
			cout<<"Invalid Input";
		}
		else {
		cin>>c;

			if(c=='y') {
				cout<<number+5;
			}
			else {
				cout<<number;
			}
		}
	}


```
