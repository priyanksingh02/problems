```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int digits, sum;
    cin >> digits >> sum;
    if(sum == 0) {
        if(digits == 1) {
            cout << "0 0";
        }
        else {
            cout << "-1 -1";
        }
    }
    else {
        //minimum
        if(sum <= (digits-1)*9) {
            cout << "1";
            int n_nines = (sum-1)/9;
            int n_zeros = digits - 2 - n_nines;
            string zeros(n_zeros, '0');
            cout << zeros;
            cout << sum - 1 - 9*n_nines;
            string nines(n_nines, '9');
            cout << nines;
        }
        else if (sum > (digits) * 9) {
            cout << "-1";
        }
        else {
            int val = sum - 9*(digits-1);
            assert(val > 0 and val <= 9);
            cout << val;
            cout << string (digits - 1, '9');
        }
        cout << " ";
        //maximum
        if(sum > (digits) * 9) {
            cout << "-1";
        }
        else {
            int n_nines = sum/9;
            cout << string(n_nines, '9');
            if(n_nines == digits)
                return 0;
            int val = sum - 9*n_nines;
            assert(val >= 0 and val <= 9);
            cout << val;
            if(digits > n_nines + 1) {
                cout << string(digits - n_nines - 1, '0');
            }
        }
    }
}
```