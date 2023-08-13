# Input Mismatch Exception

Input Mismatch exception occurs when an input of different datatype is given other than the required. In common practice, it occurs when String or double datatype is given for an int datatype. Let's handle this exception for practice. Obtain int type input from the user. Display the obtained input if no exception occurs. If an exception occurs, prompt the user as specified in Sample I/O. In the Main method, obtain integer input from the user and perform actions as specified above

#### Input format :
Input consist of an integer

#### Output format :
Refer sample output

**Sample test cases :<br>
Input 1 :** <br>
10<br>
**Output 1 :<br>**
10

**Input 2 :<br>**
hello<br>
**Output 2 :<br>**
Input mismatch Exception occured while reading the value




-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
#include <exception>
using namespace std;

int main() {
      int number;
                 cin >> number;
          try {
              if(number!=0)
                  cout<<number;
                else
                    throw 0;
          } catch (int e) {
                  cout << "Input mismatch Exception occured while reading the value" ;
          }
          
            return 0;
}

```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include<iostream>
#include<stdexcept>
using namespace std;
int main() {
  int n;
  std::cin.exceptions(std::istream::failbit | std::istream::badbit);
  try {
    std::cin >> n;
    cout<<n;
  } catch(istream::failure) {
    std::cout << "Input mismatch Exception occured while reading the value" << std::endl;
  }
  return 0;
}
```
		
