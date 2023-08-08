# Right Triangle of Dots

 

The much awaited event at the entertainment industry every year is the "Screen Awards". This year the event is going to be organized on December 25 to honour the Artists for their professional excellence in Cinema. The Organizers of the event, J&R Events, decided to design the logo of the Screen Awards as a digitalized image and display it on the LED panel boards for the show promotions all across the venue. The Event team wanted to border the logo with right triangles which will describe it better.

For this purpose, the Event development team are in the task to find if N dots can make a right triangle or not (all N dots must be used). Given N dots, we can make it look like a Right Triangle (45-45-90 triangle) exactly with N dots. Rearrange the given N dots, like this:

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/874fadd2-901c-4627-817f-1c143a42cc48)


Your task is to help the team.In the Main method, obtain input from the user in the console and display "Yes" if you can make a right triangle using N dots, otherwise "No" by calling the find method





#### Input format :
First line of the input consists of an integer N

#### Output format :
Output "Yes" (without quotes) if you can make a right triangle using N dots, otherwise "No"(without quotes).

**Sample test cases :<br>
Input 1 :<br>**
6<br>
**Output 1 :<br>**
Yes



-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int find(int n);

int main()
{
    int n;
    cin>>n;
    if(find(n)==1){cout<<"Yes";}
    else{cout<<"No";}
    return 0;
}

int find(int n)
{
    int i,j=1;
    for(i=1;i<n;i++)
    {
        if((i*(i+1)/2)==n){break;}
        if((i*(i+1)/2)>n){j=0;break;}
    }
    return j;
}
```












