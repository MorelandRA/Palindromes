#include <iostream> 	// cin >>, cout <<;
#include <string> 	// Strings

using namespace std;

int main();
bool recursive_palindrome(string);	 // Checks for a palindrome using a recursive algorithm.
bool iterative_palindrome(string);	 // Checks for a palindrome using an iterative algorithm.

int main()
   {

   string str;
   cout << "Please enter a string." << endl;  	         // Get input
   cin >> str;

   if (recursive_palindrome(str)) 			 // Solve recursively and show results
	{
	cout << str << " is a palindrome (recursive)." << endl;
	}
   else
	{
	cout << str << " is not a palindrome (recursive)." << endl;
	}


   if (iterative_palindrome(str))			 // Solve iteratively and show results
	{
	cout << str << " is a palindrome (iterative)." << endl;
	}
   else
	{
	cout << str << " is not a palindrome (iterative)." << endl;
	}
   }


bool recursive_palindrome(string str)
   {
   bool success = false;						    	 // Default value; will be changed to true if the string is a palindrome.
   if(str.length() == 0 || str.length() == 1)					 // If the string is of length 0 or 1, it must be a palindrome.
	{
	success = true;
	}
   else if (str[0] == str[ str.length() - 1]) 					 // If it's longer, it can be a palindrome only if:
										 	 // The string between the first and last characters is a palindrome AND
											 // The first and last characters are the same.
	{
	success = recursive_palindrome( str.substr(1, str.length() - 2) );	 // Check to see if the string in between the first and last characters is a palindrome.
	}
   return success;
   }

bool iterative_palindrome(string str)
   {
   bool palin = true; 	         	// Will turn to false if lIndex and rIndex do not match.
   int lIndex = 0; 			// Left index; counts from the left.
   int rIndex = str.length()-1;		// Right index; counts from the right.

   while(palin == true && lIndex < rIndex) 	// Counting from both the far left and far right, check to see if the two characters are the same.
	{  				        // If they are, move in one and check again, until the left counter crosses the right counter.
	if(str[lIndex] != str[rIndex]) 	        // If they aren't, change the value of palin to false and end the loop.
	   {
	   palin = false;
	   }
	lIndex++;
	rIndex--;
	}

   return palin;
   }

