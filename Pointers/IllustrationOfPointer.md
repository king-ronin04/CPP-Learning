# Illustration of Pointer

Few of the students in a class started playing game during their leisure hour. In this game, there were cards with numbers written on it. Each person need to pick 2-cards from this set. The two-cards are denoted as A and B. The goal of the game is to modify the value of A and B. A should be modified as absolute sum of A and B and B should be modified as absolute difference between A and B. The resultant A and B should always be positive.
<br>
Write a program to find the modified values of A and B to accomplish this goal using functions and pointers.

**Function specifications:**<br>
void changeValue(int *a, int *b)

This function changes the value of A and B as per problem description

#### Input format :
Input will contain two integers, A and B

#### Output format :
Print the updated value of A and B.

**Sample test cases :<br>
Input 1 :<br>**
5 7<br>
**Output 1 :<br>**
12<br>
2



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<cstdlib>
using namespace std;
void changeValue(int*a,int*b)
{
    int c=*a;
    int d=*b;
    *a=abs(c+d);
    *b=abs(c-d);
}
int main()
{
    int a,b;
    cin>>a>>b;
    changeValue(&a,&b);
    cout<<a<<"\n";
    cout<<b;
    return 0;
}



```
