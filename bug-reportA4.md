# Bug 1

1. **The incorrect original code or code snippit that you wrote:**

#include<iostream>
using namespace std;

void func(int array[], int size, int n)
{
        for(int i = 0;i < size;i++)
        {
                if( array[i] > n)
                        cout << array[i] ; 
        }
        cout << '\n';
}

int main()
{
        // first test case
        cout << "test case 1: ";
        int size1 = 5, n1 = 3;
        int array1[size1];
        array1[0] = 1; 
        array1[1] = 2; 
        array1[2] = 3; 
        array1[3] = 4;
        array1[4] = 5;
        // calling the function
        func(array1, size1, n1);
        
        
        // second test case
        cout << "test case 2: ";
        int size2 = 7, n2 = 8;
        int array2[size2];
        array2[0] = 5; 
        array2[1] = 4; 
        array2[2] = 7; 
        array2[3] = 10;
        array2[4] = 11;
        array2[5] = 9; 
        array2[6] = 14;
        
        // calling the function
        func(array2, size2, n2);
}

2. **What bug does the original code have?**

  Unexpected error while using cout function.

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**

Not using this ' ' errows may have such impact.

4. **How to correct the bug?**

Use '' and use proper cout command and the proper line is cout << array[i] << ' ';

5. **The corresponding bug-free code or code snippet is:**

#include<iostream>
using namespace std;

void func(int array[], int size, int n)
{
        for(int i = 0;i < size;i++)
        {
                if( array[i] > n)
                        cout << array[i] << ' ';
        }
        cout << '\n';
}

int main()
{
        // first test case
        cout << "test case 1: ";
        int size1 = 5, n1 = 3;
        int array1[size1];
        array1[0] = 1; 
        array1[1] = 2; 
        array1[2] = 3; 
        array1[3] = 4;
        array1[4] = 5;
        // calling the function
        func(array1, size1, n1);
        
        
        // second test case
        cout << "test case 2: ";
        int size2 = 7, n2 = 8;
        int array2[size2];
        array2[0] = 5; 
        array2[1] = 4; 
        array2[2] = 7; 
        array2[3] = 10;
        array2[4] = 11;
        array2[5] = 9; 
        array2[6] = 14;
        
        // calling the function
        func(array2, size2, n2);
}


6. **What is the take-away message from this bug?**

Always know the importance of even a single arrow.

# Bug 2

1. **The incorrect original code or code snippit that you wrote:**

#include<iostream>
using namespace std;

void func(int array[], int size, int n)
{
        for(int i = 0;i < size;i++)
        {
                if( array[i] > n)
                        cout << array[i] << ' ';
        }
        cout << '\n';
}

int main()
{
        // first test case
        cout << "test case 1: ";
        int size1 , n1 ;
        int array1[size1];
        array1[0] = 1; 
        array1[1] = 2; 
        array1[2] = 3; 
        array1[3] = 4;
        array1[4] = 5;
        // calling the function
        func(array1, size1, n1);
        
        
        // second test case
        cout << "test case 2: ";
        int size2 , n2 ;
        int array2[size2];
        array2[0] = 5; 
        array2[1] = 4; 
        array2[2] = 7; 
        array2[3] = 10;
        array2[4] = 11;
        array2[5] = 9; 
        array2[6] = 14;
        
        // calling the function
        func(array2, size2, n2);
}
2. **What bug does the original code have?**

Segmentation Fault ( Core Dumped ). 

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**

Decalaration of size and integer value is requied.

4. **How to correct the bug?**
 
Simply put size and integer value.

5. **The corresponding bug-free code or code snippet is:**

#include<iostream>
using namespace std;

void func(int array[], int size, int n)
{
        for(int i = 0;i < size;i++)
        {
                if( array[i] > n)
                        cout << array[i] << ' ';
        }
        cout << '\n';
}

int main()
{
        // first test case
        cout << "test case 1: ";
        int size1 = 5, n1 = 3;
        int array1[size1];
        array1[0] = 1; 
        array1[1] = 2; 
        array1[2] = 3; 
        array1[3] = 4;
        array1[4] = 5;
        // calling the function
        func(array1, size1, n1);
        
        
        // second test case
        cout << "test case 2: ";
        int size2 = 7, n2 = 8;
        int array2[size2];
        array2[0] = 5; 
        array2[1] = 4; 
        array2[2] = 7; 
        array2[3] = 10;
        array2[4] = 11;
        array2[5] = 9; 
        array2[6] = 14;
        
        // calling the function
        func(array2, size2, n2);
}

6. **What is the take-away message from this bug?**

Declaration of size of array is required.

# Bug 3

1. **The incorrect original code or code snippit that you wrote:**

#include<iostream>
using namespace std;

bool is_prime(int number)
{
        for(int i = 2;i * i <= number;)
        {
                // if the number is divisible by any number 
                // other than 1 and itself it is not prime
                
                if(number % i == 0)
                        return false;
        }
        
        // given number is a prime
        return true;
}

int main()
{
        int number;
        
        // first test case
        number = 7;
        if(is_prime(number))
                cout << number << " is a prime number.\n";
        else
                cout << number << " is not a prime number.\n";
        
        // second test case     
        number = 9;
        if(is_prime(number))
                cout << number << " is a prime number.\n";
        else
                cout << number << " is not a prime number.\n";      
}

2. **What bug does the original code have?**

  Not having usage of i++ while usage of for loop. 

3. **What misunderstanding of C++ concepts lead you to this incorrect code?**

Not having clarification about i++

4. **How to correct the bug?**

use i++ in for loop.

5. **The corresponding bug-free code or code snippet is:**

#include<iostream>
using namespace std;

bool is_prime(int number)
{
        for(int i = 2;i * i <= number;i++)
        {
                // if the number is divisible by any number 
                // other than 1 and itself it is not prime
                
                if(number % i == 0)
                        return false;
        }
        
        // given number is a prime
        return true;
}

int main()
{
        int number;
        
        // first test case
        number = 7;
        if(is_prime(number))
                cout << number << " is a prime number.\n";
        else
                cout << number << " is not a prime number.\n";
        
        // second test case     
        number = 9;
        if(is_prime(number))
                cout << number << " is a prime number.\n";
        else
                cout << number << " is not a prime number.\n";      
}

6. **What is the take-away message from this bug?**

we have proper knowledge where we have to use i++.
