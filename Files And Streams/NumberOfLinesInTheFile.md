# Number Of Lines in the file

Write the program to create a file "sample.txt" . Open the file and read the content to count the number of lines .


**Rule:**

The file name should be sample.txt.

#### Input format :
Give the input as a text file .

#### Output format :
The output will be the integer which is number of lines in the file.

**Sample test cases :<br>
Input 1 :<br>**
Today C++ is the most widely used System Programming Language.<br>
Most of the state of the art software have been implemented using C++.<br>
Easy to learn<br>
Structured language<br>
It produces efficient programs.<br>
It can handle low-level activities.<br>
It can be compiled on a variety of computers.<br>
**Output 1 :<br>**

File content: Today C++ is the most widely used System Programming Language.<br>
Most of the state of the art software have been implemented using C++.<br>
Easy to learn<br>
Structured language<br>
It produces efficient programs.<br>
It can handle low-level activities.<br>
It can be compiled on a variety of computers.<br>
Numbers of lines in the file : 7


---------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
#include <fstream>
using std::ofstream;
using std::ifstream;
using namespace std;
 
int main() 
{
    fstream file;
file.open("sample.txt",ios::out);
   ofstream outdata;
   int count=0;
   string str="Today C++ is the most widely used System Programming Language.\nMost of the state of the art software have been implemented using C++.\nEasy to learn\nStructured language\nIt produces efficient programs.\nIt can handle low-level activities.\nIt can be compiled on a variety of computers.";
   string line;
   
  outdata.open("sample.txt"); 
      outdata << str << endl;
   outdata.close();
   cout<<"\nFile content: ";
    
   while(!file.eof())
   {
       file>>str; 
       cout<<str;
   }
   ifstream ifile("sample.txt");
    while (getline(ifile, line))
    {
        count++;
    }
    cout << "\nNumbers of lines in the file : " << count << endl;
    file.close();
    ifile.close();
   
   return 0 ;
}





```
