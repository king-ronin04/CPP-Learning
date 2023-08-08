# Reverse the digits

 

Asha’s birthday is shortly coming and her parents have planned to arrange for a house party. Deepa was Asha’s best friend and was expecting her birthday since a month. This is because Deepa’s Dad has promised her that he and Deepa together would design a Reverse Talking kitty toy all by themselves and gift it to Asha. Deepa believed that Asha might be overjoyed with this gift from her dear friend.

Deepa’s Dad put the best of his efforts to design the toy. As a first module in the design he intended to reverse a numeric input given to it. He needs your help to write a recursive method for reversing the digits of the given number N. Please assist him in the task.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/193e2d0d-83c4-48de-9c77-85ceb2024f25)


In the Main function, obtain input from the user in the console and display the reverse of a N digit number by calling the reverse method 





#### Input format :
The first line of the input is an integer N.

#### Output format :
Print the reverse of a N digit number.

**Sample test cases :<br>
Input 1 :<br>**
1234<br>
**Output 1 :<br>**
4321


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int reverse(int n)
{
    static int rev;
    if(n!=0)
    {
        rev=rev*10;
        rev=rev+n%10;
        reverse(n/10);
    }
    else return 0;
    return rev;
}
int main()
{
    int n;
   cin>>n;
    n=reverse(n);
    cout<<n;
    return 0;
}

```




