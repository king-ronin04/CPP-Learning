# Caption Contest
Exeter Caption Contest is a competition open to all writers worldwide. The entrants will have one day to compose and submit a caption that will be based on the theme posted on the competition page.

Robin, a creative writer had penned two captions for the contest but he unknowingly misplaced them. After searching long, he managed to locate his captions, but some letters in them have become unreadable. The captions were in two very old sheets of paper, each of which originally contained a string of lowercase English letters. The strings on both the sheets have equal lengths.

Robin would like to estimate the difference between these strings. Let's assume that the first string is named S1, and the second S2. The unreadable symbols are specified with the question mark symbol '?'. The difference between the strings equals to the number of positions i, such that S1i is not equal to S2i, where S1i and S2i denote the symbol at the i th position in S1 and S2, respectively.

Robin would like to know the minimal and the maximal difference between the two strings, if he changes all unreadable symbols to lowercase English letters. Robin is not an expertise in programming and so he needs your help solving this problem!

#### Input format :
The second line of the input contains a string S1
<br>
The second line of the input contains a string S2.
<br>
Both strings consist of lowercase English letters and question marks in places where the symbols are unreadable.

#### Output format :
Output the minimal and the maximal difference between two given strings separated with a single space.

**Sample test cases :<br>
Input 1 :<br>**
a?c<br>
??b<br>
**Output 1 :<br>**
1 3


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;

int main(){
    
    string str1,str2;
    cin>>str1>>str2;
    int minx=0,maxx=0;
    for(int i=0;i<str1.length();i++){
        if(str1[i]=='?'|| str2[i]=='?'){
            maxx=maxx+1;
        }
        else if(str1[i]!=str2[i]){
            minx=minx+1;
            maxx=maxx+1;
        }
    }
    cout<<minx<<" "<<maxx;
    
    return 0;
    
}

```

