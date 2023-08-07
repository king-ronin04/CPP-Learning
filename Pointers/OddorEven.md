# Odd or Even

Mrs. Anitha , our favourite Maths teacher wanted to teach her students to check whether the given number is odd or even.
<br>
Write a program to accept an integer and to check whether the given number is odd or even using functions and pointers.

**Note:** Print the text "a is an odd number " and "a is an even number" inside the function. 

__Function Specification:__ <br>
void oddoreven(int *a)

This function prints the text "a is an odd number" if the number is odd, else prints "a is an even number" if the number is even.

#### Input format :
The input consists of an integer.



#### Output format :
Output prints whether the given integer is an odd or even number.

**Sample test cases :<br>
Input 1 :<br>**
10<br>
**Output 1 :<br>**
10 is even


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
void oddoreven(int *a)
{
    cout<<*a<<" is";
    (*a%2==0)?cout<<" even":cout<<" odd";
}
int main()
{
    int a;
    cin>>a;
    oddoreven(&a);
    return 0;
}
```
