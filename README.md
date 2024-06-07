Kth max and min element in array in C++
Here, in this page we will discuss the program to find the kth max and min element in an array in C++ . We use the concept of set in finding the kth maximum and minimum element of the array. We are giving with the size of the array along with array elements and the value of K. We have to print the maximum and the minimum element.

kth max and min element in array in C++
Algorithm :
Take the size of the array from the user and store it in variable say n.
Now, declare a vector of size n and take the n elements of the vector say arr from the user.
Declare one variable say k and take the value of k from the user.
Now, declare a set say s and insert the vector values in it.
Declare an iterator say itr and point it to first element of the array and using the advance() function pass itr and k-1 to it, so that it will point to the kth element of the set. (As in set data is stored in sorted manner).
Now print the value of itr (which reflects the kth minimum value of the vector)
Again set itr to s.begin().
Now, pass the itr and n-k to advance() so that it will point to kth maximum value.
k-th minimum and maximum element in an array
Code in C++
#include<bits/stdc++.h>
using namespace std;
int main(){

  int n;
  cin>>n;

  vectorarr(n);

  for(int i=0; i<n; i++)
    cin>>arr[i];

  int k;
  cin>>k;

  set s(arr.begin(), arr.end());

  set::iterator itr = s.begin(); // s.begin() returns a pointer to first element in the set

  advance(itr, k - 1); //itr points to kth element (minimum)in set

  cout <<"Minimum :"<< *itr << "\n";

  itr = s.begin();

  advance(itr, n-k); //itr points to kth element (maximum)in set

  cout <<"Maximum :"<< *itr << "\n";

  return 0;
}

Output :

6

80 90 23 45 2 67

4

Minimum :67

Maximum :45
