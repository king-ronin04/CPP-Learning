# Minimum and Maximum
The ExConFair is the region's largest trade fair on Construction Equipments & Technology. The Event organizers hired college students as volunteers to work at the fair as the event is targeted to be attended by approx. 30 million visitors.

At the Office in the fair, there are two guards who count how many times a volunteer enters into the fair ground. Though the duty of a guard is 24 hour in a day, but sometimes they fall asleep during their duty and could not track the entry of volunteers in the fair ground. But one better thing is that they never fall asleep at the same time. At least one of them remains awake and counts who enters into the office. Now the Event Head wants to calculate how many times a volunteer has entered into the fair ground. He asked to the guard and they give him two integers A and B, count of first guard and second guard respectively.

Help the Event Head to count the minimum and maximum number of times a volunteer could have entered into the fair ground.
#### Input format :
First line of the input consists of two integers that correspond respectively to A and B.

#### Code constraints :
Output a single line containing two space separated integers, the minimum and maximum number of times a volunteer could have entered into the fair ground

**Sample test cases : <br>
Input 1 :** <br>
30 40<br>
**Output 1 :** <br>
40 70

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
using namespace std;
int main()
{
    int num1,num2,sum=0;
    cin>>num1>>num2;
    if(num1>num2)
     {
    cout<<num1;
     }
   else
   {
       cout<<num2;
   }
   sum=num1+num2;
   cout<<" "<<sum;

    return 0;
}

```
