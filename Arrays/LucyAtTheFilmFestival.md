# Lucy at the Film Festival
LucarnosFilm Festival is an annual film festival and is also known for being a prestigious platform for art house films. This time at the Lucarnos Film festival there are N movies screened, each of different genre ranging from drama movies to comedy ones and teen movies to horror ones. Lucy is a huge fan of movies and visited the film festival, but she's not sure which movie she should watch.

Each movie can be characterized by two integers Li and Ri, denoting the length and the rating of the corresponding movie. Lucy wants to watch exactly one movie with the maximal value of Li × Ri. If there are several such movies, she would pick a one with the maximal Ri among them. If there is still a tie, she would pick the one with the minimal index among them.

Write a program to help Lucy pick a movie to watch at the film festival.

#### Input format :
The first line of the input description contains an integer n. Assume that the maximum value for n as 50.
<br>
The second line of the input description contains n integers L1, L2, ...,Ln.
<br>
The following line contains n integers R1, R2, ...,Rn.

#### Output format :
Output a single integer i denoting the index of the movie that Lucy should watch in the film festival. Note that you follow 1-based indexing.

**Sample test cases :<br>
Input 1 :<br>**
2<br>
1 2<br>
2 1<br>
**Output 1 :<br>**
1

**Input 2 :<br>**
4<br>
2 1 4 1<br>
2 4 1 4<br>
**Output 2 :<br>**
2

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j,k,l;
    cin>>n;
    int a[n],b[n];
    for(i=0;i<n;i++)
    {
        cin>>a[i];
    }
    for(i=0;i<n;i++)
    {
        cin>>b[i];
        a[i]=a[i]*b[i];
    }
    j=a[0];
    for(i=1;i<n;i++)
    {
        if(j<a[i]){j=a[i];k=b[i];}
    }
    for(i=n-1;i>=0;i--)
    {
        if((j==a[i])&&(b[i]>=k)){k=b[i];l=i+1;}
    }
    cout<<l;
    return 0;
}


```
