# Count no of vowels- Files



Write a program to read the content from the file(sample.txt) and count number of vowels.

**Rules:**

The input file should be named as "sample.txt".The input file should be named as "sample.txt".



#### Input format :
Input consists of characters

#### Output format :
Output prints the number of vowels in the text

**Sample test cases :<br>
Input 1 :<br>**
Time is a great teacher but unfortunately it kills all its pupils<br>
**Output 1 :<br>**
Number of vowels in file are 21


---------------------------------------------------------------------------------------------------------------------------------------------------------------


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
        if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U')
        count++;
    }
    
    cout << "Number of vowels in file are " << count;

fin.close();
    return 0;
}




```
