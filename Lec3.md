---
layout: default
title: Lecture 3
---

<script src="https://platform.linkedin.com/badges/js/profile.js" async defer type="text/javascript"></script>

🇸🇦 [Arabic](https://translate.google.com/translate?hl=ar&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec3) 🇫🇷 [French](https://translate.google.com/translate?hl=fr&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec3) 🇪🇸 [Spanish](https://translate.google.com/translate?hl=es&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec3) 🇩🇪 [German](https://translate.google.com/translate?hl=de&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec3)

# Complexity Analysis & Recursion

## Complexity Analysis

### Introduction

* **What it is:**
  - Measures how fast (time) or how much memory (space) an algorithm uses as input size grows.
  - Relation between **input growth and (time or memory)**.
* **Why it matters:** Helps you choose the most efficient solution, especially for large inputs.

#### Notations
* Omega Notation (Best Case)→ `Ω(...)`
* Theta Notation (Average Case)→ `Θ(...)`
* **Big-O Notation (Worst Case)→** `O(...)`

### Big-O (Worst Case)

* **Definition:** Upper bound on time or space usage in the worst-case scenario.
* **Notation:** `O(...)`

### Common Time Complexities

* **O(1) – Constant Time**

  * Runs in the same time regardless of input size.
  * *Example:* Accessing `arr[5]`.

* **O(N) – Linear Time**

  * Time grows directly with input size `N`.
  * *Example:* Looping once over an array of size `N`.<br>
    _**Visual Explanation :** [Linear Search Visualization](https://visualgo.net/en/array)_


* **O(N²) – Quadratic Time**

  * Time grows with the square of input size.
  * *Example:* Nested loops over an array.<br>
    _**Visual Explanation :** [Selection Sort Visualization](https://algorithm-visualizer.org/brute-force/selection-sort)_
  

* **O(log N) – Logarithmic Time**

  * Time grows with the logarithm of `N`.
  * *Example:* Binary search on a sorted array.<br>
    _**Visual Explanation :** [Binary Search Visualization](https://algorithm-visualizer.org/branch-and-bound/binary-search)_

![Common Time Complexities Chart](https://paper-attachments.dropbox.com/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio+17.png)

_Chart Source: [freeCodeCamp Big-O Cheat Sheet](https://www.freecodecamp.org/news/big-o-cheat-sheet-time-complexity-chart/)_


### Rules for Simplifying Big-O

1. **Drop lower-order terms:**
   `O(N² + N) → O(N²)`
2. **Drop constant factors:**
   `O(3N) → O(N)`
3. **Keep only the fastest-growing term.**

### Sample Code

```cpp
// O(N) example: sum of all elements in an array
int sumArray(int arr[], int N) {
    int sum = 0;               // O(1)
    for (int i=0; i<N; i++) {  // runs N times → O(N)
        sum += arr[i];         // O(1)
    }
    return sum;                // O(1)
}
// Total: O(1) + O(N)* (O(1) + O(1)) → O(N)
```

---

## 2. Recursion

### Structure
* Base Case
* Step
* Assume it works (Call Back)
```cpp
  int rec(int i) {
      // Base Case
      ..

      // Step
      ..
  }
  ```

### Call Stack

* **What it is:** A stack in memory that tracks active function calls.
* **How it works:**

  1. Each call pushes a new frame.
  2. When a function returns, its frame is popped.
  3. Too many nested calls can cause **stack overflow**.

### Factorial Problem

* **Definition:**

  ```
  n! = n × (n−1) × (n−2) × … × 1
  ```
* **Recursive Form:**

  ```
  fact(n) = 
    if n == 0: return 1
    else:      return n * fact(n−1)
  ```
* **Code:**

  ```cpp
  long long fact(int n) {
      if (n == 0)         // base case
          return 1;
      return n * fact(n-1); // step
  }
  ```
_**Visual Explanation :** [Factorial Visualization](https://visualgo.net/en/recursion)_

### Fibonacci

* **Definition:**

  ```
  F(0) = 0,  
  F(1) = 1,  
  F(n) = F(n-1) + F(n-2)
  ```
* **Recursive Code:**

  ```cpp
  int fib(int n) {
      if (n <= 1)       // base cases
          return n;

      return fib(n-1) + fib(n-2);   // step
  }
  ```

_**Visual Explanation :** [Fibonacci Visualization](https://visualgo.net/en/recursion)_

<br>

"To understand recursion, one must first understand recursion."
— Anonymous (Popular among computer scientists, often attributed to humorous folklore)
<br>
<br>

---

<br>

© 2025 Pathline Training Academy | Made with 💙 by <div class="badge-base LI-profile-badge" data-locale="en_US" data-size="large" data-theme="light" data-type="HORIZONTAL" data-vanity="omar-khalifa-625586292" data-version="v1"><a class="badge-base__link LI-simple-link" href="https://eg.linkedin.com/in/omar-khalifa-625586292?trk=profile-badge">Omar Khalifa</a></div>
                
[Back to Top](#top)
