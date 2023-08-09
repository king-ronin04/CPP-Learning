# Math Olympiad

 

The KISA Math Olympiad is held annually across all the Schools to identify and encourage the mathematical creativity of children of all grades. Samuel is a little genius in math of Grade 5 who was participating in the contest.

 

The question bank of the contest contains 35 questions and lasts for duration of 1 hour. Samuel was so confident of all the questions but he was seemed stuck at one question. He needs your help in answering that question so that he could score full marks and get a Gold medal in the event. The question that needs your assistance is as follows:


Write a recursive method to find the m-th summation of first n natural numbers. m-th summation of first n natural numbers is defined as following.<br>
If m > 1<br>
SUM(n, m) = SUM(SUM(n, m - 1), 1)<br>
Else
<br>
SUM(n, 1) = Sum of first n natural numbers.
<br>
We are given m and n, we need to find SUM(n, m).

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/006d7e67-04f4-4d60-a203-70709a0ea479)


In the Main function, obtain input from the user in the console and display the m-th summation of first n natural numbers by calling the summation 

#### Input format :
First line of the input is an integer ‘n’.
<br>
Second line of the input is an integer ‘m’.

#### Output format :
Output in a single line an integer that gives the m-th summation of first n natural numbers.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
3<br>
**Output 1 :<br>**
7260



-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include<iostream>
using namespace std;
int summation(int n,int m)
{
    if(m==0)
    return n;
    if(m!=0)
    {
        n=n*(1+n)/2;
        n=summation(n,m-1);
    }
    return n;
}

int main()
{
    int n,m,i;
    cin>>n;
    cin>>m;
    i=summation(n,m);
    cout<<i;
    return 0;
}


```
