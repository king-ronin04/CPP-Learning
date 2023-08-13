Write a program to display the marks obtained by a student in Physics,Chemistry and Mathematics for calculating cut-off marks.The maximum marks a student can score in subject is 100.Handle the exception if the mark entered by the student is above 100 or below 0. Obtain inputs from the user and display the output in the console.

#### Input format :
First line of the input consist of a string
<br>
Next input is the marks

#### Output format :
Refer sample output

**Sample test cases :<br>
Input 1 :**
```
Ankit
99
89
75
```
**Output 1 :**
```
99
89
75
```

**Input 2 :**
```
Sharma
126
33
89
```
**Output 2 :**
```
Invalid Marks
```




-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include<iostream>
using namespace std;
int main()
{
	int p,c,m,err=0;
	string name;
	
	
		try 
		{
			
			cin>>name;
			cin>>p;
			
			if(!(p>=0 && p<=100)) 
			{
				throw(p); 
			}
			
			cin>>c;
			
			if(!(c>=0 && c<=100)) 
			{
				throw(c); 
			}
			
			cin>>m;
			
			if(!(m>=0 && m<=100)) 
			{
				throw(m); 
			}
			
			err=0; 
				cout<<p<<"\n"<<c<<"\n"<<m;
		}
	
		catch(int e)
		{
			cout<<"Invalid Marks"<<endl; 
			err=1; 
		}

	 
}

```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------



```cpp
#include <iostream>

using namespace std;

class InvalidMarkException
{

public:
  InvalidMarkException (string message)
  {
    this->message = message;
  }

  string getMessage ()
  {
    return message;
  }

private:
  string message;
};

int
main ()
{
  string name;
  int physics, chemistry, mathematics;


  cin >> name;


  cin >> physics >> chemistry >> mathematics;

  try
  {
    if (physics > 100 || physics < 0)
      {
	throw InvalidMarkException ("Invalid Marks");
      }
    else if (chemistry > 100 || chemistry < 0)
      {
	throw InvalidMarkException ("Invalid Marks");

      }
    else if (mathematics > 100 || mathematics < 0)
      {
	throw InvalidMarkException ("Invalid Marks");

      }
    else
      {

	cout << physics << endl;
	cout << chemistry << endl;
	cout << mathematics << endl;
      }
  }
  catch (InvalidMarkException e)
  {
    cout << e.getMessage () << endl;
  }

  return 0;
}

```
		
