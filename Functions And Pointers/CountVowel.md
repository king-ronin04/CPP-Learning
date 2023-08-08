# Count vowel

In the Mini project 8th module is to find the number of vowel letters in a word(consider both uppercase and lowercase). Rita allotted this function to Patrick.
<br>
Help Patrick to write a program to find the number of vowel letters in a word.

**Function Specification:**<br>
int findNumberOfVowels(char);



#### Input format :
Input consists of a string

#### Output format :
Output consists of an integer saying the number of vowel in the given word.

**Sample test cases :<br>
Input 1 :<br>**
Alice<br>
**Output 1 :<br>**
3


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<cstdlib>
using namespace std;

int findNumberOfVowels(char *ptr)
{
    int i,count=0;
    for(i=0;i<30;i++)
    {
        switch(*(ptr+i))
        {
            case 97:count++;break;
            case 65:count++;break;
            case 69:count++;break;
            case 101:count++;break;
            case 73:count++;break;
            case 105:count++;break;
            case 79:count++;break;
            case 111:count++;break;
            case 85:count++;break;
            case 117:count++;break;
        }
        if(*(ptr+i)=='\0'){break;}
    }
    return count;
}
int main()
{
    int i;
    char *p=(char*)malloc(sizeof(char)*10);
    cin>>p;
    i=findNumberOfVowels(p);
    cout<<i;
    return 0;
}
```



