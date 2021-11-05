```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int candles, b, hrs = 0;
    cin >> candles >> b;
    hrs = candles;
    while(candles >= b) {
        int new_candles = candles/b;
        hrs += new_candles;
        candles -= new_candles*b; // remove burnt
        candles += new_candles;
    }
    cout << hrs;   
}
```