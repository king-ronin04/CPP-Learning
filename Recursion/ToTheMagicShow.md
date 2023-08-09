# To the Magic Show

 

The Magic Castle, the home of the Academy of Magical Arts has organized the great 'WonderWorks Magic Show'. Renowned magicians were invited to mystify and thrill the crowd with their world’s spectacular magic tricks. Rahul has promised to take his little kids Akash and Anusha to this renownedshow.

 

Unfortunately Rahul got a bit late to return from work, but he did not want to disappoint the kids.So he started off with themto the show in his car.He thought to take a short route to reach the show on time but he was not sure if it is possible to reach the magic show venue at the point (x2, y2) from his house which is at a point (x1, y1).

 

Given coordinates of a source point (x1, y1), write a recursive method to determine if it is possible to reach the destination point (x2, y2).

 

Note: From any point (x, y) there only two types of valid movements: (x, x + y) and (x + y, y).

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/ef887300-f936-46d4-bb25-46b85a89ddfe)


In the Main function, obtain input from the user in the console and display "True" if the given source point will reach the destination point, else display "False" by calling the isReachable method 

#### Input format :
First line of the input contains the source point (x1, y1).
<br>
Second line of the input contains the source point (x2, y2).

#### Output format :
Output "True" (without quotes) if the given source point will reach the destination point. Print "False" (without quotes) otherwise.

**Sample test cases :<br>
Input 1 :<br>**
2 10<br>
26 12<br>
**Output 1 :<br>**
True


-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include<iostream>
using namespace std;
int isReachable(int x1,int y1,int x2,int y2)
{
    int x,y;
    if((x1>x2)||(y1>y2))
    {
        return 0;
    }
    else if((x1==x2)&&(y1==y2))
    {
        return 1;
    }
    else if((x1<=x2)&&(y1<=y2))
    {
        x= isReachable(x1,y1+x1,x2,y2);
        y= isReachable(x1+y1,y1,x2,y2);
    }
    if((x==1)||(y==1))
    {
    return 1;}
    return 0;
}
int main()
{
    int x1,x2,y1,y2,i=0;
    cin>>x1>>y1;
    cin>>x2>>y2;
    i=isReachable(x1,y1,x2,y2);
    (i==1)?cout<<"True":cout<<"False";
    return 0;
}

```
