# Arithmetic Exception

An exception is an unwanted or unexpected event, which occurs during the execution of a program i.e at runtime, it disrupts the normal flow of the program. For example, there are 10 statements in your program and there occurs an exception at statement 5, rest of the code will not be executed i.e. statement 6 to 10 will not run. If we perform exception handling, rest of the statement will be executed. That is why we use exception handling.

For practice in exception handling, obtain the cost for 'n' days of an item and n as input and calculate the cost per day for the item. In case, zero is given as input for n, an arithmetic exception is thrown, handle the exception and prompt the user accordingly (Refer sample I/O).

In the Main method, obtain input from the user and store the values in int type. Handle exception if one occurs.

#### Input format :
First line of the input consist of the cost of item for n days
<br>
Second line of the input consist of value of n

#### Output format :
Output prints the cost per day of the item

**Sample test cases :<br>
Input 1 :<br>**
100<br>
0<br>
**Output 1 :<br>**
Cannot divide by zero

**Input 2 :<br>**
100<br>
20<br>
**Output 2 :<br>**
5




-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
#include<exception>
using namespace std;

int main(){
		int cost,noOfDays;
		cin>>cost;
		cin>>noOfDays;
		try{
		    if(noOfDays==0)
		    throw runtime_error("Cannot divide by zero");
		
		int result = cost/noOfDays;
		cout<<result;
	   }
	catch(runtime_error &e) {
		cout<<e.what();
	}

}
```
		
-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
using namespace std;

int main() {
      int cost, noOfDays;
        cin >> cost >> noOfDays;
        
          try {
                if(noOfDays==0){
                    throw noOfDays;
                }
                  int result = cost / noOfDays;
                      cout << result << std::endl;
          } catch (int e) {
                  cout << "Cannot divide by zero";
          }
          
            return 0;
}

```
		
