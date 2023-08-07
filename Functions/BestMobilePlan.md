# Best Mobile Plan
St. Patrick Convent organizes a project exhibition "Innovative Minds" every year with an objective to provide the platform and unleash the potential of the students by showcasing their innovative projects.

Albert is a science expert and is a topper at his high school. He became interested about the project exhibition and enrolled his name for the same.

Albert’s Dad has a cell phone but often seemed to worry about the price plans for his phone that best fits for his usage pattern and monthly expenses. There are two options, each plan has different costs for daytime minutes, evening minutes and weekend minutes.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/225ff2a9-5390-412e-a1cd-338c8ab4b7db)


Having this as a spark for his project, Albert decided to design a handy application that will input the number of each type of minutes and output the cheapest plan for this usage pattern,using the format shown below. In the case that the two plans are the same price, output both plans.

He needs your help to evaluate his project and suggest corrections.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/a3ab99bd-f3b1-4177-8a0c-ccebaff6d4a3)


In the Main function, obtain input from the user in the console and call the printPlanDetails method 



#### Input format :
First line of the input is an integer that gives the usage during the daytime in minutes.
<br>
Second line of the input is an integer that gives usage during the evening in minutes.
<br>
Third line of the input is an integer that gives usage during the night in minutes.

#### Output format :
Output should print the cheapest plan for this usage pattern. In the case that the two plans are the same price, output both plans

**Sample test cases :<br>
Input 1 :<br>**
251<br>
10<br>
60<br>
**Output 1 :<br>**
Plan A costs 51.25<br>
Plan B costs 18.95<br>
Plan B is cheapest


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<iomanip>
using namespace std;
void printPlanDetails(int d,int e,int n);
void printPlanDetails(int d,int e,int n)
{
    float a=0,b=0;
    if(d>100){a=(d-100)*0.25;}
    if(d>250){b=(d-250)*0.45;}
    a=a+(e*0.15)+(n*0.2);
    b=b+(e*0.35)+(n*0.25);
    cout<<fixed<<setprecision(2)<<"Plan A costs "<<a<<"\nPlan B costs "<<b<<"\n";
    if(a==b){cout<<"Plan A and B are the same price";}
    else
    {(a<b)?cout<<"Plan A is cheapest":cout<<"Plan B is cheapest";}
}
int main()
{
    int daytime,evening,night;
    cin>>daytime>>evening>>night;
    printPlanDetails(daytime,evening,night);
    return 0;
}

```
