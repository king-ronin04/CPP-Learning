# Nela's Birthday and Colorfull Balloons

Nella is an eight-year-old princess who will inherit the kingdom of Castlehaven. It is her birthday today and her Dad, the King of Castlehaven has arranged for a grand party.Nella loves colorful balloons and so her Dad planned to decorate the entire palace with balloons of the colors that Nella loved. So he asked her about her color preferences. The sophisticated princess that Nella is, she likes only two colors — amber and brass. Her Dad boughtn balloons, each of which was either amber or brass in color.

You are provided this information in a string s consisting of characters 'a' and 'b' only, where 'a' denotes that the balloon is amber, where 'b' denotes it being brass colored. When Nella saw the balloons, she was furious with anger as she wanted all the balloons of the same color. In her rage, she painted some of the balloons with the opposite color (i.e., she painted some amber ones brass and vice versa) to make all balloons appear to be the same color.

It took her a lot of time to do this, but you can probably show her the right way of doing so, thereby teaching her a lesson to remain calm in difficult situations, by finding out the minimum number of balloons needed to be painted in order to make all of them the same color.



#### Input format :
The first and only line of input contains a string s.

#### Output format :
Output a single line containing an integer — the minimum number of flips required.

**Sample test cases :<br>
Input 1 :<br>**
ab<br>
**Output 1 :<br>**
1



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main(){
    int a=0,b=0;
    string str;
    cin>>str;
    for(int i=0;i<str.length();i++){
        if(str[i]=='a')
            a++;
        else
            b++;
    }
    cout<<(a<b?a:b);
    return 0;
}

```
