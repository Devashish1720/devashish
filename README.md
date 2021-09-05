# devashish
DSA BOOTCAMP ASSIGNMENT
Submitted by- DEVASHISH TRIPATHY 
Email- devatripathy2002@gmail.com 


Q1. Write a program to Swap to two numbers.
Ans- 
#include<iostream>
using namespace std;
int main()
{
int a=10,b=20,temp;
cout<<"value before swapping are"<<"a="<<a<<"b="<<b;
temp=a;
a=b;
b=temp;
cout<<"value after swapping"<<"a="<<a<<"b"<<b;
return 0;
}

Q2. Write a program to find the largest number among three numbers entered by the user.
Ans-
#include <iostream>
using namespace std;

int main() {    
    float n1, n2, n3;

    cout<< "Enter three numbers:";
    cin>>n1>>n2>>n3;

    if(n1>= n2 && n1>= n3)
        cout<< "Largest number:"<<n1;

    if(n2 >= n1 && n2 >= n3)
       cout<< "Largest number:"<<n2;
    
    if(n3 >= n1 && n3 >= n2)
       cout << "Largest number:"<<n3;
  
    return 0;
}

Q3. Write a program to check whether a year entered by a user is Leap year or not.
Ans-

#include <iostream>
using namespace std;
 
int main()
{
    int year;
  cout<<"Enter the year in yyyy";
    cin >> year;
    if (year % 4 == 0)
        cout << year << " is a leap year";
    else
        cout << year << " is not a leap year";
return 0;
}
Q4. Write a program to display Fibonacci Series upto nth term. (Using loops)
Ans- 
#include <iostream>
using namespace std;

int main() {
    int n, t1 = 0, t2 = 1, nextTerm = 0;

    cout<< "Enter the number of terms: ";
    cin >>n;

    cout <<"Fibonacci Series:";

    for (int i = 1; i <= n; ++i) {
                if(i == 1) {
            cout<< t1 << ", ";
            continue;
        }
        if(i == 2) {
            cout<< t2 << ", ";
            continue;
        }
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
        
        cout<< nextTerm << ", ";
    }
    return 0;
}

Q5. Write a program to check whether a number is Prime or Not.
Ans-
#include <iostream>
using namespace std;

int main() {
    int i, n;
    bool isPrime = true;

    cout<< "Enter a positive integer: ";
    cin >> n;

    // 0 and 1 are not prime numbers
    if (n == 0 || n == 1) {
        isPrime = false;
    }
    else {
        for (i = 2; i <= n / 2; ++i) {
            if (n % i == 0) {
                isPrime = false;
                break;
            }
        }
    }
    if (isPrime)
        cout << n << " is a prime number";
    else
        cout << n << " is not a prime number";

    return 0;
}


Q6. Print this pattern using loops
For n=5
        *
       * *
      * * *
     * * * *
    * * * * *
Ans-
#include<iostream>
using namespace std;
int main()
{
int n=5, s, i, j;
for(i = 1; i <= n; i++)
{
for(s = i; s < n; s++)
{
cout << " ";
}

for(j = 1; j <= (2 * i - 1); j++)
{
cout << "*";
}
cout << "\n";
}
}

Q7.Write a program that takes n elements from the user and displays the second largest element of an array.
Ans-
#include <iostream>
using namespace std;
int main(){
   int n, num[50], largest, second;
   cout<<"Enter number of elements: ";
   cin>>n;
   for(int i=0; i<n; i++){
      cout<<"Enter Array Element"<<(i+1)<<": ";
      cin>>num[i];
   }
      if(num[0]<num[1]){ 
      largest = num[1];
      second = num[0];
   }
   else{ 
      largest = num[0];
      second = num[1];
   }
   for (int i = 2; i< n ; i ++) {
            if (num[i] > largest) {
         second = largest;
         largest = num[i];
      }
      
      else if (num[i] > second && num[i] != largest) {
         second = num[i];
      }
   }
   cout<<"Second Largest Element in array is: "<<second;
   return 0;
}

Q8. https://www.hackerrank.com/callenges/array-left-rotation/problem
Ans-
int rotateLeft() {
    int N, d, i;
    cin >> N >> d;
    int start = N - d;
    int *arr = new int[N];
    for (i=0; i<N; ++i) {
        if (start == N) start = 0;
        cin >> arr[start++];
    }
    for (i=0; i<N; ++i) cout << arr[i] << " ";
    return 0;
}

Q9. https://www.hackerrank.com/challenges/grading/problem
Ans- 
int gradingStudents() {
     int n, x;
     cin>>n;
     for(int i=0; i<n; i++){
        cin>>x;
        if(x>=38 and x%5>=3){
            while(x%5!=0){
               x++;
            }
        }
        cout<<x<<endl;
     }
}

Q10.  https://www.hackerrank.com/challenges/camelcase/problem
Ans-
int camelcase(){
    string s;
    cin >> s;
    int t=1;
    for (int i=0;i<s.length();i++)
        if (isupper(s[i]))
        t++;
        cout<<t<<endl;
    return 0;
}

