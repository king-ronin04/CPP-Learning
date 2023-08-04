# Charity Dinner
WeCanNGO Trust is organizing a charity dinner at St. John’s College. Since older students are both wiser and richer, the members of the trust decide that the price of each ticket will be based on how many years the students have been in the school. A first year student will buy a PINK ticket, a second year student will buy a GREEN ticket, a third year student will buy a RED ticket, and a fourth year student will buy an ORANGE ticket.

Assume that all tickets are sold. Each colour of ticket is uniquely priced. Write a program to output all combinations of tickets that produce exactly the desired amount to be raised. The combinations may appear in a specific order. First ORANGE is considered, then RED, then GREEN and finally PINK. Also display the total number of combinations found and the smallest number of tickets to be printed to raise the desired amount so that printing cost is minimized.

#### Input format :
First 4 lines of the input correspond to the cost of a PINK, GREEN, RED, ORANGE ticket (in the exact order).
<br>
Last line of the input corresponds to the exact amount of money to be raised by selling tickets.

#### Output format :
Output all combinations of tickets that produce exactly the desired amount to be raised. The combinations may appear in any order. Output the total number of combinations found. Output the smallest number of tickets to print to raise the desired amount so that printing cost is minimized.
<br>
Refer sample input and output for formatting specifications.

**Sample test cases :<br>
Input 1 :<br>**
1<br>
2<br>
3<br>
4<br>
3<br>
**Output 1 :<br>**
#of PINK is 0 # of GREEN is 0 # of RED is 1 # of ORANGE is 0<br>
#of PINK is 1 # of GREEN is 1 # of RED is 0 # of ORANGE is 0<br>
#of PINK is 3 # of GREEN is 0 # of RED is 0 # of ORANGE is 0<br>
Total combinations is 3<br>
Minimum number of tickets to print is 1<br>

**Input 2 :<br>**
1<br>
2<br>
4<br>
3<br>
4<br>
**Output 2 : <br>**
#of PINK is 0 # of GREEN is 0 # of RED is 1 # of ORANGE is 0 <br>
#of PINK is 0 # of GREEN is 2 # of RED is 0 # of ORANGE is 0<br>
#of PINK is 1 # of GREEN is 0 # of RED is 0 # of ORANGE is 1<br>
#of PINK is 2 # of GREEN is 1 # of RED is 0 # of ORANGE is 0<br>
#of PINK is 4 # of GREEN is 0 # of RED is 0 # of ORANGE is 0<br>
Total combinations is 5<br>
Minimum number of tickets to print is 1<br>


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int p,g,r,o,t,i,j,k,l,min=10000,c=0,x;
    cin>>p>>g>>r>>o>>t;
    for(i=0;i<=t;i++)
    {
        for(j=0;j<=t;j++)
        {
            for(k=0;k<=t;k++)
            {
                for(l=0;l<=t;l++)
                {
                    if(((p*i)+(g*j)+(r*k)+(o*l))==t)
                    {
                        cout<<"# of PINK is "<<i<<" # of GREEN is "<<j<<" # of RED is "<<k<<" # of ORANGE is "<<l<<"\n";
                        c++;
                        x=i+j+k+l;
                        if(min>x)
                        {
                            min=x;
                        }
                    }
                }
            }
        }
    }
    cout<<"Total combinations is "<<c<<"\n";
    cout<<"Minimum number of tickets to print is "<<min;
    return 0;
}


```
