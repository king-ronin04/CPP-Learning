# Building

Create a structure called Building. 

struct Building
<br>
{
<br>
char name[100];
<br>
double length;
<br>
double width;
<br>
double height;
<br>
double ratePerSqFt;
<br>
};

Write a program to get the details of 'n' buildings  and to display the name, area and value of each building.
<br>
Length, width and height of the building are given in feet. The area and the value of the building is calculated and displayed in the output.

#### Input format :
The first line of the input consists of the value of n.
<br>
Next input is the n building details.

#### Output format :
The output prints the name, area and value separated by a space.

**Sample test cases :<br>
Input 1 :**
```
3 
srivatsa 200 150 10 650.5
vaishnavi 1050.5 700 12 800
zebra 2000 1300 12 1000
```
**Output 1 :**
```
srivatsa 30000.00 19515000.00
vaishnavi 735350.00 588280000.00
zebra 2600000.00 2600000000.00
```


-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
#include<cstring>
#include<bits/stdc++.h>
using namespace std;
struct Building
{
char name[100];
double length;
double width;
double height;
double ratePerSqFt;
};
int main()
{
  int n,i;
  cin>>n;
  struct Building b[n];
  double area[n],value[n];
  for(i=0;i<n;i++) {
      cin>>b[i].name>>b[i].length>>b[i].width>>b[i].height>>b[i].ratePerSqFt;
  }
  for(i=0;i<n;i++) {
      area[i] = b[i].length*b[i].width;
      value[i] = area[i]*b[i].ratePerSqFt;
  }
  for(i=0;i<n;i++){
      cout<<b[i].name<<" ";
      cout<<fixed<<setprecision(2)<<area[i]<<" ";
      cout<<fixed<<setprecision(2)<<value[i]<<"\n";
  }
    return 0;
}

```
