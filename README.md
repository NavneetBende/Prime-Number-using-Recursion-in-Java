# Prime-Number-using-Recursion-in-Java

To Check Number Is Prime or Not Using Recursion in Java
Here, in this page we will discuss the program to check a number is prime number or not using recursion in Java programming language. We are given with a number and check if it is prime or not. We will discuss both recursive and non-recursive approach to check if a given number is prime or not. A number is prime, if it is divisible by 1 and number itself.

Example :

Input : Number : 35
Output : No
Explanation : 35 is not a prime number, as factors of 35 are 1, 5.
Prime number between 1 to 100 in C++
Method 1 (Using Recursion) 
Create a isprime(int n, int i=2), it return bool values)
Base condition will be :
if (n <= 2)    
return (n == 2) ? true : false;
if (n % i == 0)
return false;
if (i * i > n)   
return true;

Otherwise return isprime(n, i+2)
Prime Number Using Recursion in Java
Time and Space Complexity
The Time Complexity : O(sqrt(n)) and the Space Complexity : O(1)
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Power of a Number

Largest element in an array

Code in Java
Run
public class Main
{
     static boolean isPrime(int n, int i)
    {
        // Base cases
        if (n <= 2) 
           return (n == 2) ? true : false; 
       if (n % i == 0) 
           return false; 
       if (i * i > n)

            return true;
        // Check for next divisor
        return isPrime(n, i + 1);
    }

  // Driver program to test above function
  public static void main(String[] args)
  {  
    int n = 12;
    if (isPrime(n, 2))
      System.out.println("Yes it's a Prime");
   else
     System.out.println("Not a Prime");
   }
 }
Not a Prime
 

What exactly is recursion?
Recursion is the process by which a function calls itself directly or indirectly, and the corresponding function is known as a recursive function. Certain problems can be solved quite easily using a recursive algorithm.
Code in Java (Using Loop)
Run
public class Main
{
      static boolean isPrime(int n)
    {
        // Check if number is less than
        // equal to 1
        if (n <= 1)
            return false;
        // Check if number is 2
        else if (n == 2)
            return true;

        // Check if n is a multiple of 2
        else if (n % 2 == 0)
            return false;

        // If not, then just check the odds
        for (int i = 3; i <= Math.sqrt(n); i += 2)
        {
            if (n % i == 0)
                return false;
        }
        return true;
    }

    // Driver code
    public static void main(String[] args)
    {
        if (isPrime(20))
            System.out.println("true");

        else
            System.out.println("false");
    }
}
Output
false
