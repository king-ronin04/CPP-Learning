# Distance between 2 points  

Mrs. Anitha , our favourite Maths teacher wanted to teach her new batch of students to find the distance between 2 points.
<br>
Write a program to accept 2 points and to calculate distance between them using functions and pointers.

**Function Specification:<br>**
float distance(int *x1, int *y1, int *x2, int *y2)

This function returns the distance between two points.

#### Input format :
Input consists of 4 integers.
<br>
The first 2 integers refers to x and y coordinate of Point 1
<br>
The next 2 integers refers to x and y coordinate of Point 2



#### Output format :
Output consists of 1 float. Display the output correct to 2 decimal places.

**Sample test cases :<br>
Input 1 :<br>**
2 3<br>
4 1<br>
**Output 1 :<br>**
Distance between 2 points is 2.83


-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
#include<cmath>
#include<iomanip>
using namespace std;
float distance(int*x1,int*y1,int*x2,int*y2)
{
    return sqrt(pow(*x1-*x2,2)+pow(*y1-*y2,2));
}
int main()
{
    int x1,x2,y1,y2;
    cin>>x1>>y1;
    cin>>x2>>y2;
    cout<<fixed<<setprecision(2)<<"Distance between 2 points is "<<distance(&x1,&y1,&x2,&y2);
    return 0;
}
```


