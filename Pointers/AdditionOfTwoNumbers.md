# Addition of two numbers

Mrs. Anitha , our favourite Maths teacher wanted to teach her new batch of students to find the sum of two numbers using pointers. In their first attempt, all her students computed the sum wrongly. She taught them the concept of pointers and pass by value and pass by reference and she again gave the same problem to the students. All the students answered the problem correctly and Mrs. Anitha was happy.
<br>
Write a program to accept a 2 integers and to calculate the sum of 2 numbers using functions and pointers.

**Note:** Print the text "Sum of two elements = " inside the function.

Use this function void __addition(int *a,int *b)__ calculates the sum of 2 numbers

#### Input format :
The input consists of 2 integers.

#### Output format :
Output consists of 1 integer

**Sample test cases :<br>
Input 1 :<br>**
4 10<br>
**Output 1 :<br>**
14



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
void addition(int *a,int *b)
{
    cout<<(*a+*b);
}
int main()
{
    int a,b;
    cin>>a>>b;
    addition(&a,&b);
    return 0;
}



```
