# Best Programmer
Baldwin High School's Best Programmer Contest is organized today and the contest hones the students coding skills by making them solve different challenges. Based on the speed and accuracy with which the students finish the challenges, the Event coordinators will rank the participants and reward them.



The entry level challenge was just one problem which the students has to program for. The problem reads like:



A positive integer, n, is said to be perfect if the sum of its proper divisors equals the number itself. (Proper divisors include 1 but not the number itself.) If this sum is less than n, the number is deficient, and if the sum is greater than n, the number is abundant.



The Event coordinators wanted to prepare the answer key for all the problems given in the contest so as to evaluate the submissions of the participants.Write a program using the following method.

**Method Name:** int findType(int)

**Description :** This method return 1 if the given integer is a deficient number, return 0 if it is a perfect number and return -1 if it is a abundant number.

#### Input format :
The input consists of an integer that corresponds to the given number.



#### Output format :
Output should display if the given number is a perfect, abundant or deficient number.

**Sample test cases :<br>
Input 1 :<br>**
4<br>
**Output 1 :<br>**
4 is a deficient number

**Input 2 :<br>**
6<br>
**Output 2 :<br>**
6 is a perfect number

**Input 3 :<br>**
100<br>
**Output 3 :<br>**
100 is an abundant number


-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int findType(int a);

int main()
{
    int num;
    cin>>num;
    cout<<num;
    if(findType(num)==0)
    {
        cout<<" is a perfect number";

    }
    else if(findType(num)==1)
    {
        cout<<" is a deficient number";

    }
    else
    {
        cout<<" is an abundant number";

    }
    return 0;
}

int findType(int a)
{
    int i,j=0;
    for(i=1;i<=a/2;i++)
    {
        if(a%i==0){j=j+i;}
    }
    if(j==a)
    return 0;
    else if(j>a)
    return -1;
    else
    return 1;
}


```




