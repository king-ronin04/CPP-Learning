# Teaching Sum Of Elements

Mrs. Anitha , our favourite Maths teacher wanted to teach her new batch of students to find the sum of a set of numbers. In their first attempt, all her students computed the sum wrongly but to her surprise she found that all the students have got the same answer. On analyzing the answer, she found that students are good in addition but they have neglected the negative sign present in front of some numbers. She taught them about positive and negative numbers and she again gave the same problem to the students. All the students did the problem correctly and Mrs. Anitha was happy.

 

Write a program to accept a set of n integers and to calculate the wrong sum and the correct sum using functions.

**PROBLEM REQUIREMENTS:**
<br>
int wrongsetsum(int n, int * a)
<br>
int correctsetsum(int n, int * a)

#### Input format :
Input consists of n+1 integers. The first integer corresponds to 'n', the number of elements in the set. The next 'n' integers correspond to the elements in the set. Assume that the maximum value of n is 20.

#### Output format :
Output consists of 2 integers. The first integer corresponds to the wrong sum and the second integer corresponds to the correct sum.



**Sample test cases :<br>
Input 1 :<br>**
5<br>
-1 2 -3 4 -5<br>
**Output 1 :<br>**
15<br>
-3


```cpp
#include<iostream>
#include<cmath>
#include<cstdlib>
using namespace std;
int wrongsetsum(int n,int *a)
{
    int sum=0,i;
    for(i=0;i<n;i++)
    {
        sum=sum+abs(*(a+i));
    }
    return sum;
}
int correctsetsum(int n,int *a)
{
    int sum=0,i;
    for(i=0;i<n;i++)
    {
        sum=sum+*(a+i);
    }
    return sum;
}


int main()
{
    int i,n;
    cin>>n;
    int *p=(int*)malloc(n*sizeof(int));
    for(i=0;i<n;i++)
    {
        cin>>*(p+i);
    }
    i=wrongsetsum(n,p);
    cout<<i;
    i=correctsetsum(n,p);
    cout<<"\n"<<i;
    return 0;
}


```



