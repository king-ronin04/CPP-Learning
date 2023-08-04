# Array with duplicate elements
An integer array with positive (> 0) elements is created where every element except one has a unique duplicate.
<br>
A given duplicate may occur more than once, for example in the array { 1, 2, 1, 2, 3, 2, 2} the element 2 occurs 4 times so there are 2 sets of unique duplicates. 
<br>
Find the only element without a unique duplicate.

#### Input format :
First line of the input contains the number of elements in the integer.
<br>
Second line of input contains N integers where every value occurs in pairs except one.

#### Output format :
Output in a single line the missing registration Id

**Sample test cases :<br>
Input 1 :<br>**
3<br>
1 2 1<br>
**Output 1 :<br>**
2

**Input 2 :<br>**
3<br>
1 1 1<br>
**Output 2 :<br>**
1



----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;

int main(){
    int n;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++)
        cin>>arr[i];
        
    int xorans=0;
    for(auto x:arr)
        xorans=xorans^x;
    cout<<xorans;
    return 0;
}
```
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;

int main()
{
	int n, i, j, k;
	cin >> n;
	if (n <= 0) throw "Invalid Input";
	int *a = new int[n];
	for (i = 0; i < n; i++) {
		cin >> a[i];
		if (a[i] <= 0) throw "Invalid Input";
	}
	int target = -1;
	bool found = false;
	for (i = 0; i < n; i++) {
		k = a[i];
		if (k == -1) continue;
		if (i == n - 1 && !found) {
			found = true;
			target = k;
			break;
		}
		a[i] = -1;
		for (j = i + 1; j < n; j++) {
			if (k == a[j]) { 
				a[j] = -1; 
				break;
			}
			if (j == n - 1) { 
				if (!found) {
					found = true;
					target = k;
				} else {
					throw "Invalid Input";
				}
			}
		}
	}
	if (found) {
		cout << target;
	} else {
		throw "Invalid Input";
	}
	return 0;
}


```

