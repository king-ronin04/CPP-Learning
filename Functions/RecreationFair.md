# Recreation Fair
The Warners Club arranged for a Recreation Fair for kids and adults for the winter season ahead. The Club offered outdoor activities for adults like hiking, cycling, power soccer and indoor activities like chess, carom and card games for kids below 10 years. Gary and Dory accompanied their parents for the fair and wanted to play the cricket collectable card game as they are crazy about the collectable cards.

In their spare time, they usually have a way of playing some game involving such cards. Both also have the habit of exchanging the repeated cards with their friends. That day at the Fair, Gary and Dory thought about a different game. With the cards in hand, each person tried to make an exchange with the other person following this simple rule: each person must count how many cards he owned. After this, they had to split these cards into stacks, all of it with the same size, as large as it was possible for both players. Then, each one chooses one of the friend's card stacks to receive.

For example, if Gary and Dory would change the cards with respectively 8 and 12 cards each, both must put his cards in stacks of four cards (Gary would have two stacks and Dory had three stacks), and both choose a stack from his friend to receive it.

Help Gary and Dory find the maximum size of the stack of cards which can be exchanged between the two players.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/557c5d23-a154-46e9-bcdf-f49501d2758a)


In the Main function, obtain input from the user in the console and display the maximum size of the stack of cards which can be exchanged between the two players by calling the findValue method 



#### Input format :
The first line of the input contain an integer F1 (1 ≤ F1 ≤ 1000), which corresponds to the amount of collectable cards that Gary have to change.
<br>
The second line of the input contain an integer F2 (1 ≤ F2 ≤ 1000), which corresponds to the amount of collectable cards that Dory have to change.

#### Output format :
Output the maximum size of the stack of cards which can be exchanged between the two players, in a single line.

**Sample test cases :<br>
Input 1 :<br>**
8<br>
12<br>
**Output 1 :<br>**
4


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int findValue(int n1,int n2);

int main()
{
    int num1,num2;
    cin>>num1>>num2;
    cout<<findValue(num1,num2);
    return 0;
}

int findValue(int n1,int n2)
{
    int i,j=1;
    for(i=2;i<=n1;i++)
    {
        if((n1%i==0)&&(n2%i==0)){j=j*i;n1=n1/i;n2=n2/i;i=1;}
    }
    return j;
}
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int findValue(int a,int b){
    if(b==0)
        return a;
    else
    return findValue(b,a%b);
}

int main(){
    int a,b;
    cin>>a>>b;
    
    cout<<findValue(a,b);
}
```

