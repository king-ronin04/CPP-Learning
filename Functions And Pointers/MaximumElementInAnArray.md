# Maximum Element in an Array

Sita has been promoted as a Team Leader and she has been shifted to Multimedia Team. As she needs to extensively work on audio, image and video signals, she is planning to spend a day in mastering the basics of 1-D and 2-D arrays. Can you please help her out?

Write a program to find the maximum element in an array. 

#### Input format :
Input consists of n+1 integers.
<br>
The first line of the input contains an integer corresponds to ‘n’ , the size of the array.
<br>
The next ‘n’ integers correspond to the elements in the array. Assume that the maximum value of n is 15.

#### Output format :
Output prints the maximum element in an array.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
20 10 30 15 22<br>
**Output 1 :<br>**
30


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include <iostream>
#include <algorithm> 
using namespace std; 
  
int main() 
{ 
    int n,i;
    cin>>n;
    int arr[n]; 
  for(i=0;i<n;i++)
  {
      cin>>arr[i];
  }
    cout<< *max_element(arr, arr + n); 
    return 0; 
} 
```



