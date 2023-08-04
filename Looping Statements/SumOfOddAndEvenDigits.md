# Sum of Odd and Even Digits

Write a program to calculate the sum of odd and even digits in a number. The input consists of a single integer 'n' which corresponds to the given number.The output must display the sum of odd numbers and even numbers.

#### Input format :
Input consists of a long number.

#### Output format :
Output prints the sum of odd numbers and even numbers separated by a space.

**Sample test cases : <br>
Input 1 :** <br>
3924209420352 <br>
**Output 1 :** <br>
29 16


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int main()
{
	   long int number;
	  int n,even=0,odd=0;
	    cin>>number;
	    while(number!=0)
	    {
	   n=number%10;
	   if(n%2==0)
	   {
	   even=even+n;
	   }
	   else
	   {
	   odd=odd+n;
	   }
	number=number/10;
	    }
	    cout<<odd<<" "<<even;
	}




```
