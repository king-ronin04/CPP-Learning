# Team Event
Super Quiz Bee is a famous quiz Competition that tests students on a wide variety of academic subjects. This week’s competition was a Team event and students who register for the event will be given a unique registration code N. The participants are teamed into 10 teams and the team to which a participant is assigned to depends on the absolute difference between the first and last digit in the registration code.

The event organizers wanted your help in writing an automated program that will ease their job of assigning teams to the participants. If the registration number given is less than 10, then the program should display "Invalid Input".

#### Input format :
The only line of input contains an integer N.

#### Output format :
Output the absolute difference between the first and last digit of N.

**Sample test cases :<br>
Input 1 :** <br>
345<br>
**Output 1 :** <br>
2<br>

**Input 2 :** <br>
9 <br>
**Output 2 :** <br>
Invalid Input


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
using namespace std;
int main()
{
    int num,n,i,l;
    cin>>num;
    if(num>=10)
    {
      n=num%10;
      l=num;
      for(i=0;num>0;i++)
      {
          num=num/10;
          if(num>0){l=num;}
      }
      (l>=n)?cout<<l-n:cout<<n-l;
    }
    else
    {
        cout<<"Invalid Input";
    }
}


```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<math.h>
using namespace std;
int first(int n){
    int c=(int)log10(n);
    n=(int)(n/(int)(pow(10,c)));
    return n;
}

int last(int n){
    return n%10;
}
int main(){
    int n;
    cin>>n;
    if(n<10){
        cout<<"Invalid Input";
    }
    else if(n>=10)
    cout<<abs(first(n)-last(n)); 
    return 0;
}

```
