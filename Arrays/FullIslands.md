# Full Islands

Nurikabe logical game (sometimes called Islands in the Stream) is a binary determination puzzle. The puzzle is played on a typically rectangular grid of cells, some of which contain numbers. You must decide for each cell if it is white or black (by clicking on them) according to the following rules:
- All of the black cells must be connected.
- Each numbered cell must be part of a white island of connected white cells.
- Each island must have the same number of white cells as the number it contains (including the numbered cell).
- Two islands may not be connected.
- There cannot be any 2x2 blocks of black cells.

Unnumbered cells start out grey and cycle through white and black when clicked. Initially numbered cells are white in color.

#### Problem Statement:

The step 1 of solving the puzzle is identifying "Full islands".

An island is full if it contains as many white cells as the number in the region. Any 1s are trivially full regions. When you encounter a full region, any cells that boarder it must be black. Here we show the cells that must be black due to a single celled white island.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/39f46bde-29ac-48f8-8745-7fc3b7913454)

Write a program that when given the initial board configuration will identify the full islands.

#### Input format :
First line of the input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a valid initial board configuration with N*N cells. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by the integer 20 in the matrix representation of the input configuration.



#### Output format :
Output should display the board configuration with N*N cells after applying step 1. Grey colored cells are represented by the integer 20, numbered cells are represented by the same number given in the input and black cells are represented by 0.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
20 20 1 20 3<br>
20 20 20 20 20<br>
20 20 20 20 20<br>
20 20 20 20 20<br>
6 20 3 20 20<br>
**Output 1 :<br>**
20 0 1 0 3 <br>
20 20 0 20 20 <br>
20 20 20 20 20 <br>
20 20 20 20 20 <br>
6 20 3 20 20 


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j;
    cin>>n;
    int a[n][n];
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            cin>>a[i][j];
        }
    }
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            if((a[i-1][j]==1)&&(i>0)){a[i][j]=0;}
            if((a[i+1][j]==1)&&(i<n-1)){a[i][j]=0;}
            if((a[i][j-1]==1)&&(j>0)){a[i][j]=0;}
            if((a[i][j+1]==1)&&(j<n-1)){a[i][j]=0;}
        }
    }
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            cout<<a[i][j]<<" ";
        }
        cout<<"\n";
    }
    return 0;
}

```
