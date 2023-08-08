# Triangle

We have triangles made of wodden blocks. The topmost row has 1 block, the next row down has 2 blocks, the next row has 3 blocks, and so on. Compute recursively (no loops or multiplication) the total number of blocks in such an arrangement of triangles with the given number of rows.
<br>
For example,<br>
    triangle(2) → 3

**Function specification:** <br>
int triangle(int n)



#### Input format :
Input consists of a single integer corresponding to the number of triangles

#### Output format :
The output consists of a single integer corresponding to the total number of blocks

**Sample test cases :<br>
Input 1 :<br>**
2<br>
**Output 1 :<br>**
3



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int triangle(int n) {
		if(n == 0) {
			return 0;
		}
		if(n == 1) {
			return 1;
		}
		else {
			return n+triangle(n-1);
		}
}
int main()
{
	    int n;
		cin>>n;
		cout<<triangle(n);
    return 0;
	}

```





