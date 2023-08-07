# Swapping 2 numbers

Mrs. Anitha , our favourite Maths teacher wanted to teach her students to swap two elements.
<br>
Write a program to accept 2 integers and to swap them using functions and pointers.
<br>
**Function Specification:**<br>
void swap(int *a,int *b)<br>
This functions swaps 2 integers.

#### Input format :
The input consists of 2 integer.

#### Output format :
Output prints the integers after swapping.

**Sample test cases :<br>
Input 1 :<br>**
4 5<br>
**Output 1 :<br>**
5 4


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
void swap(int*a,int*b)
{
    *a=*a+*b;
    *b=*a-*b;
    *a=*a-*b;
}

int main()
{
    int a,b;
    cin>>a>>b;
    swap(&a,&b);
    cout<<a<<" "<<b;
    return 0;
}


```
