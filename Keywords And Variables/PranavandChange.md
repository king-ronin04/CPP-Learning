# Pranav and Change
Pranav, an enthusiastic kid visited the "Fun Fair 2017" along with his family. His father wanted him to purchase entry tickets from the counter for his family members. Being a little kid, he is just learning to understand about units of money. Pranav has paid some amount of money for the tickets but he wants your help to give him back the change of Rs. N using minimum number of rupee notes.

Consider a currency system in which there are notes of seven denominations, namely, Rs. 1, Rs. 2, Rs. 5, Rs. 10, Rs. 50, Rs. 100. If the change given to Pranav Rs. N is input, write a program to computer smallest number of notes that will combine to give Rs. N.

#### Input format :
First line of the input is an integer N, the change to be given to Pranav

#### Output format :
Output should display the the smallest number of notes that will combine to give N.

**Sample test cases : <br>
Input 1 :** <br> 
1200<br>
**Output 1 :** <br>
12

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int main()
{
  int cash,sum;
    cin>>cash;
    sum=cash/100;
    cash=cash%100;
    sum=sum+(cash/50);
    cash=cash%50;
    sum=sum+(cash/10);
    cash=cash%10;
    sum=sum+(cash/5);
    cash=cash%5;
    sum=sum+(cash/2);
    cash=cash%2;
    sum=sum+(cash/1);
    cout<<sum;
return 0;
}


```
