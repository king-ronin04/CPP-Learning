# Compare 2 arrays

Write a program to find whether 2 arrays are contains the same element in same index position.



#### Input format :
Input consists of 2n+1 integers. The first integer corresponds to ‘n’ , the size of the array. The next ‘n’ integers correspond to the elements in the first array. The next ‘n’ integers correspond to the elements in the second array.Assume that the maximum value of n is 15.

#### Output format :
Print yes if the 2 arrays are the same. Print no if the 2 arrays are different

**Sample test cases :<br>
Input 1 :<br>**
5<br>
2 3 6 5 4<br>
2 3 6 5 4<br>
**Output 1 :<br>**
yes


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```cpp
#include<iostream>
#include<cstdlib>
using namespace std;
int main()
{
    int n,i;
    cin>>n;
    int *ptr1=(int*)malloc(n*sizeof(int));
    int *ptr2=(int*)malloc(n*sizeof(int));
    for(int i=0;i<n;i++)
{
    cin>>*(ptr1+i) ;
}

for(int i=0;i<n;i++)
{
    cin>>*(ptr2+i);
}
    /*for(i=0;i<(2*n);i++)
    {
        cin >> *p+i>> endl;
    }*/
    for(i=0;i<n;i++)
    {
        if(*(ptr1+i)!=(*(ptr2+i))){cout<<"no";break;}
        if(i==n-1){cout<<"yes";}
    }
    return 0;
}
```


