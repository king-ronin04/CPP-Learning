# Help Lost Child
Harry, a little boy was accompanied by his Dad to visit the "Aquatica Carnival". The event saw a large crowd and the Security Chiefs found it hard to control them. Very regretfully, Harry got lost and was seen extremely worried. He wanted to reach back home as soon as possible. He was standing currently at coordinates (x1, y1) in 2-D plane. His home is at coordinates (x2, y2).

Please help him by giving a command by telling the direction in which he should go, so as to reach his home. If you give him a direction, he will keep moving in that direction till he reaches home. There are four possible directions you can give as command - "left", "right", "up", "down". It might be possible that you can't instruct Harry in such a way that he reaches his home. In that case, display the output as "sad".
#### Input format :
First line of the input contains four space separated integers x1, y1, x2, y2.

#### Output format :
Output a single line containing "left" or "right" or "up" or "down" or "sad" (without quotes).

**Sample test cases :<br>
Input 1 :** <br>
0 0 1 0<br>
**Output 1 :** <br>
right


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int x1,y1,x2,y2;
    cin>>x1>>y1>>x2>>y2;
    if(y1==y2)
    {
        if(x1>x2)
        {
            cout<<"left";
        }
        else if(x2>x1)
        {
            cout<<"right";
        }
    }
    else if(x1==x2)
    {
        if(y1>y2)
        {
            cout<<"down";
        }
        else if(y2>y1)
        {
        cout<<"up";
        }
    }
    else
    {
    cout<<"sad";
    }
    return 0;
}

```
