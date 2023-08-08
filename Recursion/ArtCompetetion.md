# Art Competition

 

Ocean Awareness Art Competition is a yearly art competition that engages students to promote the need to preserve, protect, and restore the world’s oceans and aquatic resources. The Contest was organized at an outdoor auditorium in the City and large mass of school kids is expected to participate.

 

Every student participating in the contest will be registered at the venue entrance and be provided with an enrollment Id. To ensure the safety of the students, the Event organizers decided to make a disciplined seating arrangement by sticking the students’ enrollment Id on the chairs. There were N enrollments approximately expected for the contest and based on this, the event organizers wanted to print the enrollment numbers in white sheets to stick to the chairs.

 

You are to help the organizers in taking the printed formats of the enrollment numbers. Write a recursive method to print the enrollment numbers from 1 to N without the help of Loops.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/3572fc42-d872-4f11-8e65-c7bb0680cfb3)


In the Main function, obtain input from the user in the console and call the printNumbers method 


#### Input format :
First line of the input is an integer N.

#### Output format :
Output the enrollment numbers from 1 to N without using loops.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
**Output 1 :<br>**
1 2 3 4 5 


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
void printnumbers(int n)
{
    static int i=1;
    if(i<=n)
    {
        cout<<i<<" ";
        i++;
        printnumbers(n);
    }
}

int main()
{
    int n;
    cin>>n;
    printnumbers(n);
    return 0;
}
```




