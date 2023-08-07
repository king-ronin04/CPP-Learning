# Alternating Code

It is IPL Season and the first league match of Dhilip’s favorite team, "Chennai Super Kings". The CSK team is playing at the IPL after 2 years and like all Dhoni lovers, Dhilip is also eagerly awaiting to see Dhoni back in action.

After waiting in long queues, Dhilip succeeded in getting the tickets for the big match. On the ticket, there is a letter-code that can be represented as a string of upper-case Latin letters.

Dhilip believes that the CSK Team will win the match in case exactly two different letters in the code alternate. Otherwise, he believes that the team might lose. Please see note section for formal definition of alternating code.

You are given a ticket code. Please determine, whether CSK Team will win the match or not based on Dhilip’sconviction. Print "YES" or "NO" (without quotes) corresponding to the situation.

**Note:**
Two letters x, y where x != y are said to be alternating in a code, if code is of form "xyxyxy...".

#### Input format :
First and only line of the input contains a string S denoting the letter code on the ticket.

#### Output format :
Output a single line containing "Yes" (without quotes) based on the conditions given and "No" otherwise.

**Sample test cases :<br>
Input 1 :<br>**
ABABAB<br>
**Output 1 :<br>**
Yes


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<cstring>
using namespace std;
int main()
{
    int i,len,s=0;
    char a[20],x,y;
    cin>>a;
    len=strlen(a);
    x=a[0];y=a[1];
    if(x==y){s=1;}
    else{
    for(i=0;i<len;i++)
    {
        if(i%2==0){if(x!=a[i]){s=1;break;}}
        else if(y!=a[i]){s=1;break;}
    }
    }
    (s==1)?cout<<"No":cout<<"Yes";
    return 0;
}


```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
bool check(string str){
    int len=str.length();
    if(len%2!=0){
        if(str[0]!=str[len-1]){
            return false;
        }
    }else{
        for(int i=0;i<len-2;i++){
            if((str[i]!=str[i+2]) && (str[i+1]!=str[i+3])){
                return false;
            }
        }
    }
    return true;
}
int main(){
    string str;
    cin>>str;
    bool flag=check(str);
    if(flag)
        cout<<"Yes";
    else
        cout<<"No";
    
    return 0;
}

```
