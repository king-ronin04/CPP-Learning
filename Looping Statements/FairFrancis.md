# Fair Francis
"Think Academy" has arranged for a competitive test for engineering students from rural villages. Those successful students of the test will be awarded the scholarship for their GRE/TOEFL preparations at Think Academy. Francis, the co-coordinator and founder of the academy has N different problemsets and there are N students who are appearing for the test. Each problemset contains zero or more problems. He will give each student exactly one problemset. But the problemsets might contain different number of problems in each one, which looks unfair.

Since Francis is a fair tutor, he decided to move some problems from problemset to another problemset (he can do this multiple times), until all problemsets contain the same number of problems.

Sometimes it's impossible to do so, and he might need to delete some problems completely before moving any problem, then he will start moving the problems. He needs your help to write a program to calculate the minimum number of problems to be deleted, and the minimum number of problems to be moved. 

#### Input format :
First line of the input contains one integer N (1 <= N <= 100) representing the number of problemsets and the number of trainees.
<br>
Second line of the input contains N non-negative integers separated by a single space, representing the number of problems in each problemset. Each problemset will contain at most 100 problems.
#### Output format :
Output a single line which will contain the minimum number of problems to be deleted, followed by a space then the minimum number of problems to be moved.

**Sample test cases :<br>
Input 1 :<br>**
3<br>
3 3 3<br>
**Output 1 :** <br>
0 0

**Input 2 :<br>**
4<br>
6 4 5 3<br>
**Output 2 :<br>**
2 1


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j=0,k,l,m=0;
    cin>>n;
    int a[n];
    for(i=0;i<n;i++)
    {
        cin>>a[i];
        j=j+a[i];
    }
    k=j/n;
    l=j-(k*n);
    for(i=0;i<n;i++)
    {
        if(a[i]<k){a[i]=0;}
        else{a[i]=a[i]-k;}
        m=m+a[i];
    }
    m=m-l;
    cout<<l<<" "<<m;
    return 0;
}

```
