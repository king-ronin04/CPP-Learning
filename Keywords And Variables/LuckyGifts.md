# Lucky Gifts
"Planet Kids Entertainment Fair" is back to delight kids and parents. The Fair will have non-stop entertainment with an extravaganza of games, exciting rides, sports, art & crafts, role-plays, inspiring competitions, prizes & gifts, and yummy food.

Few lucky attendees at the Fair will be given a pack of candies as a lucky gift and the show coordinator has assigned you the task for choosing the number of attendees who will receive the pack of candies. There are 'N' candies available and you need to decide how many candies to place in each pack. Each pack must contain the same number of candies. You should choose an integer A between 1 and N, inclusive, and place exactly A candies into each pack. You should make as many packs as possible but since you enjoy eating candies very much, you eat the remaining candies. 

Write a program that will calculate the pack size(A) so that you can eat as many candies as possible. If multiple pack size will result in the same number of leftover candies, then print the largest pack size.

#### Input format :
The first and only line of input contains an integer N

#### Output format :
Output a single line that gives the pack size that will maximize the number of leftover candies

**Sample test cases :<br>
Input 1 :** <br>
5 <br>
**Output 1 :** <br>
3

---------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
  int tot_candy;
cin  >> tot_candy;
tot_candy=(tot_candy/2)+1;
cout <<tot_candy;
return 0;
}


```
