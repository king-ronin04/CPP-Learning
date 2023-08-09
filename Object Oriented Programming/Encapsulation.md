# Encapsulation

The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. To achieve this, you must declare class variables/attributes as private (cannot be accessed from outside the class). If you want others to read or modify the value of a private member, you can provide public get and set methods.

Consider the following attribute to display the salary of an employee
<br>
salary as integer
<br>
Obtain the input from the user and display it on the console.

#### Input format :
Input consist of an integer

#### Output format :
Output prints the integer

**Sample test cases :<br>
Input 1 :** <br>
10000 <br>
**Output 1 :<br>**
10000


-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>
using namespace std;

class Employee {
  private:
    
    int salary;

  public:
    
    void setSalary(int s) {
      salary = s;
    }
    
    int getSalary() {
      return salary;
    }
};

int main() {
  Employee myObj;
  int salary;
  cin>>salary;
  myObj.setSalary(salary);
  cout << myObj.getSalary();
  return 0;
}
```
