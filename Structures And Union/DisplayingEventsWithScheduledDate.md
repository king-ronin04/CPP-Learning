# Displaying Events with scheduled Date

Silver Bells is an organization with creative and innovative ideas working towards making every Event, and unforgettable experience. Agnes, the founder of the Company wanted to develop an Event Management System that would let its Clients plan and host events seamlessly. 
<br>
VMTech Software Solutions has tied up with Silver Bells to organize its annual event "Showtime!", an entertaining extravaganza with events like musical karaoke, fashion ramps, skits, etc., Agnes has appointed you to write a piece of code in the Event Management System that would help the company serve the requirements for this Corporate event. 

Write a program to create a structure named Date with three members i.e, day (int),  month (String), year(int). Create another structure named Event with five members i.e, name(String), type(String), duration(int in days), expenses (in lakhs, float)), scheduledDate (date). Below are the Date and Event structure:

struct Date
<br>
{
<br>
int day;
<br>
string month;
<br>
int year;
<br>
};

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
struct Date scheduledDate;
<br>
};

In the main method, get the details of an Event and display the details.

#### Input format :
First input should contain a string that gives the name of the Event.
<br>
Second input should contain a string that gives the type of the Event.
<br>
Third input should contain an integer that gives the duration of the Event.
<br>
Fourth input should contain a float value that gives the projected expenses of the Event.
<br>
Fifth line of the input contains the date.

#### Output format :
Output should display the Event name, Type, Duration and the projected expense separated by a space in first line.
<br>
The second line displays the date of the event.
<br>
Refer sample input and output for formatting specifications.

**Sample test cases :<br>
Input 1 :**
```
food fest 2017
public
3
5.7
12 August 2017
```
**Output 1 :**
```
food fest 2017 public 3 5.7L
12 August 2017
```
**Input 2 :**
```
book exhibition
private
2
8.2
18 September 2019
```
**Output 2 :**
```
book exhibition private 2 8.2L
18 September 2019
```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
#include<cstring>
using namespace std;
struct Date
{
int day;
string month;
int year;
};

struct Event
{
string name;
string type;
int duration;
float expenses;
struct Date scheduledDate;
};
int main()
{
   struct Event d;
   getline(cin,d.name);
   cin>>d.type>>d.duration>>d.expenses>>d.scheduledDate.day>>d.scheduledDate.month>>d.scheduledDate.year;
   cout<<d.name<<" "<<d.type<<" "<<d.duration<<" "<<d.expenses<<"L"<<"\n"<<d.scheduledDate.day<<" "<<d.scheduledDate.month<<" "<<d.scheduledDate.year;
   
    return 0;
}

```
