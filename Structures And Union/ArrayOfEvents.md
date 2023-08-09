# Array of Events

Silver Bells is an organization with creative and innovative ideas working towards making every Event, and unforgettable experience. Agnes, the founder of the Company wanted to develop an Event Management System that would let its Clients plan and host events seamlessly.

The Company has signed up a big time Event Management deal for the biggest "Handloom and Handicrafts Expo" from the Central Division of Handlooms & Handicraft to promote, market and sale products produced by weavers and artisans across the country. The Expo will showcase various kinds of events like fashion show, product exhibition, traditional dance shows using the handicrafts, etc., Agnes has appointed you to write a piece of code in the Event Management System that would help the company serve this biggest Event.

Hence create a structure named Event with four members i.e, name(String), type(String), duration(int in days) and expenses (in lakhs, float). Below is the Event structure:

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

Write a program that will create an array of Events for the above structure Event. The program should contain a menu-driven main method with the following menus:
1) Display all Events
2) Search for an Event by name
3) List all events of a particular type
4) Display the details of the most expensive event

#### Input format :
The first line of the input consists of the value of n.
<br>
Next n inputs is the event name, event type, duration and expenses.
<br>
Next input is the choice.
<br>
If the selected choice requires any input, get it in the last line.

#### Output format :
Output is based on the selected choice. Refer sample output for formatting specifications.

**Sample test cases :<br>
Input 1 :<br>**
```
3
food fest
public
2
5.7
birthday party
private
1
1.22
seminars 2017
public
3
4.3
3
public
```
**Output 1 :<br>**
```
1. Display all events
2. Search for an event by name
3. List all the events of a particular type
4. Display the details of the most expensive event
food fest public 2 5.7L
seminars 2017 public 3 4.3L
```

**Input 2 :<br>**
```
3
food fest
public
2
5.7
birthday party
private
1
1.22
seminars 2017
public
3
4.3
2
birthday party
```
**Output 2 :<br>**
```
1. Display all events
2. Search for an event by name
3. List all the events of a particular type
4. Display the details of the most expensive event
birthday party private 1 1.22L
```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
#include<cstring>
#include<stdlib.h>

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
    int i,n,choice;
    cin>>n;
    struct Event e[n];
    for(i=0;i<n;i++) {
        cin.ignore();
        getline(cin,e[i].name);
        
        cin>>e[i].type;
        
        cin>>e[i].duration;
        cin>>e[i].expenses;
    }
    cout<<"1. Display all events\n";
    cout<<"2. Search for an event by name\n";
    cout<<"3. List all the events of a particular type\n";
    cout<<"4. Display the details of the most expensive event\n";
    cin>>choice;
    switch(choice) {
        case 1:
        for(i=0;i<n;i++) {
            cout<<e[i].name<<" "<<e[i].type<<" "<<e[i].duration<<" "<<e[i].expenses<<"L\n";
        }
        break;
        case 2: 
        {
        string name1;
        cin.ignore();
        getline(cin,name1);
        for(i=0;i<n;i++) {
            if((e[i].name.compare(name1))==0) {
                cout<<e[i].name<<" "<<e[i].type<<" "<<e[i].duration<<" "<<e[i].expenses<<"L\n";
            }
        }
        break;
        }
        case 3:
        {
        char type1[50];
        cin>>type1;
        for(i=0;i<n;i++) {
            if((e[i].type.compare(type1))==0) {
                cout<<e[i].name<<" "<<e[i].type<<" "<<e[i].duration<<" "<<e[i].expenses<<"L\n";
            }
        }
        break;
        }
        case 4:
        {
        float max = e[0].expenses;
        for(i=0;i<n;i++) {
            if(e[i].expenses>max) {
                max = e[i].expenses;
            }
        }
        for(i=0;i<n;i++) {
            if(e[i].expenses == max) {
                cout<<e[i].name<<" "<<e[i].type<<" "<<e[i].duration<<" "<<e[i].expenses<<"L\n";
            }
        }
        break;
        }
    }
    return 0;
}

```
