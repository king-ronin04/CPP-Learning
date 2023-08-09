# Array of objects

Create an array of Employee objects. Also, add a provision for adding a new object to the array of Employee objects. Create an interactive console to get input from the user for performing actions on the array. Create a class Employee with the following public attributes:
<br>
id - as an Integer
<br>
name - as a String
<br>
salary - as Float
<br>
Create a method called display() to display the array of employee details.

In the Main method, obtain input from the console and call the display() function appropriately.

#### Input format :
Number of employee details
<br>
Id,Name and Salary separated by space

#### Output format :
Output prints the employee details

**Sample test cases :<br>
Input 1 :**
```
3
101 Ankit 10000
102  Sharma 20000
103 Dev 40000
```
**Output 1 :**
```
101  Ankit  10000
102  Sharma  20000
103  Dev  40000
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>  
using namespace std;  
class Employee {  
   public:  
       int id;      
       string name; 
       float salary;  
       public:
   void set_id(int digit) { id = digit; }
   int get_id() const { return id; }
   public:
   void set_salary(int sal) { salary = sal; }
   int get_salary() const { return salary; }
   public:
   void set_name(string n) { name = n; }
   string get_name() const { return name; }
       
       void display()    
        {    
            cout<<id<<"  "<<name<<"  "<<salary<<endl;    
        }    
};  
int main() {  
     
    int n,i;
    cin>>n;
    Employee e1[n];
    for(i=0;i<n;i++){
    cin>>e1[i].id>>e1[i].name>>e1[i].salary;
    e1[i].display();   
    }
      
    return 0;  
}  
```
