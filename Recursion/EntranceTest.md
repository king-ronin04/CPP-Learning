# Entrance Test

 

"Success Academy" has arranged for a entrance test for High School students from rural villages. Those successful students of the test will be awarded the scholarship for their IIT/JEE preparations at Success Academy. Sunil, the co-coordinator and founder of the academy has given one problem for the first stage of the test. The problem goes like this:

 

Given two integers x and n, find the number of ways to express x as sum of n-th powers of unique natural numbers. It is given that 1 <= n <= 20.

 

Sunil himself has not computed the solution of the problem. Write a recursive method to help him find the answer for the same to evaluate the students.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/fe538125-d927-4d3f-a4a3-20ea3cc47f40)


In the Main function, obtain input from the user in the console and display the number of ways to express x as sum of n-th powers of unique natural numbers by calling the countWays method 

#### Input format :
The first line of input contains the integer x.
<br>
The second line contains the integer n.

#### Output format :
Output the number of ways to express x as sum of n-th powers of unique natural numbers in a single line.

**Sample test cases :<br>
Input 1 :<br>**
100<br>
2<br>
**Output 1 :<br>**
3


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<cmath>
using namespace std;
int count(int x,int n,int num)
{
    int i;
    i=x-pow(num,n);
    if(i==0)
    {
        return 1;
    }
    if(i<0)
    {
        return 0;
    }
    else
    return count(i,n,num+1)+count(x,n,num+1);
}
int countWays(int x,int n)
{
    return count(x,n,1);
}
int main()
{
    int x,n;
    cin>>x;
    cin>>n;
    cout<<countWays(x,n);
    return 0;
}

```


