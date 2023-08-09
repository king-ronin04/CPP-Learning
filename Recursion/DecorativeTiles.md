# Decorative Tiles

 

Carlton Inn is planning to organize a Food Festival bringing together at one place, a wide variety of cuisines from across the world on account of Christmas. The Hotel Management has rented out a hall of an indoor Auditorium for this extravaganza.

 

The Event hall was of area N*M and the coordinators planned to decorate the hall’s flooringwith carpet tiles embellishing the opulence of the event. They have infinite number of tiles of size 2i X 2i, where i = 0, 1, 2,… so on. Their task is to find minimum number of tiles required to fill the given area with tiles.

 

Help them accomplish their task by writing a recursive method that finds the minimum number of tiles required to fill the given area with tiles.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/5f9cc5ee-7ab2-4538-bc21-17ba8895086e)


In the Main function, obtain input from the user in the console and display the minimum count of tiles required by calling the minimumTiles method

#### Input format :
First line of the input is an integer ‘N’.
<br>
Second line of the input is an integer ‘M’.

#### Output format :
Output an integer in a single line that gives the minimum count of tiles required.



**Sample test cases :<br>
Input 1 :<br>**
5<br>
6<br>
**Output 1 :<br>**
9


-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include<iostream>
using namespace std;
int minimumTiles(int n,int m)
{
    static int count,s,m1;
    int i=1,j=1;
    if(s==0){m1=m;s++;}
    while(i<=n)
    {
        i=i*2;
    }
    i=i/2;
    while(j<=m)
    {
        j=j*2;
    }
    j=j/2;
    if(n==0)
    {
        return count;
    }
    else if(m==0)
    {
        minimumTiles(n-i,m1);
    }
    else
    {
        (i>j)?(count=count+(i/j)):(count=count+(j/i));
        minimumTiles(n,m-j);
    }
    return count;
}
int main()
{
    int n,m;
    cin>>n;
    cin>>m;
    cout<<minimumTiles(n,m);
    return 0;
}
```




-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include<iostream>
using namespace std;

int minimumTiles(int n,int m){
    if(n==0||m==0)
        return 0;
    else if(n%2==0 && m%2==0)
        return minimumTiles(n/2,m/2);
    else if(n%2==0&&m%2==1)
        return (n+minimumTiles(n/2,m/2));
    else if(n%2==1 && m%2==0)
        return (m+minimumTiles(n/2,m/2));
    else
        return (n+m-1+minimumTiles(n/2,m/2));
        
        
}

int main(){
    int n,m;
    cin>>n>>m;
    cout<<minimumTiles(n,m);
    return 0;
}
```

