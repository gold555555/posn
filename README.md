#include <bits/stdc++.h>
using namespace std;

int main() { int n, m, i, j; cin >> n ;

  for(i=0; i<n; i++){
   // cout << " ";
    for(j=0;j<n;j++){
    	if(j==n-1 && i<n){
         cout << "*";
  
	 }
	 
	
	else if(i+j == n-1 && i>0 && i<n-1 && j<n-1 && j>0){
			cout << "*";
		}else	if(i == n-1 && j<n-1){
         	cout << "*";
  
	 }
		
		else{
			cout << " ";
		}

	}
       cout << endl;  
    
}
}
