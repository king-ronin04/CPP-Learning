# Casper at the Carnival

The Circoloco Children Carnival is the City’s largest and successful event dedicated to children and families. Casper is a smart little boy who loves eating cookies and drinking fresh juices. He visits the carnival with his parents and is going to spend N minutes at the event ground. Each minute he either eats a cookie or drinks fresh juice. Cookies are very sweet and thus Casper’s parents have instructed him to drink fresh juice in the next minute, after eating a cookie.



You are given whether he ate a cookie or drank fresh juice in each of the N minutes. Your task is to check if Casper followed his parents' instructions. That is, you need to verify whether after each eaten cookie he drinks fresh juice in the next minute.



#### Input format :
The first line of the input contains an integer N denoting the number of minutes.
<br>
The second line of the input contains N space-separated strings S1, S2, ...,SN. The string Si is either "cookie" (if Casper eats a cookie in the i-th minute) or "juice" (otherwise).



#### Output format :
Output a single line containing the answer — "Yes"(without quotes) if Casper followed his parents' instructions, and "No"(without quotes) otherwise, both without the quotes.

**Sample test cases :<br>
Input 1 :<br>**
7<br>
cookie juice juice cookie juice cookie juice<br>
**Output 1 :<br>**
Yes


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<cstring>
using namespace std;
int main()
{
    int i,s,n;
    cin>>n;
    char str[n][30];
    (n>1)?(s=0):(s=1);
    for(i=0;i<n;i++)
    {
        cin>>str[i];
        if(i>0)
        {
            if((strcmp(str[i-1],"cookie")==0)&&(strcmp(str[i],"juice")!=0)){s=1;}
        }
        if(i==n-1){if(strcmp(str[n-1],"cookie")==0){s=1;}}
    }
    (s==1)?cout<<"No":cout<<"Yes";
    return 0;
}



```

