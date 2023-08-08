# Candy Quiz

 

Anto and Jim were best friends. They went to a nearby Super Market to get some candies, where they saw an on-the-spot event organized for the kids. The event is a one minute quiz game where two kids can participate and the winners were announced a basket full of candies.

 

Anto and Jim eagerly participated in the game and managed to answer most of the questions right. The final question came to them from the host looked a bit tricky to solve. They wanted your help to answer it and take home the candies. The question posted to them was to find the last non-zero digit of n! where the event host gave them the value of ‘n’.

 

Given 'n', write a recursive method to find the last non-zero digit of n!.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/6fd66f99-693c-4023-84bb-db1398bc028a)


In the Main function, obtain input from the user in the console and display the last non-zero digit of n! by calling the lastNonZeroDigit method

#### Input format :
First and only line of the input is an integer ‘n’.

#### Output format :
Output the last non-zero digit of n! in a single line.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
**Output 1 :<br>**
2



-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<cstdlib>
using namespace std;
int lastNonZeroDigit(long long int num)
{
    static int s;
    if(s==0)
    {
        int i;long long int fact=1;
        for(i=1;i<=num;i++)
        {
            if(fact%10==0){fact=fact/10;}
            if(fact>1000000000){fact=fact%1000;}
            fact=fact*i;
        }
        num=fact;
        s=1;
    }
    if(num%10==0){return lastNonZeroDigit(num/10);}
    return abs(num%10);
}
int main()
{
    int n;
    cin>>n;
    cout<<lastNonZeroDigit(n);
    return 0;
}

```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;


static int dig[]={1,1,2,6,4,2,2,4,2,8};
int fun(int n){
    if(n<10) return dig[n];
    if(((n/10)%10)%2==0)
        return (6*fun(n/5)*dig[n%10])%10;
    else 
        return(4*fun(n/5)*dig[n%10])%10;
}

int main(){
    int n;
    cin>>n;
    cout<<fun(n);
}
```



