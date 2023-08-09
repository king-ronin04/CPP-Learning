# Array of Events with scheduled Date

Silver Bells is an organization with creative and innovative ideas working towards making every Event, and unforgettable experience. Agnes, the founder of the Company wanted to develop an Event Management System that would let its Clients plan and host events seamlessly. 
<br>
The Company has signed up a big time Event Management deal for the biggest “Handloom and Handicrafts Expo” from the Central Division of Handlooms & Handicraft to promote, market and sale products produced by weavers and artisans across the country. The Expo will showcase various kinds of events like fashion show, product exhibition, traditional dance shows using the handicrafts, etc., Agnes has appointed you to write a piece of code in the Event Management System that would help the company serve this biggest Event. 
<br>
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

In the main method, create an array of Events for the structure Event and get the details of all events and should contain a menu-driven main method with the following menus:

1) Display all Events
2) Display all Events scheduled in a specific month
3) Display all Events scheduled on a specific date

#### Input format :
The first line of the input consists of the value of n.
<br>
Next input is the event details.
<br>
Next input is the choice.
<br>
If the choice requires further input, Input it in the next line.

#### Output format :
The output prints the event details based on the choice. Refer sample input and output.

**Sample test cases :<br>
Input 1 :**
```
3
food fest
public
5
5.2
10 June 2014
seminar
private
8
8.6
18 September 2020
birthday party
public
7
7.2
26 June 2015
1
```
**Output 1 :**
```
1. Display all the events
2. Display the events on a specific month
3. Display the events on a specific date
food fest public 5 5.2
10 June 2014
seminar private 8 8.6
18 September 2020
birthday party public 7 7.2
26 June 2015
```
**Input 2 :**
```
3
food fest
public
5
5.2
10 June 2014
seminar
private
8
8.6
18 September 2020
birthday party
public
7
7.2
26 July 2015
2
September
```
**Output 2 :**
```
1. Display all the events
2. Display the events on a specific month
3. Display the events on a specific date
seminar private 8 8.6
18 September 2020
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
    int i,n,choice;
    cin>>n;
    struct Event e[n];
    for(i=0;i<n;i++) {
        cin.ignore();
        getline(cin,e[i].name);
        cin>>e[i].type>>e[i].duration>>e[i].expenses>>e[i].scheduledDate.day>>e[i].scheduledDate.month>>e[i].scheduledDate.year;
    }
    cin>>choice;
    cout<<"1. Display all the events\n";
    cout<<"2. Display the events on a specific month\n";
    cout<<"3. Display the events on a specific date\n";
    switch(choice) {
        case 1:
        for(i=0;i<n;i++) {
            cout<<e[i].name<<" "<<e[i].type<<" "<<e[i].duration<<" "<<e[i].expenses<<"\n";
            cout<<e[i].scheduledDate.day<<" "<<e[i].scheduledDate.month<<" "<<e[i].scheduledDate.year<<"\n";
        }
        break;
        case 2:
        {
            string m1;
            cin>>m1;
        for(i=0;i<n;i++) {
            if(e[i].scheduledDate.month.compare(m1) == 0) {
                cout<<e[i].name<<" "<<e[i].type<<" "<<e[i].duration<<" "<<e[i].expenses<<"\n";
                cout<<e[i].scheduledDate.day<<" "<<e[i].scheduledDate.month<<" "<<e[i].scheduledDate.year<<"\n";
            } 
        }
        break;
        }
        case 3:
        {
            int d1;
            cin>>d1;
            for(i=0;i<n;i++) {
                if(e[i].scheduledDate.day == d1) {
                    cout<<e[i].name<<" "<<e[i].type<<" "<<e[i].duration<<" "<<e[i].expenses<<"\n";
                    cout<<e[i].scheduledDate.day<<" "<<e[i].scheduledDate.month<<" "<<e[i].scheduledDate.year<<"\n";
                }
            }
            break;
        }
    }
    
    return 0;
}

```
