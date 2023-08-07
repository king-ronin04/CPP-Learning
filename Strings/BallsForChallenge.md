# Balls for Challenge

The Circoloco Children Carnival is the City’s largest and successful event dedicated to children and families. The main focus at the carnival is the workshop arena where kids can participate in engaging and educational activities.

Charlie, a little boy accompanied by his Mom visited the fair, where he participated at the "Balls for Challenge" activity. He was given many balls of white and black colors. During the play, he arranged the balls into two rows both consisting of N number of balls. These two rows of balls are given to you in the form of strings X, Y. Both these string consist of 'W' and 'B', where 'W' denotes a white colored ball and 'B' a black colored.

Other than these two rows of balls, Charlie has an infinite supply of extra balls of each color. He wants to create another row of N balls, Z in such a way that the sum of hamming distance between X and Z, and hamming distance between Y and Z is maximized.

Hamming Distance between two strings X and Y is defined as the number of positions where the color of balls in row X differs from the row Y ball at that position. e.g. hamming distance between "WBB", "BWB" is 2, as at position 1 and 2, corresponding colors in the two strings differ. As there can be multiple such arrangements of row Z, Charlie wants you to find the lexicographically smallest arrangement which will maximize the above value.



#### Input format :
First line of the input will contain a string X denoting the arrangement of balls in first row.
<br>
Second line of the input will contain the string Y denoting the arrangement of balls in second row.

#### Output format :
Output a single line containing the string of length N denoting the arrangement of colors of the balls belonging to row Z.

**Sample test cases :<br>
Input 1 :<br>**
WBWB<br>
WBBB<br>
**Output 1 :<br>**
BWWW


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main(){
    int c=0;
    string str1,str2;
    cin>>str1>>str2;
    for(int i=0;i<str1.length();i++){
        if(str1[i]==str2[i]){
            if(str1[i]==87){
                cout<<"B";
            }
            else{
                cout<<"W";
            }
        }
        else{
            c++;
            if(c%2==0){
                cout<<str2[i];
            }else{
                cout<<str1[i];
            }
        }
    }
    return 0;
}

```
