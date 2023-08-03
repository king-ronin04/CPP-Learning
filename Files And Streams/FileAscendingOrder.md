# File Ascending Order

Write a program to create a file with integer values and open the file in read mode to read the content of the file then sort the content of the file in ascending order.

**Rule:**

The input file name should be named as "sample.txt".



#### Input format :
Given the input as a file containing integer values.
<br>
First line of the input consists of the number of values to be entered.
<br>
Second line of input consists of the values that to be sorted

#### Output format :
Output consists of the sorted values

**Sample test cases :<br>
Input 1 :<br>**
5<br>
3 5 2 4 1<br>
**Output 1 :<br>**
1<br>
2<br>
3<br>
4<br>
5



---------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
#include <fstream>
using std::ofstream; 
using namespace std;
 
int main()
{
fstream file;
   file.open("sample.dat",ios::out);
   ofstream outdata;
   int i,j,n,a;
   cin>>n;
   int number[n];
 for (i=0; i<n; ++i)
 {
   cin>>number[i];
 }
 outdata.open("sample.dat"); 
for (i=0; i<n; ++i)
{
      outdata<<number[i]<<endl;
}
   outdata.close();
for (i = 0; i < n; i++)
    {
        for (j = 0; j < (n - i - 1); j++)
        {
            if (number[j] > number[j + 1])
            {
                a = number[j];
                number[j] = number[j + 1];
                number[j + 1] = a;
            }
        }
    }
 
        for (i = 0; i < n; i++) 
        {
            cout<<number[i]<<"\n";
        }
 file.close();
    return 0;
}



```
