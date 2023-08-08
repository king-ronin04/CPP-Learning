# Nice Number

 

" The Greatest Furniture Expo" is a biggest fair exhibiting furniture products, services and equipment, interior services, decoration plans, modular kitchen accessories, bedroom furniture, stylish sittings etc in the Furniture industry. It is a 4-day event and on the inaugural day of the event, the Event coordinators have announced for a Lucky lottery contest.

 

According to the Lucky lottery, the visitors’ entry tickets are collected and the visitors whose ticket numbers are nice numbers are chosen as winners and attractive discount coupons are distributed to the winners. A nice number is a positive integer which has exactly 4 divisors.

 

The Event coordinators wanted to know if a specific’s entry ticket number is a nice number or not.


![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/28642e8d-f4f7-4d40-a27c-450fdfb6e5f5)



In the Main function, obtain input from the user in the console and display "Nice" if the given ticket number is a nice number. Print "Not Nice" otherwise by calling the findType method..



#### Input format :
First line of the input is an integer that corresponds to the entry ticket number of a visitor

#### Output format :
Output should display "Nice"(without quotes) if the given ticket number is a nice number. Print "Not Nice"(without quotes) otherwise.



**Sample test cases :<br>
Input 1 :<br>**
6<br>
**Output 1 :<br>**
6 is Nice


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int findType(int a);

int main()
{
    int num;
    cin>>num;
    if(findType(num)==1)
    {
        cout<<num<<" is Nice";
    }
    else cout<<num<<" is not Nice";
    return 0;
}
int findType(int a)
{
    int i,j=0;
    for(i=2;i<=a/2;i++)
    {
        if(a%i==0){j++;}
    }
    if(j==2){return 1;}
    else return 0;
}

```




