# Enrolling the Events

Be it a concert, conference, corporate event or weddings, people have started to take interest in all kinds of events equally and actively. Silver Bells is an organization with creative and innovative ideas working towards making every Event, an unforgettable experience. Agnes, the founder of the Company wanted to develop an Event Management System that would let its Clients plan and host events seamlessly.

The primary requirement of the Event management System would be to enroll the details of any Event as given by the Clients. Agnes has assigned you the responsibility to write a program that will create a structure named Event with four members i.e, name(String), type(String), duration(int in days) and expenses (in lakhs, float). Below is the Event structure:

struct Event
<br>
{
<br>
string name;
<br>
string type;
<br>
int duration;
<br>
float expenses;
<br>
};

Your program should get the details of an Event and display the same in the main method. Can you accomplish the responsibility by following the requirements given?

#### Input format :
First input should contain a string that gives the name of the Event.
<br>
Second input should contain a string that gives the type of the Event.
<br>
Third input should contain an integer that gives the duration of the Event.
<br>
Fourth input should contain a float value that gives the projected expenses of the Event.



#### Output format :
Output should display the Event name, Type, Duration and the projected expense separated by a space.
<br>
Refer sample input and output for formatting specifications.

**Sample test cases :<br>
Input 1 :**
```
food fest 2017
public
3
5.7
```
**Output 1 :**
```
food fest 2017 public 3 5.7L
```
**Input 2 :**
```
book exhibition
public
2
3.2
```
**Output 2 :**
```
book exhibition public 2 3.2L
```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
#include<cstring>
using namespace std;
struct Event
{
string name;
string type;
int duration;
float expenses;
};
int main()
{
    struct Event e;
    getline(cin,e.name);
    cin>>e.type>>e.duration>>e.expenses;
    cout<<e.name<<" "<<e.type<<" "<<e.duration<<" "<<e.expenses<<"L";
    return 0;
}

```
