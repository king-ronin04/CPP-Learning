# Sum of the Integers in the file

Create a input file "sample.txt" with integer values. Write a program to Open the file and read the content to find the sum of all values in the file.


**Rule:**

The file name should be sample.txt.

#### Input format :
Give the input as a file which contains the integer values.
<br>
First line of the input consists of number of values to be given.
<br>
Second line of the input consists of the numbers.

#### Output format :
The output will be the integer which is sum of the integers

**Sample test cases :<br>
Input 1 :<br>**
5<br>
1 2 3 4 5<br>
**Output 1 :<br>**
15

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
int i,n,sum=0;
   cin>>n;
   int num[n];
 for (i=0; i<n; ++i)
 {
   cin>>num[i];
 }
 for(i=0;i<n;i++)
 {
 sum=sum+num[i];
 }
 cout<<sum;
 outdata.open("sample.dat"); 
for (i=0; i<n; ++i)
      outdata << num[i] << endl;
 outdata.close();
file.close();
    
   return 0;
}

```
