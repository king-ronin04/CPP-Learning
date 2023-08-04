# Insomnia cure
«One dragon. Two dragon. Three dragon», — the princess was counting. She had trouble falling asleep, and she got bored of counting lambs when she was nine.

However, just counting dragons was boring as well, so she entertained herself at best she could. Tonight she imagined that all dragons were here to steal her, and she was fighting them off. Every k-th dragon got punched in the face with a frying pan. Every l-th dragon got his tail shut into the balcony door. Every m-th dragon got his paws trampled with sharp heels. Finally, she threatened every n-th dragon to call her mom, and he withdrew in panic.

Write a program to find how many imaginary dragons suffered moral or physical damage tonight, if the princess counted a total of d dragons?

#### Input format :
Input data contains integer numbers k, l, m, n and d, each number in a separate line (1 ≤ k, l, m, n ≤ 10, 1 ≤ d ≤ 105).

#### Output format :
The output displays the number of damaged dragons.

**Sample test cases :<br>
Input 1 :** <br>
1<br>
2<br>
3<br>
4<br>
12<br>
**Output 1 :** <br>
12 <br>

**Input 2 :**  <br>
2<br>
3<br>
4<br>
5<br>
24<br>
**Output 2 :**  <br>
17


-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
#include<iostream>
using namespace std;
int main()
{
	   int i,k,m,n,l,d,count=0;
	   cin>>k;
	   cin>>l;
	   cin>>m;
	   cin>>n;
	   cin>>d;
     for(i=1;i<=d;i++)
	   {
	       if(i%k==0||i%l==0||i%m==0||i%n==0)
	       {
	           count++;
	       }
	   }
	   cout<<count;
	}



```
