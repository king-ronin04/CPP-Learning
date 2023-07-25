# Co-Partners in Train
Tim and Bob are off to a famous Education Fair "Knowledge Forum 2017" at Uzhlanda. This time they have to travel without their guardians. Tim got very interested in the arrangement of seats inside the train coach.
<br>
The entire coach could be viewed as an arrangement of consecutive blocks of size 8. 

BerthNumber Compartment
<br>
1-8 1
<br>
9-16 2
<br>
17-24 3
<br>
... and so on

 Each of these size-8 blocks are further arranged as:
<br>
 1LB, 2MB, 3UB, 4LB, 5MB, 6UB, 7SL, 8SU
<br>
 9LB, 10MB, ...
<br>
.......
<br>
.......

Here LB denotes lower berth, MB middle berth and UB upper berth.
<br>
The following berths are called Co-Partners in Train:
<br>
3 UB 6 UB
<br>
2 MB 5 MB
<br>
1 LB 4 LB
<br>
7 SL 8 SU
<br>
and the pattern is repeated for every set of 8 berths. 
<br>
Tim and Bob are playing this game of finding the co-partner in train of each berth. Write a program to do the same.

#### Input format :
The input consists of an integer N, which corresponds to the berth number whose neighbor is to be found out.

#### Output format :
The output is to display the berth of the neighbor of the corresponding seat.

**Sample test cases :<br>
Input 1 :** <br>
1 <br>
**Output 1 :** <br>
4LB <br>

**Input 2 :** <br>
5 <br>
**Output 2 :** <br>
2MB 

**Input 3 :** <br>
3 <br>
**Output 3 :** <br>
6UB 

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int a,count;
    cin>>a;
    count=a%8;
    if(count==0){ a=a-1;}
    else if(count<4){a=a+3;}
    else if(count<7){a=a-3;}
    else if(count==7){a=a+1;}
    switch(count)
    {
        case 0:cout<<a<<"SL";break;
        case 1:cout<<a<<"LB";break;
        case 2:cout<<a<<"MB";break;
        case 3:cout<<a<<"UB";break;
        case 4:cout<<a<<"LB";break;
        case 5:cout<<a<<"MB";break;
        case 6:cout<<a<<"UB";break;
        case 7:cout<<a<<"SU";break;
    }
    return 0;
}


```
