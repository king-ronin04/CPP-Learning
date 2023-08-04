# Count of Numbered Cells

Nurikabe logical game (sometimes called Islands in the Stream) is a binary determination puzzle. The puzzle is played on a typically rectangular grid of cells, some of which contain numbers. You must decide for each cell if it is white or black (by clicking on them) according to the following rules:

- All of the black cells must be connected.
- Each numbered cell must be part of a white island of connected white cells.
- Each island must have the same number of white cells as the number it contains (including the numbered cell).
- Two islands may not be connected.
- There cannot be any 2x2 blocks of black cells.

Unnumbered cells start out grey and cycle through white and black when clicked. Initially numbered cells are white in color.

#### Problem Statement:

Write a program to find the count of numbered cells, given a valid initial board configuration. Below figure is the sample valid initial configuration.

#### Input format :
First line of the input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a valid initial board configuration with N*N cells. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by the integer 20 in the matrix representation of the input configuration.



#### Output format :
Output should display an integer that gives the count of numbered cells, given a valid initial board configuration.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
20 20 1 20 3<br>
20 20 20 20 20<br>
20 20 20 20 20<br>
20 20 20 20 20<br>
6 20 3 20 20<br>
**Output 1 :<br>**
4



----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j,k=0;
    cin>>n;
    int a[n][n];
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            cin>>a[i][j];
            if(a[i][j]<11){k++;}
        }
    }
    cout<<k;
    return 0;
}


```
