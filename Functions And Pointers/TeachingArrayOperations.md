# Teaching Array Operations
Operations that can be performed on arrays are
<br>
Finding the sum of elements in an array
<br>
Finding the mean of elements in an array
<br>
Finding the median of elements in an array
<br>
Write a program to perform the array operations mentioned above using pointer functions.

**Problem Requirements:**
<br>
int sum(int n, int * a)
<br>
int median(int n, int * a)
<br>
float mean(int n, int * a)

#### Input format :
Input consists of n+1 integers. The first integer corresponds to 'n' the size of the array. The next 'n' integers correspond to the elements of an array. Assume that the maximum value of n is 20 and 'n' is always odd.

#### Output format :
Output consists of 3 lines.
<br>
The first line consists of an integer which corresponds to the sum of the elements in an array.
<br>
The second line consists of a floating point number which corresponds to the mean of the array. Mean is displayed correct to decimal places.
<br>
The third line consists of an integer which corresponds to the median of the array.



**Sample test cases :<br>
Input 1 :<br>**
5<br>
1 2 4 5 3<br>
**Output 1 :<br>**
15<br>
3.00<br>
3

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<iomanip>
using namespace std;
int sum(int n,int *a)
{
    int sum=0,i;
    for(i=0;i<n;i++)
    {
        sum=sum+a[i];
    }
    return sum;
}
int median(int n,int *a)
{
    int i,j,temp=a[0];
    for(i=0;i<n;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if(a[i]>a[j]){temp=a[i];a[i]=a[j];a[j]=temp;}
        }
    }
    temp=n/2;
    return a[temp];
}
float mean(int n,int *a)
{
    float i;
    i=sum(n,a);
    return i/n;
}
int main()
{
    int i,n;
    cin>>n;
    int a[n];
    for(i=0;i<n;i++)
    {
        cin>>a[i];
    }
    cout<<sum(n,a)<<fixed<<setprecision(2)<<"\n"<<mean(n,a)<<"\n"<<median(n,a);
    return 0;
}
```



