# C-Program-to-Find-the-Sum-of-First-N-Natural-Numbers

Sum of Natural Numbers in C
In this article, we will see C Program to Find the Sum of First N Natural Numbers. A Natural number is the same as a Counting number. They are used to Count the number of real physical objects. Natural numbers start from 1 and go on infinite.
 
The positive numbers 1,2,3 ... are known as natural numbers.


Formula for Sum of First n natural numbers is : n(n+1)/2.
If you want to add first 5 Natural number 
then we find the Sum of 1+2+3+4+5 =15.
sum of first n natural number in c
What we will learn
Method 1: Iterative way
Method 2: Direct Formula
Method 3: Recursive Approach
Method 1
For an input n

Create variable sum = 0
Run a for loop in iteration (I) from 1 -> n
Each time adding I to sum
Print the sum value after the loop terminates
Code
Run
#include <stdio.h>

int main()
{
    int n; 
    scanf("%d",&n);
    
    int sum = 0;
    
    for(int i=1;i<=n;i++) 
        // is same as writing sum = sum + i
        sum += i;
        
    printf("Sum is %d",sum);
    
    return 0;
}

// Time complexity : O(n)
// Space complexity : O(1)
 
Output
5
Sum is 15
While loop in C
Related Pages
Sum of N natural numbers

Sum of numbers in a given range

Greatest of two numbers

Greatest of the Three numbers

Leap year or not

Method 2
For an input n

Create variable sum = 0
Use formula sum =  n(n+1)/2
Print the sum value
Code
Run
#include <stdio.h>

int main()
{
    int n; 
    scanf("%d",&n);
    
    int sum = n*(n+1)/2;

    printf("The sum is %d",sum);
    
    return 0;
}
// Time complexity : O(1)
// Space complexity : O(1)
 
Output
6
Sum is 21
Method 3
For an input n

Create variable sum = 0
Call function getSum(sum, n)
Base Case, n == 0 return sum
Others return n + getSum(sum, n-1)
Print the sum value in main
Code
Run
#include <stdio.h>

int getSum(int sum,int n)
{
    if(n==0) 
        return sum;
        
    return n+getSum(sum,n-1);
}

int main()
{
    int n, sum = 0; 
    scanf("%d",&n);

    printf("%d",getSum(sum, n));
    
    return 0;
}
// Time complexity : O(n)
// Space complexity : O(1)
// Auxilary space complexity : O(N)
// Due to function call stack
 
Output
5
Sum is 15
