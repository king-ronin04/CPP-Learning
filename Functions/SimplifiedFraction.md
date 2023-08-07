# Simplified Fraction

 

St. Patrick Convent organizes a project exhibition "Innovative Minds" every year with an objective to provide the platform and unleash the potential of the students by showcasing their innovative projects. Pasha is a smart high school student and was eager to participate in the fair for the first time.

 

After a lot of ground works, she decided her project and set out to design the same. Her project requirement was to design an advanced calculator that has a fraction feature that will simplify fractions. The project will accept a non-negative integer as a numerator and a positive integer as a denominator and outputs the fraction in simplest form. That is, the fraction cannot be reduced any further, and the numerator will be less than the denominator.

 

Help Pasha to program her advanced calculator and succeed in her first ever project presentation. You can assume that all input numerators and denominators will produce valid fractions.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/6409264b-a3f5-4a10-bd31-421a6b0e3c07)


In the Main function, obtain input from the user in the console and call the printValue method 



#### Input format :
First line of the input is a non-negative integer which is the numerator in the fraction.
<br>
Second line of the input is a positive integer which is the denominator in the fraction.

#### Output format :
Output the simplified form of the fraction in a single line.

**Sample test cases :<br>
Input 1 :<br>**
20<br>
4<br>
**Output 1 :<br>**
5


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
void printValue(int a,int b);
void printValue(int a,int b)
{
    int i;
    if((a>=b)||(a==0)){cout<<a/b;}
    for(i=2;i<=a/2;i++)
    {
        if((a%i==0)&&(b%i==0)){a=a/i;b=b/i;i=1;}
    }
    if(a%b!=0)
    {
        cout<<" "<<a%b<<"/"<<b;
    }
}

int main()
{
    int divisor,dividend;
    cin>>dividend>>divisor;
    printValue(dividend,divisor);
    return 0;
}
```

