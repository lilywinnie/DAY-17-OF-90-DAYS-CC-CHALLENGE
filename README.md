# DAY-17-OF-90-DAYS-CC-CHALLENGE

# 1. ATM


Pooja would like to withdraw X US Dollar from an ATM. The cash machine will only accept the transaction if X is a multiple of 5, and Pooja's account balance has enough cash to perform the withdrawal transaction (including bank charges). For each successful withdrawal the bank charges 0.50 US Dollar.

Calculate Pooja's account balance after an attempted transaction.


Input Format

Each input contains 2 numbers X and Y.

X is the amount of cash which Pooja wishes to withdraw. Y is Pooja's initial account balance.


Output Format

Output the account balance after the attempted transaction, given as a number with two digits of precision. If there is not enough money in the account to complete the transaction, output the current bank balance.


Constraints

0<X≤2000 - the amount of cash which Pooja wishes to withdraw.

0≤Y≤2000 with two digits of precision - Pooja's initial account balance.

Sample 1:

Input

30 120.00

Output

89.50

Explanation:
Example - Successful Transaction

Sample 2:

Input

42 120.00

Output

120.00

Explanation:
Example - Incorrect Withdrawal Amount (not multiple of 5)

Sample 3:

Input

300 120.00

Output

120.00

Explanation:
Example - Insufficient Funds


    #include <bits/stdc++.h>
    using namespace std;
    
    int main() {

    int X;          
    double Y;      
    
    cin >> X >> Y;
    
        cout << fixed << setprecision(2);
        
        if (X % 5 == 0 && (X + 0.50) <= Y) 
            cout << Y - X - 0.50 << "\n";
        else 
            cout << Y << "\n";
        
    
    return 0;}


# 2. Is it hot or cold


Chef considers the climate HOT if the temperature is above 20, otherwise he considers it COLD. You are given the temperature C, find whether the climate is HOT or COLD.


Input Format

The first line of input will contain a single integer T, denoting the number of test cases.
The first and only line of each test case contains a single integer, the temperature C.


Output Format

For each test case, print on a new line whether the climate is HOT or COLD.

You may print each character of the string in either uppercase or lowercase (for example, the strings hOt, hot, Hot, and HOT will all be treated as identical).

Constraints

1≤T≤50

0≤C≤40

Sample 1:

Input

2

21

16


Output

HOT

COLD

Explanation:
Test case 1: The temperature is 21, which is more than 20. So, Chef considers the climate HOT.

Test case 2: The temperature is 16, which is not more than 20. So, Chef considers the climate COLD.


    #include <bits/stdc++.h>
    using namespace std;
    
    int main() {
    	
    	int t;
    	cin >> t ;
    	
    	while(t--){
    	    
    	    int C;
    	    cin >> C;
    	    
    	    if(C>20)
    	        cout<<"HOT"<<"\n";
    	        
    	    else
    	        cout<<"COLD"<<"\n";
    	    
    	    
    	}
        
        return 0;}


# 3. Football Cup


It is the final day of La Liga. Chef has a certain criteria for assessing football matches.
In particular, he only likes a match if:

The match ends in a draw, and,
At least one goal has been scored by either team.
Given the goals scored by both the teams as X and Y respectively, determine whether Chef will like the match or not.


Input Format

The first line of input will contain a single integer T, denoting the number of test cases. The description of T test cases follows.
Each test case consists of a single line of input containing two space-separated integers X and Y — the goals scored by each team.


Output Format

For each test case, output YES if Chef will like the match, else output NO.

You may print each character of the string in uppercase or lowercase (for example, the strings YeS, yEs, yes and YES will all be treated as identical).

Constraints

1≤T≤100

0≤X,Y≤9

Sample 1:

Input

4

1 1

0 1

0 0

2 2


Output

YES

NO

NO

YES

Explanation:
Test case 1: It is a draw in which both teams have scored a goal, Chef will like this match.

Test case 2: The game is not a draw. Hence, Chef will not like this match.

Test case 3: Neither team scored a goal, so Chef will not like this match.

Test case 4: It is a draw in which both teams scored 2 goals each. Chef will like this match.


    #include <bits/stdc++.h>
    using namespace std;
    
    int main() {
        
        int T;
        cin>>T;
        
        while (T--){
            
            int X,Y;
            cin>>X>>Y;
            
            if(X == Y && X > 0)
                cout<<"YES\n";
                
            else
                cout<<"NO\n";
            
        }
        
        return 0;}



# 4. Pass the Exam
Chef appeared for an exam consisting of 
3
3 sections. Each section is worth 
100
100 marks.

Chef scored 
A
A marks in Section 
1
1, 
B
B marks in section 
2
2, and 
C
C marks in section 
3
3.

Chef passes the exam if both of the following conditions satisfy:

Total score of Chef is 
≥
100
≥100;
Score of each section 
≥
10
≥10.
Determine whether Chef passes the exam or not.

Input Format
The first line of input will contain a single integer 
T
T, denoting the number of test cases.
Each test case consists of a single line containing 
3
3 space-separated numbers 
A
,
B
,
C
A,B,C - Chef's score in each of the sections.
Output Format
For each test case, output PASS if Chef passes the exam, FAIL otherwise.

Note that the output is case-insensitive i.e. PASS, Pass, pAsS, and pass are all considered same.

Constraints

1≤T≤1000

0≤A,B,C≤100

Sample 1:

Input

5

9 100 100

30 40 50

30 20 40

0 98 8

90 80 80


Output

FAIL

PASS

FAIL

FAIL

PASS


Explanation:

Test Case 1: Although Chef's total score is 209≥100, still Chef fails the exam since his score in section 1 is <10.

Test Case 2: Chef cleared each section's cutoff as well his total score =120≥100.

Test Case 3: Although Chef cleared each section's cutoff but his total score is 90<100. So he fails the exam.

Test Case 4: Although Chef's total score is 106≥100, still Chef fails the exam since his score in section 1 is <10.

Test Case 5: Chef cleared each section's cutoff as well his total score =250≥100.


    #include <bits/stdc++.h>
    using namespace std;
    
    int main() {
        
    int T;
    cin >> T;
    
    while (T--) {
        int A, B, C;
        cin >> A >> B >> C;
        
        if ((A + B + C >= 100) && (A >= 10 && B >= 10 && C >= 10))
            cout << "PASS\n";
        else 
            cout << "FAIL\n";
        
        }
        
        return 0;}

# 5. Scalene Triangle


Given A,B, and C as the sides of a triangle, find whether the triangle is scalene.

Note:

A triangle is said to be scalene if all three sides of the triangle are distinct.
It is guaranteed that the sides represent a valid triangle.


Input Format

The first line of input will contain a single integer T, denoting the number of test cases.
Each test case consists of three space-separated integers A,B, and C — the length of the three sides of the triangle.

Output Format

For each test case, output on a new line, YES, if the triangle is scalene, and NO otherwise.

You may print each character of the string in uppercase or lowercase. For example, YES, yes, Yes, and yEs are all considered identical.

Constraints

1≤T≤100

1≤A≤B≤C≤10

C<(A+B)

Sample 1:

Input

4

2 3 4

1 2 2

2 2 2

3 5 6


Output

YES

NO

NO

YES

Explanation:

Test case 1: The side lengths are 2,3, and 4. Since no two side lengths are equal, the triangle is scalene.

Test case 2: The side lengths are 1,2, and 2. The sides B and C have the same length. Thus, the triangle is not scalene.

Test case 3: The side lengths are 2,2, and 2. The sides A,B, and C have the same length. Thus, the triangle is not scalene.

Test case 4: The side lengths are 3,5, and 6. Since no two side lengths are equal, the triangle is scalene.



    #include <bits/stdc++.h>
    using namespace std;
    
    int main() {
        
        int t;
        cin>>t;
        
        while(t--){
            
            int a,b,c;
            cin>>a>>b>>c;
    
            if (a!=b && b!=c && a!=c) 
                cout << "YES\n";
            
            else 
                cout << "NO\n";
            
            }
    	
        return 0;}



