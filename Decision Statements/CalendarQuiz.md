# Calendar Quiz
Super Quiz Bee is a famous quiz Competition that tests students on a wide variety of academic subjects. This week’s participants were kids of age 12 to 15 and the quiz questions were based on Gregorian calendar.

In the first round of the competition, the Host of the event told the participants that it was Monday on the date 01/01/2001. Later he questioned each one of the participant what would be the day on the 1st January, giving them a particular year. Write a program to help the Host validate the answers given by the participants.
#### Input format :
The first line contains an integer that corresponds to a year

#### Output format :
Output the day on the 1st January of that given year.

**Sample test cases : <br>
Input 1 :** <br>
2001<br>
**Output 1 :**<br>
Monday

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int main()
{
    int year,d,c,f=0;
    cin>>year;
    year=year-1;
    d=year%100;
    c=year/100;
    f=d/4;
    f=f+d;
    f=f+(c/4);
    f=f-(2*c);
    f=f+29;
    f=f%7;
    if(f<0)
    {
        f=f+7;
    }
    switch(f)
    {
        case 0:cout<<"Sunday";break;
        case 1:cout<<"Monday";break;
        case 2:cout<<"Tueday";break;
        case 3:cout<<"Wednesday";break;
        case 4:cout<<"Thursday";break;
        case 5:cout<<"Friday";break;
        case 6:cout<<"Saturday";break;
    }
    return 0;
}


```
