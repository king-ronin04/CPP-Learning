# Most occurring element

An array is filled with one of the values 1, 2 or 3.
<br>
Find the value that occurs the most in the array.
<br>
If two or more values occur the most number of times print the lower value.

#### Input format :
First line of input contains an integer N, denoting the number of elements in the array.
<br>
Next line of input contains N values, each of which is either 1, 2 or 3.

#### Output format :
Print the minimum number of rooms that need to be painted in order to have all the rooms painted with same color i.e red, blue or green

**Sample test cases :<br>
Input 1 :<br>**
3<br>
1 2 1<br>
**Output 1 :<br>**
1

**Input 2 :<br>**
3<br>
1 2 3<br>
**Output 2 :<br>**
1


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;

int max(int a, int b)
{
	if (a > b) return a;
	return b;
}

int main()
{
	int n, i, c3, c2, c1;
	cin >> n;
	int *a = new int[n];
	for (i = 0; i < n; i++) {
		cin >> a[i];
	}
	c1 = 0; c2 = 0; c3 = 0;
	for (i = 0; i < n; i++) {
		switch (a[i]) {
		case 1:
			c1++;
			break;
		case 2:
			c2++;
			break;
		case 3:
			c3++;
			break;
		default:
			throw "invalid input";
			break;
		}
	}
	int count = max(max(c1, c2), c3);
	if (count == c1) cout << "1";
	else if (count == c2) cout << "2";
	else if (count == c3) cout << "3";

	return 0;
}

```

----------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
#include<map>
using namespace std;

int main(){
    int n;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++)
        cin>>arr[i];
        
    map<int,int> mp;
    for(int i=0;i<n;i++)
        mp[arr[i]]++;
    int maxi=-1;
    for(auto x:mp){
        if(maxi<x.second){
            maxi=x.second;
        }
    }
    
    for(auto x:mp){
        if(x.second==maxi)
        {
            cout<<x.first;
            break;
        }
    }
    return 0;
    
}

```


