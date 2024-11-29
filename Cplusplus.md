```markdown
# C++ Cheatsheet for Competitive Programming

## Basics
```cpp
#include <iostream>
using namespace std;

int main() {
    ios_base::sync_with_stdio(false); // Faster I/O
    cin.tie(NULL);
    // Your code here
    return 0;
}
```

## Common Headers
```cpp
#include <iostream>      // for input/output
#include <vector>        // for dynamic arrays
#include <algorithm>     // for algorithms like sort, max, min
#include <cmath>         // for mathematical functions
#include <set>           // for sets
#include <map>           // for maps
#include <unordered_map> // for unordered maps
#include <unordered_set> // for unordered sets
#include <queue>         // for queues and priority queues
#include <stack>         // for stacks
#include <deque>         // for double-ended queues
#include <bitset>        // for bit manipulation
#include <string>        // for strings
#include <numeric>       // for numeric functions like accumulate
```

## Input/Output
```cpp
// Fast Input/Output
ios_base::sync_with_stdio(false);
cin.tie(NULL);

// Input
int x;
cin >> x;

// Output
cout << x << endl;
```

## Control Structures

### If-Else
```cpp
int x = 10;

if (x > 0) {
    cout << "x is positive" << endl;
} else if (x < 0) {
    cout << "x is negative" << endl;
} else {
    cout << "x is zero" << endl;
}
```

### For Loop
```cpp
for (int i = 0; i < 10; ++i) {
    cout << i << " ";
}
cout << endl;
```

### While Loop
```cpp
int i = 0;
while (i < 10) {
    cout << i << " ";
    ++i;
}
cout << endl;
```

### Do-While Loop
```cpp
int i = 0;
do {
    cout << i << " ";
    ++i;
} while (i < 10);
cout << endl;
```

## Data Structures

### Vectors
```cpp
#include <vector>

vector<int> v;
v.push_back(1); // Add element
v.pop_back();   // Remove element
v.size();       // Get size
v.clear();      // Remove all elements
```

### Sets
```cpp
#include <set>

set<int> s;
s.insert(1);  // Add element
s.erase(1);   // Remove element
s.count(1);   // Check if element exists
s.size();     // Get size
s.clear();    // Remove all elements
```

### Unordered Sets
```cpp
#include <unordered_set>

unordered_set<int> us;
us.insert(1);
us.erase(1);
us.count(1);
us.size();
us.clear();
```

### Maps
```cpp
#include <map>

map<int, int> m;
m[1] = 10;   // Insert or update element
m.erase(1);  // Remove element
m.count(1);  // Check if key exists
m.size();    // Get size
m.clear();   // Remove all elements
```

### Unordered Maps
```cpp
#include <unordered_map>

unordered_map<int, int> um;
um[1] = 10;
um.erase(1);
um.count(1);
um.size();
um.clear();
```

### Stacks
```cpp
#include <stack>

stack<int> s;
s.push(1);   // Add element
s.pop();     // Remove element
s.top();     // Get top element
s.size();    // Get size
s.empty();   // Check if empty
// No direct clear method, you need to pop all elements manually
```

### Queues
```cpp
#include <queue>

queue<int> q;
q.push(1);   // Add element
q.pop();     // Remove element
q.front();   // Get front element
q.size();    // Get size
q.empty();   // Check if empty
```

### Priority Queues
```cpp
#include <queue>

priority_queue<int> pq; // Max-heap by default
pq.push(1);             // Add element
pq.pop();               // Remove top element
pq.top();               // Get top element
pq.size();              // Get size
pq.empty();             // Check if empty

// Min-heap
priority_queue<int, vector<int>, greater<int>> pq;
```

### Deques
```cpp
#include <deque>

deque<int> dq;
dq.push_back(1);  // Add element to back
dq.push_front(2); // Add element to front
dq.pop_back();    // Remove element from back
dq.pop_front();   // Remove element from front
dq.front();       // Get front element
dq.back();        // Get back element
dq.size();        // Get size
dq.clear();       // Clear all elements
```

## Algorithms

### Sorting
```cpp
#include <algorithm>
#include <vector>

vector<int> v = {4, 3, 1, 2};
sort(v.begin(), v.end()); // Ascending sort
sort(v.rbegin(), v.rend()); // Descending sort
```

### Finding Maximum/Minimum
```cpp
#include <algorithm>
#include <vector>

vector<int> v = {4, 3, 1, 2};
int max_val = *max_element(v.begin(), v.end());
int min_val = *min_element(v.begin(), v.end());
```

### Accumulate (Sum of elements)
```cpp
#include <numeric>
#include <vector>

vector<int> v = {1, 2, 3, 4};
int sum = accumulate(v.begin(), v.end(), 0);
```

### Binary Search
```cpp
#include <algorithm>
#include <vector>

vector<int> v = {1, 2, 3, 4};
bool found = binary_search(v.begin(), v.end(), 3);
```

### Lower Bound / Upper Bound
```cpp
#include <algorithm>
#include <vector>

vector<int> v = {1, 2, 3, 4};
auto lb = lower_bound(v.begin(), v.end(), 2); // First element not less than 2
auto ub = upper_bound(v.begin(), v.end(), 2); // First element greater than 2
```

## Miscellaneous

### GCD / LCM
```cpp
#include <algorithm>

int gcd(int a, int b) {
    return __gcd(a, b);
}

int lcm(int a, int b) {
    return (a * b) / gcd(a, b);
}
```

### Bit Manipulation
```cpp
#include <bitset>

bitset<8> bs(string("10101010"));
bs.set(1);    // Set bit at index 1
bs.reset(1);  // Reset bit at index 1
bs.flip(1);   // Flip bit at index 1
bs.count();   // Count number of 1s
bs.to_ulong(); // Convert to unsigned long
```
```

This C++ cheatsheet now includes control structures and is formatted in Markdown. If you need more detailed explanations or additional topics, feel free to ask!
