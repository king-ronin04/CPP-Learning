# Adjacent characters

Given a string, write a program to compute a new string where identical chars that are adjacent in the original string are separated from each other by a "*".

#### Input format :
The input consists of a string

#### Output format :
Output prints a new string where identical chars that are adjacent in the original string are separated from each other by a "*"

**Sample test cases :<br>
Input 1 :<br>**
hello
**Output 1 :<br>**
hel*lo


-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;

int main(){
    string str;
    getline(cin,str);
    string newstr="";
    for(int i=0;i<str.length();i++){
        newstr+=str[i];
        if((i<str.length())&&(str[i]==str[i+1])){
            newstr+="*";
        }
    }
    cout<<newstr;
}
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include <iostream>
using namespace std;
void pairStar(string& input, string& output,
              int i = 0)
{
    output = output + input[i];
    if (i == input.length() - 1)
        return;
    if (input[i] == input[i + 1])
        output = output + '*';

    pairStar(input, output, i+1);
}
int main()
{
    string input, output = "";
    cin>>input;
    pairStar(input, output);
    cout << output << endl;
    return 0;
}


```
