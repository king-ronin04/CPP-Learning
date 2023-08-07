# Little Authors

"Little Authors" Slogan Writing Competition was organized for School students at Orchids Senior School. Any student who is creative and effective in communicating ideas in short, yet powerful about any instant topic can participate in the competition. The important guideline for the contest is that the Slogan should contain a string where the number of occurrences of some character in it is equal to the sum of the numbers of occurrences of other characters in the string. 

 

Write a program to help the event organizers to determine whether the submitted Slogans adhere to the given condition.

#### Input format :
First and only line of input contains one string S consisting of lowercase letters.

#### Output format :
Output a single line containing "Yes"(without quotes) if the string satisfies the condition given above or "No"(without quotes) otherwise.

**Sample test cases :<br>
Input 1 :<br>**
acab<br>
**Output 1 :<br>**
acab:Yes

**Input 2 :<br>**
abc<br>
**Output 2 :<br>**
abc:No


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
// You are using GCC
#include<iostream>
using namespace std;

int main(){
    int s=0,c=0;
    char ch;
    string str;
    getline(cin,str);
    int len=str.length();
    if(len%2==1){
        s=0;
    }
    else{
        for(int i=0;i<len;i++){
            ch=str[i];
            for(int j=0;j<len;j++){
                if(ch==str[j]){
                    c++;
                }
            }
            if(c==(len-c)){
                s=1;
                break;
            }
            c=0;
        }
    }
    if(s==0)
        cout<<str<<":No";
    else
        cout<<str<<":Yes";
    return 0;
    
}

```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<cstring>
using namespace std;
int main()
{
    int i,j,len,c1=0,s=0;
    char str[30],ch;
    cin>>str;
    ch=str[0];
    len=strlen(str);
    if(len%2==1){s=0;}
    else{
    for(i=0;i<len;i++)
    {
        ch=str[i];
        for(j=0;j<len;j++)
        {
            if(ch==str[j]){c1++;}
        }
        if(c1==(len-c1)){s=1;break;}
        c1=0;
    }
    }
    (s==0)?cout<<str<<":No":cout<<str<<":Yes";
    return 0;
}


```
