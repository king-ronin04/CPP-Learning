# Number Challenge

Mike set off with great zeal to the "Kracker Jack Fun Fair 2017". There were numerous activities in the fair, though Mike being a math expert, liked to participate in the Number Challenge.



Mike was given a string D of numbers containing only digits 0's and 1's. His challenge was to make the number to have all the digits same. For that, he should change exactly one digit, i.e. from 0 to 1 or from 1 to 0. If it is possible to make all digits equal (either all 0's or all 1's) by flipping exactly 1 digit then he has to output "Yes", else print "No" (without quotes).



Write a program to help Mike win over his challenge.



#### Input format :
First and only input contains a string D of numbers made of only digits 1's and 0's.

#### Output format :
Output “Yes" or a "No", depending on whether its possible to make it all 0s or 1s or not. 

**Sample test cases :<br>
Input 1 :<br>**
101<br>
**Output 1 :<br>**
Yes


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;

int main(){
    int zero=0,one=0;
    string str;
    cin>>str;
    
    for(int i=0;i<str.length();i++){
        if(str[i]==48)
            zero++;
        else
            one++;
    }
    if((zero==1)||(one==1)){
        cout<<"Yes";
    }else{
        cout<<"No";
    }
    return 0;
    
}
```
