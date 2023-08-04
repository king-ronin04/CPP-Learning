# Rectangle's Area

An array is filled with positive integers.
<br>
If any set of 4 values can be picked up from this array representing the lengths of 4 sides of a rectangle, print the maximum possible area.
<br>
Or print -1 if a rectangle cannot be formed from the values given in the array.

#### Input format :
The first line of the input contains a single integer N denoting the number of elements in the array.
<br>
The second line of each test case contains N space-separated integers A1, A2, ...,AN denoting the lengths of sides

#### Output format :
Output a single line containing an integer representing the maximum possible area for rectangle or output -1, if it's impossible to form any rectangle using the available values.

**Sample test cases :<br>
Input 1 :<br>**
4<br>
3 2  3 2<br>
**Output 1 :<br>**
6

**Input 2 :<br>**
5<br>
2 3 4 3 2<br>
**Output 2 :<br>**
6


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;

void swap(int& a, int& b)
{
	int tmp = a;
	a = b;
	b = tmp;
}

bool bubble_sweep(int* arr, int n)
{
	bool sorted = true;
	for (int i = 0; i < n - 1; i++) {
		if (arr[i] > arr[i + 1]) {
			swap(arr[i], arr[i + 1]);
			sorted = false;
		}
	}
	return sorted;
}

typedef struct  {
	int l;
	int w;
	bool vaild;
} RECT_SIDES;

RECT_SIDES get_rect_sides(int* arr, int len, int sort_len)
{
	RECT_SIDES ret;
	ret.vaild = false;
	ret.l = ret.w = -1;
	for (int i = len - 1; i > len - sort_len; i--) {
		if (arr[i] == arr[i - 1]) {
			i--;
			if (ret.l == -1) {
				ret.l = arr[i];
			} else if (ret.w == -1) {
				ret.w = arr[i];
				ret.vaild = true;
				break;
			}
		}
	}
	return ret;
}

int main()
{
	int n, k = 2, l = 0;
	cin >> n;
	if (n <= 0) throw "Invalid Input";
	int *a = new int[n];
	for (int i = 0; i < n; i++) {
		cin >> a[i];
	}
	RECT_SIDES ret;
	ret.vaild = false;
	bool sorted = false;
	for (int i = 0; i < n; i++) {
		if (!sorted) sorted = bubble_sweep(a, n - i);
		if (i >= 3 && (ret = get_rect_sides(a, n, i + 1)).vaild) {
			break;
		}
	}
	if (ret.vaild) {
		cout << ret.l * ret.w;
	} else {
		cout << "-1";
	}
	return 0;
}

```
