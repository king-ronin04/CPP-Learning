# Winter Challenge

Swapna is a regular reader of Youth Digest magazine. The magazine has a whole host of fun and interesting facts from around for the youth especially that encourage interactivity and enhances their imagination.


"Winter Challenge" is an event announced in the December month edition of the magazine. Readers of the magazine who are between 10 to 15 years can participate in the special challenge. Those readers who participate and give the correct answer for the challenge will avail exciting gift coupons. According to the event, the challenge published was:

Given 0 < x < m, where x and m are integers, the modular inverse of x is the unique integer n, 0 < n < m, such that the remainder upon dividing x × n by m is 1.

For example,
<br>
if x = 4 and m = 17, we get n = 13
<br>
4 x 13 = 52 = 17 x 3 + 1, so the remainder when 52 is divided by 17 is 1, and thus 13 is the inverse of 4 modulo 17.

 

Swapna wants your help to find the correct answer for the problem based on the inputs given in the magazine.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/c9fd2131-83c8-43af-bf5b-e45dab1d764f)

In the Main function, obtain input from the user in the console and display the modular inverse n, or -1 if there is no such integer n by calling the findValue method 

#### Input format :
First line of the input is an integer that corresponds to x.
<br>
Second line of the input is an integer that corresponds to m.



#### Output format :
Output should display the appropriate value or print -1 otherwise.

**Sample test cases :<br>
Input 1 :<br>**
4<br>
17<br>
**Output 1 :<br>**
13


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int findValue(int x,int m);

int main()
{
    int x,m;
    cin>>x;
    cin>>m;
    cout<<findValue(x,m);
    return 0;
}

int findValue(int x,int m)
{
    int i,j;
    for(i=1;i<100000;i++)
    {
        j=(m*i)+1;
        if(j%x==0){break;}
    }
    if(j%x==0){return j/x;}
    else return -1;
}


```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int findValue(int,int);


int findValue(int x,int m){
    for(int i=m;i>=1;i--){
        if((i*x-1)%m==0)
            return i;
    }
    return -1;
}



int main(){
    int n,m;
    cin>>n>>m;
    
    cout<<findValue(n,m);
    return 0;
}
```
