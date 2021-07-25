### Sum of positive square elements in an array
```c++
#include<bits/stdc++.h>

using namespace std;

int main()
{
	int arr[5];
	int size=sizeof(arr)/sizeof(arr[0]);
	int sum=0;
	for(int i=0;i<size;++i)
	{
		cin>>arr[i];
		
	}
	
	for(auto x:arr)
	{
		sum+=x*x;
	}
	cout<<sum;
	
	return 0;
	
}
	

```

### Second smallest element in an array
```c++

#include<bits/stdc++.h>

using namespace std;

int main()
{
	int arr[5];
	int size=sizeof(arr)/sizeof(arr[0]);
	int s= INT_MAX;
	int ss=INT_MAX;
	for(int i=0;i<size;++i)
	{
		cin>>arr[i];
		
	}
	if(size==0 || size<2) cout<<" No element";

	
	for(int i=0;i<size;++i)
	{
		if(arr[i]<s)
		{
			ss=s;
			s=arr[i];
		}
		else 
		if(arr[i]<ss && arr[i]!=s)
		{
			ss=arr[i];
		}
		cout<<ss;
	}
	
	return 0;
	
}
```
	
### reverse an array

```c++
 /*  reverse the array*/

#include <bits/stdc++.h>
using namespace std;
// driver function

	
void revarray(int arr[],int start,int end){
	while(start<end){
		int temp= arr[start];
		arr[start]=arr[end];
		arr[end]=temp;
		start++;
		end--;
		}
	}
	
	void printarray(int arr[],int size){
		for (int i=0;i<size;i++)
		cout<<arr[i]<<" ";
		cout<<"\n";
		}

int main(){
	
	int arr[] = {1,2,3,4,5,6};
	int n=sizeof(arr) / sizeof(arr[0]);
	printarray(arr,n);
	revarray(arr ,0,n-1);
	cout<<"reverese array\n";
	printarray(arr,n);
	return 0;
	}

### Palindrome
```c++
  class Solution {
public:
    bool isPalindrome(string s) {
       int l=0,r=s.size()-1;
        while(l<r)
        {   
            if(!isalnum(s[l])) l++;
            if(!isalnum(s[r]))r--;
            if(isalnum(s[l])&& isalnum(s[r]))
            {
             if(tolower(s[l])!=tolower(s[r])) return false;
                l++;
                r--;
            }
        }
        return true;
    }
};

//palindrome ll
//valid palindrome II

```
### longest Palindrome substring 
```c++
#include<bits/stdc++.h>

using  namespace std;

bool isPalindrome(string s) {
       int l=0,r=s.size()-1;
        while(l<r)
        {   
            if(!isalnum(s[l])) l++;
            if(!isalnum(s[r]))r--;
            if(isalnum(s[l])&& isalnum(s[r]))
            {
             if(tolower(s[l])!=tolower(s[r])) return false;
                l++;
                r--;
            }
        }
        return true;
    }
    
string longestpal(string s)
{
	int best_len=0;
	string best_s="";
	int n=s.length();
	for(int l=0;l<n;l++)
	{
		for(int r=l;r<n;r++)
		int len= r-l+1;
		string subs=s.substr(l,len);
		if(len>best_len && isPalindrome(subs))
		{
			best_len=len;
			best_s=subs;
		}
	}
	cout<<best_len;
	cout<<best_s;
	return best_s;
}

int main(){
	string s;
	cin>>s;
	longestpal(s);
	
	}

```
