```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
	int tc;
	cin >> tc;
	while(tc--) {
		string str;
		cin >> str;
		if(str.size() > 10) {
			cout << str.front() << (int)str.size() - 2 << str.back() << "\n";
		}
		else {
			cout << str << "\n";
		}
	}
}
```