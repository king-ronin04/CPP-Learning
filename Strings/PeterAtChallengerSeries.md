# Peter at Challenger Series

The Table tennis Challenger Series is the springboard to fame for the future stars of professional table tennis. Peter is very passionate towards table tennis and made his debut in the first league match of the Series against a prominent player Horejsi.

 

Peter found some statistics of matches which described who won the points in order. A game shall be won by the player first scoring 11 points except in the case when both players have 10 points each, then the game shall be won by the first player subsequently gaining a lead of 2 points. Could you please help Peter find out who the winner was from the given statistics? (It is guaranteed that statistics represent always a valid, finished match.)



#### Input format :
First and only line of the input consists of a binary string S, which describes a match. '0' means Peter lose a point, whereas '1' means he won the point.

#### Output format :
Output on a separate line a string describing who won the match. If Peter won then print "Win" (without quotes), otherwise print "Lose" (without quotes).

**Sample test cases :<br>
Input 1 :<br>**
0101111111111<br>
**Output 1 :<br>**
Win


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;

int main(){
    string str;
    int one=0;
    getline(cin,str);
    int len=str.length();
    for(int i=0;i<len;i++){
        if(str[i]==49){
            one++;
        }
    }
    if(one>=(len-one)){
        cout<<"Win";
    }
    else{
        cout<<"Lose";
    }
    return 0;
}


```
