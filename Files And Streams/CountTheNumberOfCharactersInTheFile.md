# Count the number of characters in the file
Write a program to create a file named "sample.txt".

Open the file and read the content to count the number of character in the file.

**Rule:**

The file name should be "sample.txt".

#### Input format :
The input file consists of characters.

#### Output format :
The output will be the integer which is number of characters in the file.



**Sample test cases :<br>
Input 1 :<br>**
Time is a great teacher but unfortunately it kills all its pupils<br>
**Output 1 :<br>**
Number of characters in file are 67

```cpp
#include<iostream>
#include <fstream>
using namespace std;

int main()
{
    ofstream fout;
    fout.open("sample.txt");
char str[300] = "Time is a great teacher but unfortunately it kills all its pupils\n";
    fout << str;
    fout.close();
    ifstream fin;
    fin.open("sample.txt");

    int count = 0;
    char ch; 

    while(!fin.eof())
    {
        fin.get(ch);
        count++;
    }
    
    cout << "Number of characters in file are " << count;
  fin.close();
    return 0;
}
```
