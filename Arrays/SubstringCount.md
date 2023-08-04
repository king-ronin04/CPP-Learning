# Substring count
Given an array A1, A2, ..., AN, count the number of subarrays of array A which are non-decreasing.
<br>
A subarrayA[i, j], where 1 ≤ i ≤ j ≤ N is a sequence of integers Ai, Ai+1, ..., Aj.
<br>
A subarrayA[i, j] is non-decreasing if Ai ≤ Ai+1 ≤ Ai+2 ≤ ... ≤ Aj. Count the total number of such subarrays.

Refer hint.

#### Input format :
The first line of input contains a single integer N denoting the size of array.
<br>
The second line contains N space-separated integers A1, A2, ...,AN denoting the elements of the array.

#### Output format :
Output in a single line, the count of the total number of such sub arrays.

**Sample test cases :<br>
Input 1 :<br>**
4<br>
1 4 2 3<br>
**Output 1 :<br>**
6



----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;

int main()
{
	int n, i, j = 0, k = 0;
	cin >> n;
	int *a = new int[n];
	for (i = 0; i < n; i++) {
		cin >> a[i];
	}
	for (i = 0; i < n - 1; i++) {
		if (a[i] <= a[i + 1]) 
		{ 
			j++; 
		} else { 
			k = k + (j * (j + 1) / 2); 
			j = 0; 
		}
	}
	k = k + (j * (j + 1) / 2);
	cout << k + n;
	return 0;
}

```
