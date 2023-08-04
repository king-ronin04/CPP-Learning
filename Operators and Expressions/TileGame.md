# Tile Game
 
In connection to the National Mathematics Day celebration, the Regional Mathematical Scholars Society 
had arranged for a Mathematics Challenge Event where school kids participated in large number. 
Many interesting math games were conducted, one such game that attracted most kids was the tile
game where the kids were given 'n' square tiles of the same size and were asked to form the largest possible square using those tiles.
 
Help the kids by writing a program to find the area of the largest possible square that can be formed, given the side of a square tile (in cms) and the number of square tiles available.

**Input format :** <br>
First line of the input is an integer that corresponds to the side of a square tile (in cms).<br>
Second line of the input is an integer that corresponds to the number of square tiles available.

**Output format :** <br>
Output should display the area of the largest possible square that can be formed (in square cms) with the available tiles.

**Sample test cases :**

**Input 1 :**<br>
5<br>
8

**Output 1 :** <br>
Area of the largest possible square is 100sqcm

----------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
#include<bits/stdc++.h>
using namespace std;
int main()
{
   int side,num_square,i=1,area,ans,largest_square;
 cin >>  side;
 cin >>  num_square;
int result = pow(2,i)*pow(2,i);
while(result<num_square)
{
    ans=result;
    i++;
    result=pow(2,i)*pow(2,i);
}
area=side*side;
largest_square=area*ans;
cout<<"\nArea of the largest possible square is "<< largest_square <<"sqcm";
return 0;
}


```
