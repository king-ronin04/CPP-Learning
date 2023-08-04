# Valid Configuration

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
An island is full if it contains as many white cells as the number in the region. Any 1s are trivially full regions. When you encounter a full region, any cells that boarder it must be black. Here we show the cells that must be black due to a single celled white island.

Below figure is the one after identifying full islands.

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/fc357f5a-20ac-47da-b74d-e2a2b2adc293)


The step 2 of solving the puzzle is to identify the neighbors.
<br>
Since two numbers in a nurikabe puzzle cannot be part of the same island, any cell that has two numbered neighbors must be black. The two cases are when a cell is between two numbered cells, or (as in the image) when two numbered cells in the nurikabe are adjacent diagonally

![image](https://github.com/king-ronin04/CPP-Learning/assets/103017387/a06def1b-7a3e-42de-89cd-c5e8c2f86f1c)


Given a board configuration in which empty white cells are represented by -1, black cells are represented by 0 and grey cells are represented by 20. Write a program to find whether it is a valid configuration assuming it to be obtained after performing step 1 and 2.



#### Input format :
First and only line of input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a board configuration with N*N cells assuming it to be obtained after performing step 1 and step 2. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by 20, empty white cells are represented by -1 and black cells are represented by 0 in the matrix representation of the input configuration.

#### Output format :
Output should display "Yes" (without quotes) if the given configuration is a valid one obtained after performing step 1 and 2 of the nurikabe puzzle. Print "No" otherwise.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
20 0 1 0 2<br>
20 20 0 20 -1<br>
20 20 20 20 20<br>
3 0 2 20 20<br>
20 20 20 20 20<br>
**Output 1 :<br>**
Yes



----------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int n,i,j,s=1;
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
            if(a[i][j]==1)
            {
                if((a[i-1][j]!=0)&&(i>0)){s=0;break;}
                if((a[i+1][j]!=0)&&(i<n-1)){s=0;break;}
                if((a[i][j+1]!=0)&&(j<n-1)){s=0;break;}
                if((a[i][j-1]!=0)&&(j>0)){s=0;break;}
            }
            if((a[i][j]>0)&&(a[i][j]<11))
            {
                if((a[i+2][j]<11)&&(a[i+2][j]>0)&&(i<n-2)){if(a[i+1][j]!=0){s=0;break;}}
                if((a[i][j+2]<11)&&(a[i][j+2]>0)&&(j<n-2)){if(a[i][j+1]!=0){s=0;break;}}
                if((a[i-1][j-1]<11)&&(a[i-1][j-1]>0)&&(i>0)&&(j>0)){if((a[i-1][j]!=0)||(a[i][j-1]!=0)){s=0;break;}}
                if((a[i+1][j-1]<11)&&(a[i+1][j-1]>0)&&(i<n-1)&&(j>0)){if((a[i+1][j]!=0)||(a[i][j-1]!=0)){s=0;break;}}
            }
        }
        if(s==0){break;}
    }
    (s==0)?cout<<"No":cout<<"Yes";
    return 0;
}


```
