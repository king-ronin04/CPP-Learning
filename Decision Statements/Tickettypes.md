# Ticket types
The Magic Castle, the home of the Academy of Magical Arts at California has organized the great 'Wonder Works Magic Show'. Renowned magicians were invited to mystify and thrill the crowd with their world’s spectacular magic tricks. The Ticket booking for the show started 2 days prior and there were different types of tickets offered with different fare. The show organizers wanted to place a scanning machine at the entrance of the venue for scrutiny. The machine will take the input of a character denoting the various ticket types and displays the equivalent ticket type of the given character.

There are 5 types of tickets, each of which is denoted by a character (both upper case and lower case). Please find the equivalent strings for the characters.
<br>
E or e - Early Bird Ticket
<br>
D or d - Discount Ticket
<br>
V or v - VIP Ticket
<br>
S or s - Standard Ticket
<br>
C or c - Child Ticket
<br>
Write a piece of code for the scanning machine that will take the input of a character and print the equivalent string as given
#### Input format :
The first line of the input is one of the character that denotes one of ticket types

#### Output format :
Output should display the equivalent ticket type of the character.

**Sample test cases :<br>
Input 1 :** <br>
c<br>
**Output 1 :** <br>
Child Ticket

---------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include <iostream>
using namespace std;
int main()
{
    char ticket;
    cin>>ticket;
   switch(ticket)
   {
       case 'E':cout<<"Early Bird Ticket";
       break;
       case 'e':cout<<"Early Bird Ticket";
       break;
       case 'D':cout<<"Discount Ticket";
       break;
       case 'd':cout<<"Discount Ticket";
       break;
       case 'V':cout<<"VIP Ticket";
       break;
       case 'v':cout<<"VIP Ticket";
       break;
       case 'S':cout<<"Standard Ticket";
       break;
       case 's':cout<<"Standard Ticket";
       break;
       case 'C':cout<<"Child Ticket";
       break;
       case 'c':cout<<"Child Ticket";
       break;
   }
    return 0;
}


```
