#include <iostream>
#include <algorithm>
using namespace std;

int main() {
    int n;
    cin >> n;
    int heights[n];
    if(n>500){
    	cout << "Data Error" ;
    	return 0 ;
	}
   
   
    for (int i = 0; i < n; i++) {
        cin >> heights[i];
        if(heights[i] >=150 && heights[i] <= 210){
        	continue;
		}else{
			cout << "Data Error";
			return 0 ;
		}
    }

   
    int sorted_heights[n];
    copy(heights, heights + n, sorted_heights);
    sort(sorted_heights, sorted_heights + n, greater<int>());


    int positions[n];
    for (int i = 0; i < n; i++) {
        positions[i] = i + 1;
    }

    sort(positions, positions + n, [&](int a, int b) {
        return heights[a - 1] > heights[b - 1];
    });

 
    for (int i = 0; i < n; i++) {
        cout << sorted_heights[i] << " ";
    }
    cout << endl;

    for (int i = 0; i < n; i++) {
        cout << positions[i] << " ";
    }
    cout << endl;

    return 0;
}
