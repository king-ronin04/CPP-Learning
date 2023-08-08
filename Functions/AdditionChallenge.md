# Addition Challenge
 

Charlie set off with great zeal to the "Kracker Jack Fun Fair 2017". There were numerous activities in the fair, though Charlie being a Math expert, liked to participate in the Addition Challenge.

The Challenge given to him was to find S, where S=20 +21+22+...........+2N. He would succeed in his challenge if he manages to tell the answer for the problem before others. He requests your help to solve the problem in a flash.

Help Charlie to find S and win over the challenge.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/dde3c9a9-3d9d-40a7-807d-8cbd71bd0eff)


In the Main function, obtain input from the user in the console and display S by calling the findSum method 



#### Input format :
First line of the input contains one integer N (1 ≤ N ≤ 10000).

#### Output format :
Output S in a single line

**Sample test cases :<br>
Input 1 :<br>**
8<br>
**Output 1 :<br>**
511


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
unsigned long long int findSum(int n);
#include<cmath>
unsigned long long int findSum(int n)
{
    unsigned long long int s=0;int i;
    for(i=0;i<=n;i++)
    {
        s=s+pow(2,i);
    }
    return s;
}

int main()
{
    int n;
    cin>>n;
    cout<<findSum(n);
    return 0;
}

```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<math.h>
using namespace std;

int findSum(int n){
    long sum=0;
    for(int i=0;i<=n;i++){
        sum+=pow(2,i);
    }
    return sum;
    
}

int main(){
    int n;
    cin>>n;
    cout<<findSum(n);
    return 0;
}
```


