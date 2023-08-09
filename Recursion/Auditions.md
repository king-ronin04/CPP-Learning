# Auditions

 

"Singing Champs" is a famous reality series. The show organizers have planned to roll out the show’s 5th season in the coming month. The auditions for the show is announced at various Cities widely and the organizers have inaugurated the first audition today.

 

Large mass of people gathered at the venue. Based on the selection procedure for the first level, all the people are made to stand in a queue. Participants who are standing in the even positions of the queue are selected initially. Of the selected people a queue is formed and again out of these only people on even position are selected. This continues until we are left with one person.

 

To help them in the selection procedure, the organizers approached you to write a recursive method for determining the position of that final person in the original queue.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/0e6c2e12-8e28-43b5-a95d-0cc893a45212)


In the Main function, obtain input from the user in the console and display the position(original queue) of that person who is left by calling the findPos method 

#### Input format :
First and only line of the input is an integer N that corresponds to the total number of people who came for the auditions.

#### Output format :
Output the position(original queue) of that person who is left.



**Sample test cases :<br>
Input 1 :<br>**
5<br>
**Output 1 :<br>**
4


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int findPos(int pos)
{
    static int x=1;
    x=x*2;
    if(pos>x)
    {
        return findPos(pos);
    }
    if(pos==x){return x;}
    return x/2;
}
int main()
{
    int num;
    cin>>num;
    cout<<findPos(num);
    return 0;
}

```


