# Wildcard Matching

Sunil is a little scientist. Sunil has planned to design a wildcard pattern matcher to exhibit at the "Young Inventors", a tech talent show organized at his school.

Sunil wanted to design the wildcard pattern matcher supporting the wildcard character '?'. The wildcard character '?' can be substituted by any single lower case English letter for matching. He has two strings X and Y of equal length, made up of lower case letters and the character '?'.

Sunil wants your help in designing the device, to know whether the strings X and Y can be matched or not. Write a program to check whether the given strings can be matched or not.



#### Input format :
First line of the input contains the string ‘X’.
<br>
Second line of the input contains the string ‘Y’.

#### Output format :
Output a single line with the word "Yes"(without quotes) if the strings can be matched, otherwise output "No"(without quotes).

**Sample test cases :<br>
Input 1 :<br>**
s?or?<br>
sco??<br>
**Output 1 :<br>**
Yes




-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main(){
    string a,b;
    int s=0;
    getline(cin,a);
    getline(cin,b);
    for(int i=0;i<a.length();i++){
        if(a[i]!=b[i]){
            if((a[i]!=63)&&(b[i]!=63)){
                s=1;
                break;
            }
        }
    }
    if(s==0)
        cout<<"Yes";
    else
        cout<<"No";
    return 0;
}

```
