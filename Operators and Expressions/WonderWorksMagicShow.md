# WonderWorks Magic Show

The Magic Castle, the home of the Academy of Magical Arts at California has organized the great ‘WonderWorks Magic Show’. 3 renowned magicians were invited to mystify and thrill the crowd with their world’s spectacular magic tricks. At the end of each of the 3 magicians’ shows, the audience were requested to give their feedback in a scale of 1 to 10. Number of people who watched each show and the average feedback rating of each show is known. Write a program to find the average feedback rating of the WonderWorks Magic show.

**Input format :** 

First line of the input is an integer value that corresponds to the number of people who watched show 1.<br>
Second line of the input is a float value that corresponds to the average rating of show 1.<br>
Third line of the input is an integer value that corresponds to the number of people who watched show 2.<br>
Fourth line of the input is a float value that corresponds to the average rating of show 2.<br>
Fifth line of the input is an integer value that corresponds to the number of people who watched show 3.<br>
Sixth line of the input is a float value that corresponds to the average rating of show 3.<br>

**Output format :**

Output should display the overall average rating for the show. Display the rating correct to 2 decimal places.

**Sample test cases :** <br>
**Input 1 :** <br>
100<br>
9.8<br>
400<br>
9.6<br>
500<br>
5<br>
**Output 1 :** <br>
7.32

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<bits/stdc++.h>
using namespace std;
int main()
{
  int show1,show2,show3;
  float rating1,rating2,rating3,tot,result;
   cin  >> show1;
  cin  >>rating1;
  cin  >>show2;
  cin  >>rating2;
  cin  >>show3;
  cin  >>rating3;
  tot=(show1*rating1)+(show2*rating2)+(show3*rating3);
  result=tot/(show1+show2+show3);
  cout<<fixed<<setprecision(2)<<result;
  return 0;
}


```
