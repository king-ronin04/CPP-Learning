Create a dynamic integer array and print the sum over the array of each element * (array element index + 1)

#### Input format :
The first line of input consists of a positive integer n.
<br>
The next n lines of input consist of integers that are sequentially assigned to the each array element

#### Output format :
The sum over the array of each array element * (array element index + 1)

**Sample test cases :<br>
Input 1 :<br>**
5<br>
1 2 3 4 5<br>
**Output 1 :<br>**
55


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
	int i, n, sum = 0, count = 0;
	cin >> n;
	if (n < 0) {
		throw "input error";
	} else {
		int *a = new int[n];
		for (i = 0; i < n; i++) {
			cin >> a[i];
			sum = sum + (a[i] * (i + 1));
		}
		cout << sum;
	}
}

```
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;

int main(){
    int n;
    cin>>n;
    int *arr=new int[n];
    
    for(int i=0;i<n;i++){
        cin>>*(arr+i);
    }
    int sum=0;
    for(int i=1;i<=n;i++){
        sum=sum+((*(arr+(i-1)))*i);
    }
    cout<<sum;
    return 0;
}

```

