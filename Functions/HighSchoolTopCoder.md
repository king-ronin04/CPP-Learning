# High School TopCoder

 

Green Wood High School is set to premier a programming tournament for high school-aged math and science students across the country. Based on this contest, the school has called in for all the interested candidates to take up a qualifying test at the school premises.

 

Before the qualifier, the Event coordinators chose the problem sets and wanted to code it beforehand to ease the evaluation procedure. They wanted your help to code few of the problem sets, one of which was involving Fibonacci series. We all know the Fibonacci sequence, each term of it is the sum of the two previous terms. In this problem, we need to find just the last digit of a Fibonacci series termed as F(n), where n is got as input.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/ed8f3bc0-4abc-4506-a101-29e4570e7911)


In the Main function, obtain input from the user in the console and display the the last digit of the term F (n) by calling the fiboLastDigit method 

#### Input format :
The input consists of an integer n(0 <= n <= 10000).

#### Output format :
Output the last digit of the term F (n).

**Sample test cases :<br>
Input 1 :<br>**
5<br>
**Output 1 :<br>**
5


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int fiboLastDigit(int a);

int main()
{
    int n;
    cin>>n;
    cout<<fiboLastDigit(n);
    return 0;
}

int fiboLastDigit(int a)
{
    long long int x=0,y=0,z=1,i;
    int s;
    for(i=0;i<a;i++)
    {
        z=y+z;
        x=z;z=y;y=x;
    }
    x=x%10;s=x;
    return s;
}

```


