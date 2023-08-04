# Single Expansion Route

Nurikabe logical game (sometimes called Islands in the Stream) is a binary determination puzzle. The puzzle is played on a typically rectangular grid of cells, some of which contain numbers. You must decide for each cell if it is white or black (by clicking on them) according to the following rules:
- All of the black cells must be connected.
- Each numbered cell must be part of a white island of connected white cells.
- Each island must have the same number of white cells as the number it contains (including the numbered cell).
- Two islands may not be connected.
- There cannot be any 2x2 blocks of black cells.

Unnumbered cells start out grey and cycle through white and black when clicked. Initially numbered cells are white in color.

#### Problem Statement:
The step 1 of solving the puzzle is identifying "Full islands".
<br>
Below figure is the one after identifying full islands.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/a61bf0dd-fb9a-4824-a0bd-1dab6ba853d7)

The step 2 of solving the puzzle is to identify the neighbors.
<br>
Since two numbers in a nurikabe puzzle cannot be part of the same island, any cell that has two numbered neighbors must be black. The two cases are when a cell is between two numbered cells, or (as in the image) when two numbered cells in the nurikabe are adjacent diagonally.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/57419492-4d07-47f0-9999-fdabecaccc9c)


After performing step 1 and step 2 as given in the previous problem descriptions, the step 3 in solving the nurikabe puzzle is the single expansion path.
<br>
If an island in the nurikabe doesn't yet have its target number of cells, and there is only one cell bordering it that is not the opposite color, that cell must be part of the region. Note that this applies to black regions within the nurikabe, too, and to white regions that don't yet have a number. Here we show in red black cells into which black regions of the nurikabe must expand, and in green cells into which white regions must expand.
<br>
For example,

Consider the below figure, among all the numbered cells only the numbered cells 5 and 6 has single expansion path to attain its target number of cells.
<br>
The image (3a) depicts step 3 after single stage of expansion of white and black cells i.e, Green coloured cell refers to the first stage of single expansion path of numbered cells 5 and 6 and Red coloured cell refers to the first stage of single expansion path of black cell.
<br>
The image (3b) depicts the final stage of board after applying step 3.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/92bdf2b6-d83a-42c7-93da-e9238c6b4ef2)


In this problem, write a program to find the coordinates of the numbered cells for which only single expansion route is present after single stage expansion, given a valid board configuration obtained after performing step 1 and step 2.


#### Input format :
First and only line of input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a board configuration with N*N cells that is assumed to be obtained after performing step 1 and step 2. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by 20 and black cells are represented by 0 in the matrix representation of the input configuration.

#### Output format :
Output should display the coordinates of the numbered cells which has single expansion path. If no numbered cells has single expansion path, then display -1. Assume that the cell coordinates starts from (1,1) till (N,N).

**Sample test cases :<br>
Input 1 :<br>**
5<br>
0 2 20 20 20<br>
3 0 20 6 20<br>
20 20 20 20 0<br>
20 2 20 0 1<br>
20 20 20 20 0<br>
**Output 1 :<br>**
1 2<br>
2 1


----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j,k=0,s=0;
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
            if((a[i][j]<11)&&(a[i][j]>1))
            {
                if((i>0)&&(a[i-1][j]==20)){k++;}
                if((i<n-1)&&(a[i+1][j]==20)){k++;}
                if((j>0)&&(a[i][j-1]==20)){k++;}
                if((j<n-1)&&(a[i][j+1]==20)){k++;}
            }
            if(k==1){cout<<i+1<<" "<<j+1<<"\n";s=1;}
            k=0;
        }
    }
    if(s==0){cout<<"-1";}
    return 0;
}

```
