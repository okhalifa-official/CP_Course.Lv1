---
layout: default
title: Lecture 4
---

<script src="https://platform.linkedin.com/badges/js/profile.js" async defer type="text/javascript"></script>

🇸🇦 [Arabic](https://translate.google.com/translate?hl=ar&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec4) 🇫🇷 [French](https://translate.google.com/translate?hl=fr&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec4) 🇪🇸 [Spanish](https://translate.google.com/translate?hl=es&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec4) 🇩🇪 [German](https://translate.google.com/translate?hl=de&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec4)

# STLs
## Pair
### Initialization

```cpp
pair<int, int> p1 = {2, 3};                    // using initializer list
pair<string, int> p2("age", 30);              // using constructor
pair<int, string> p3 = make_pair(5, "hello"); // using make_pair()
```

### Description

A simple container to store two values together (e.g. coordinates, key-value).

### Functions

* `make_pair(a, b)` — Create a pair from two values
* `p.first` — Access the first value (O(1))
* `p.second` — Access the second value (O(1))

### Syntax

```cpp
pair<int, int> p = {2, 3};
```

### Use Cases

* Storing related values (like `x, y`).
* Sorting based on first/second element.
* Return multiple values from a function.

---

## Vector

### Initialization

```cpp
#include <vector>
vector<int> v;               // empty vector
vector<int> v(n);            // vector with n default-initialized elements
vector<int> v(n, 0);         // vector with n elements initialized to 0
vector<int> v = {1, 2, 3};   // initializer list
```

### Description

Dynamic array that resizes automatically. Allows direct access by index and efficient insertions at the end.

### Functions

* `v.push_back(x)` — Add an element to the end (O(1) amortized)
* `v.pop_back()` — Remove the last element (O(1))
* `v[i]` — Access the i-th element (O(1))
* `v.at(i)` — Safe access with bounds checking (O(1))
* `v.front()` — Access the first element (O(1))
* `v.back()` — Access the last element (O(1))
* `v.size()` — Get the number of elements (O(1))
* `v.empty()` — Check if the vector is empty (O(1))
* `v.clear()` — Remove all elements (O(n))
* `v.insert(it, val)` — Insert element at a position (O(n))
* `v.erase(it)` — Remove element from a position (O(n))
* `v.begin(), v.end()` — Iterators to the beginning and end
* `v.rbegin(), v.rend()` — Reverse iterators
* `sort(v.begin(), v.end())` — Sort vector (O(n log n))

### Use Cases

* Storing list of elements.
* Fast access by index.
* Useful in DP and graphs.

---

## Stack

### Initialization

```cpp
#include <stack>
stack<int> s;               // empty stack
```

### Description

LIFO (Last In First Out) structure using `stack<T>`.

### Functions

* `s.push(x)` — Add element to the top (O(1))
* `s.pop()` — Remove the top element (O(1))
* `s.top()` — Access the top element (O(1))
* `s.empty()` — Check if stack is empty (O(1))
* `s.size()` — Get number of elements (O(1))

### Use Cases

* Balanced parentheses.
* Backtracking.
* Undo operations.

---

## Queue

### Initialization

```cpp
#include <queue>
queue<int> q;               // empty queue
```

### Description

FIFO (First In First Out) structure using `queue<T>`.

### Functions

* `q.push(x)` — Add element to the back (O(1))
* `q.pop()` — Remove element from the front (O(1))
* `q.front()` — Access the front element (O(1))
* `q.back()` — Access the last element (O(1))
* `q.empty()` — Check if queue is empty (O(1))
* `q.size()` — Get number of elements (O(1))

### Use Cases

* BFS (Breadth-First Search).
* Scheduling processes.

---

## Deque

### Initialization

```cpp
#include <deque>
deque<int> dq;              // empty deque
deque<int> dq(n);           // deque with n default-initialized elements
deque<int> dq(n, 0);        // deque with n elements initialized to 0
deque<int> dq = {1, 2, 3};  // initializer list
```

### Description

Double-ended queue. Supports insertion/removal from both ends efficiently.

### Functions

* `dq.push_front(x)` — Add to front (O(1))
* `dq.push_back(x)` — Add to back (O(1))
* `dq.pop_front()` — Remove from front (O(1))
* `dq.pop_back()` — Remove from back (O(1))
* `dq.front()` — Access front element (O(1))
* `dq.back()` — Access back element (O(1))
* `dq[i]` or `dq.at(i)` — Access i-th element (O(1))
* `dq.empty()` — Check if empty (O(1))
* `dq.size()` — Get size (O(1))

### Use Cases

* Sliding window problems.
* Palindrome checking.

---

## Priority Queue

### Initialization

```cpp
#include <queue>
priority_queue<int> pq;                                  // max-heap
priority_queue<int, vector<int>, greater<int>> min_pq;   // min-heap
```

### Description

A max-heap by default. Highest-priority element is accessed first.

### Functions

* `pq.push(x)` — Add element (O(log n))
* `pq.pop()` — Remove top element (O(log n))
* `pq.top()` — Access top element (O(1))
* `pq.empty()` — Check if empty (O(1))
* `pq.size()` — Get number of elements (O(1))

> Use `priority_queue<T, vector<T>, greater<T>>` for a min-heap.

### Use Cases

* Dijkstra's algorithm.
* Greedy problems.
* Task scheduling.

---

## Map

### Initialization

```cpp
#include <map>
map<int, string> m;            // empty map
```

### Description

Associative container storing key-value pairs in sorted order by key.

### Functions

* `m[key] = val` — Insert or update key with value (O(log n))
* `m.at(key)` — Access value by key (throws if not found) (O(log n))
* `m.find(key)` — Returns iterator to key (O(log n))
* `m.count(key)` — Check if key exists (O(log n))
* `m.erase(key)` — Remove key (O(log n))
* `m.size()` — Number of elements (O(1))
* `m.empty()` — Check if map is empty (O(1))

### Use Cases

* Frequency count.
* Fast lookup by key.
* Memoization.

---

## Set

### Initialization

```cpp
#include <set>
set<int> s;                  // empty set
set<int> s = {1, 2, 3};      // initializer list
```

### Description

Stores unique elements in sorted order.

### Functions

* `s.insert(x)` — Insert element (O(log n))
* `s.erase(x)` — Remove element (O(log n))
* `s.find(x)` — Returns iterator to element (O(log n))
* `s.count(x)` — Check if element exists (O(log n))
* `s.size()` — Number of elements (O(1))
* `s.empty()` — Check if set is empty (O(1))
* `s.lower_bound(x)` — First element >= x (O(log n))
* `s.upper_bound(x)` — First element > x (O(log n))

### Use Cases

* Fast lookup and uniqueness.
* Finding nearest element.
* Removing duplicates.

---

## Time Complexity Comparison

| Data Structure  | Find           | Insert      | Delete      | Size    | Dynamic |
| --------------- | -------------- | ----------- | ----------- | -----   | ------- |
| Array           | O(1) \[by idx] | Not allowed | Not allowed | Fixed   | No      |
| Vector          | O(1) \[by idx] | O(1) amort. | O(1) (back) | Dynamic | Yes     |
| Stack           | O(1)           | O(1)        | O(1)        | Dynamic | Yes     |
| Queue           | O(1)           | O(1)        | O(1)        | Dynamic | Yes     |
| Deque           | O(1)           | O(1)        | O(1)        | Dynamic | Yes     |
| Priority Queue  | O(1) (top)     | O(log n)    | O(log n)    | Dynamic | Yes     |
| Map             | O(log n)       | O(log n)    | O(log n)    | Dynamic | Yes     |
| Set             | O(log n)       | O(log n)    | O(log n)    | Dynamic | Yes     |

> Note: `unordered_map` and `unordered_set` offer **O(1)** average case for find/insert/delete.

---

**Tips:**

* Use `vector` when you need a resizable array.
* Use `set` or `map` for fast lookups and ordering.
* Use `priority_queue` for greedy selection (max and min).
* Use `deque` for double insertion and deletion.

---

## Common `<algorithm>` Functions and Their Complexities

| Function                               | Description                       | Time Complexity |
| -------------------------------------- | --------------------------------- | --------------- |
| `sort(v.begin(), v.end())`             | Sorts elements in ascending order | O(n log n)      |
| `reverse(v.begin(), v.end())`          | Reverses the range                | O(n)            |
| `min_element(v.begin(), v.end())`      | Finds the min in range            | O(n)            |
| `max_element(v.begin(), v.end())`      | Finds the max in range            | O(n)            |
| `accumulate(v.begin(), v.end(), 0)`    | Sum of elements                   | O(n)            |
| `count(v.begin(), v.end(), x)`         | Counts occurrences of x           | O(n)            |
| `binary_search(v.begin(), v.end(), x)` | True if x exists in sorted range  | O(log n)        |
| `lower_bound(v.begin(), v.end(), x)`   | First element >= x (sorted)       | O(log n)        |
| `upper_bound(v.begin(), v.end(), x)`   | First element > x (sorted)        | O(log n)        |
| `next_permutation(v.begin(), v.end())` | Next lexicographical permutation  | O(n)            |

These functions simplify many common tasks and save you from implementing them manually.

<br>

"The key to mastering algorithms is not remembering every detail, but understanding when and why to use each tool."
<br>
<br>

---

<br>

© 2025 Pathline Training Academy | Made with 💙 by <a class="badge-base__link LI-simple-link" href="https://eg.linkedin.com/in/omar-khalifa-625586292?trk=profile-badge">Omar Khalifa</a>  
[Back to Top](#top)
