# Aayush's Scholarship
Aayush studies in Teswan National University. Now is the time for exam results. Aayush similar to other students, hopes that his scores in 5 subjects in the exam could fetch him a scholarship for his GRE preparation.

The following simple rules are used to find whether he is eligible to receive scholarship:
<br>
• University follows 5 point grading system. In an exam, a student can receive any score from 2 to 5. 2 is called an F grade, meaning that student has failed that exam.
<br>
• Student should not have fail any of the exams.
<br>
• Student must obtain a full score in some of his/her exams to show that he/she is excellent in some of the subjects.
<br>
• He/She must have a grade point average not less than 4.0
<br>
You are given information regarding how Aayush performed in those 5 subjects . Help him determine whether he will receive the scholarship or not

#### Input format :
The input contains 5 space separated integers denoting Aayush’s 5 subjects score in the exam

#### Output format :
Output a single line - "Yes" (without quotes) if Aayush will receive scholarship, or "No" (without quotes) otherwise.

**Sample test cases : <br>
Input 1 :** <br>
3 4 4 4 5 <br>
**Output 1 :** <br>
Yes


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
#include<iostream>
using namespace std;
int main()
{
    int s1,s2,s3,s4,s5;
    float avg=0;
    cin>>s1>>s2>>s3>>s4>>s5;
    avg=(s1+s2+s3+s4+s5)/5;
    if((s1>2)&&(s2>2)&&(s3>2)&&(s4>2)&&(s5>2))
    {
        if((s1==5)||(s2==5)||(s3==5)||(s4==5)||(s5==5))
        {
            (avg>=4)?cout<<"Yes":cout<<"No";
        }
        else
        {
            cout<<"No";
        }
    }
    else
    {
        cout<<"No";
    }
    return 0;
}

```
