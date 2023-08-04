# Math challenge

In connection to the National Mathematics Day celebration, the Regional Mathematical Scholars Society had arranged for a Math Challenge Event where high school students participated in large number. First level of the challenge was oral quiz, followed by a written test in the second round.
<br>
In the second round, the problem that the students had to answer goes like this:
<br>
For every positive number ‘n’ we define a function streak(n)=k as the smallest positive integer k such that n+k is not divisible by k+1.

 E.g:

13 is divisible by 1
<br>
14 is divisible by 2
<br>
15 is divisible by 3
<br>
16 is divisible by 4
<br>
17 is NOT divisible by 5
<br>
So streak(13)=4.

Now, define P(s,N) to be the number of integers n, 1<n<N, for which streak(n)=s. Write a program to get the input as 's' and 'N' and find the count of integers until N which has the streak value as 's'.



#### Input format :
First line of the input is an integer ‘s’ which is the streak value of an integer n.
<br>
Second line of the input is an integer ‘N’ which is the upper limit of numbers until which P(s,N) is calculated.

#### Output format :
Output is an integer that gives the count of integers until ‘N’ which has the streak value as ‘s’.

**Sample test cases :<br>
Input 1 :<br>**
3<br>
14<br>
**Output 1 :<br>**
1


----------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int main()
{
    int s,p,i,j,n,a=0,c=0;
    cin>>s>>p;
    for(i=1;i<=p;i++)
    {
        n=i;
        for(j=1;j<=p;j++)
        {
            if(n%j==0){c++;n++;}
            else{break;}
        }
        if(c==s){a++;}
        c=0;
    }
    cout<<a;
    return 0;
}


```
