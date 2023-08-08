# Junior Coders

 

Junior Coders Academy is a unique learning Centre that offers a creative and inspiring collaborative environment for building coding skills to students of Grades 1 to 12.

Williams, the proprietor of the Academy and the mentor for the students started his first session of the day with the interesting programming concept of using Functions. Post an interactive session of learning through design, Williams gave the students a small self-activity to verify from two integer numbers A and B, if B corresponds to the last digit/digits of A. Williams wanted you to write the program for evaluating the students’ codes.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/b5a84d3b-e06b-4396-81b4-e856e8e33dd8)


In the Main function, obtain input from the user in the console and display "Yes" if the second number B is the last digits of A, else Print "No" by calling the findValue method 



#### Input format :
First line of the input contains the number A.
<br>
Second line of the input contains the number B.




#### Output format :
Print "Yes")without quotes) if the second number B is the last digits of A. Print "No"(without quotes) otherwise.

**Sample test cases :<br>
Input 1 :<br>**
1234<br>
1234<br>
**Output 1 :<br>**
Yes


-------------------------------------------------------------------------------------------------------------------------------------------------------------------





```cpp
#include<iostream>
#include<cstring>
using namespace std;
int findValue(char a[],char b[]);

int main()
{
    char a[50],b[20];
    cin>>a>>b;
    if(findValue(a,b)==1)
    {
        cout<<"Yes";
    }
    else 
    cout<<"No";
    return 0;
}

int findValue(char a[],char b[])
{
    int s,t,u,v;
    s=strlen(a);
    t=strlen(b);
    u=s-t;
    for(v=0;v<t;v++)
    {
        if(a[u]!=b[v]){s=-5;break;}
        u++;
    }
    if((s==-5)||(t>s)){return 0;}
    else
    return 1;
}
```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<string>
using namespace std;

int findValue(string a, string b){
    string temp;
    if(a.length()>=b.length()){
        temp=a.substr(a.length()-b.length());
    }
    return temp==b;
}

int main(){
    string a,b;
    cin>>a>>b;
    int res=findValue(a,b);
    cout<<(res?"Yes":"No");
}

```


