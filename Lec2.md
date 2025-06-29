---
layout: default
title: Lecture 2
---

🇸🇦 [Arabic](https://translate.google.com/translate?hl=ar&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec2) 🇫🇷 [French](https://translate.google.com/translate?hl=fr&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec2) 🇪🇸 [Spanish](https://translate.google.com/translate?hl=es&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec2) 🇩🇪 [German](https://translate.google.com/translate?hl=de&sl=en&u=https://okhalifa-official.github.io/CP_Course.Lv1/Lec2)


# Arrays & Strings

## Arrays

### 1D Arrays

* A list of elements stored in a single row.
* All elements must be of the same data type (like `int`, `char`, etc.).
* You access elements using their index starting from 0.
* Example:

  ```cpp
  int arr[5] = {10, 20, 30, 40, 50};
  cout << arr[2]; // Output: 30
  ```

### 2D Arrays

* Arrays arranged in rows and columns (like a table).
* Access elements using two indices: `arr[row][col]`
* Example:

  ```cpp
  int matrix[2][3] = {
      {1, 2, 3},
      {4, 5, 6}
  };
  cout << matrix[1][2]; // Output: 6
  ```

---

## Strings

### Null Terminator

* When using `cin` to read input into a character array, it stops reading at the first space and automatically appends a null terminator (`'\0'`) to mark the end of the string.

* A null terminator is a special character (`'\0'`) that marks the end of a C-style string.

* It's automatically added at the end of string literals in C-style strings.

* Important when using character arrays instead of `string` class.

* Without the null terminator, functions like `strlen()` and `cout` may read garbage values beyond the intended end.

* Example:

  ```cpp
  char name[] = "Omar";
  // Actually stored as: ['O', 'm', 'a', 'r', '\0']
  ```

### Operations on Strings

* `getline()` reads an entire line including spaces until a newline is encountered.

* Useful when reading full sentences or names with spaces.

* Syntax: `getline(cin, variable);`

* Example:

  ```cpp
  #include <iostream>
  #include <string>
  using namespace std;

  string sentence;
  getline(cin, sentence);
  cout << "You entered: " << sentence;
  ```

* Strings are sequences of characters.

* Declare: `string name = "Omar";`

* Combine: `s1 + s2`

* Length: `s.length()` or `s.size()`

* Access characters with `s[i]`

* Loop through:

  ```cpp
  for (char c : s) {
      cout << c << " "; // print all chars in string
  }
  ```
  
* Selecting a substring with `substr(pos, len)`:
  ```cpp
  string text = "OmarKhalifa";
  string sub = text.substr(4,7);  // output: Khalifa
  ```
  

### Casting Digits from Characters

* Convert character digits like `'5'` to int:

  ```cpp
  char ch = '5';
  int digit = ch - '0'; // digit = 5
  ```

### Converting String to Integer (stoi)

* Use `stoi()` to convert an entire string to an integer.
* Only works with numeric strings like "123".
* Defined in `<string>`.
* Example:

  ```cpp
  #include <string>
  string numStr = "456";
  int num = stoi(numStr); // num = 456
  ```

  ```cpp
  char ch = '5';
  int digit = ch - '0'; // digit = 5
  ```

---

## Functions

### Function Implementation

* Reusable blocks of code that perform specific tasks.
* Helps make your code cleaner, modular, and easier to debug.
* A function has a return type, a name, parameters (optional), and a body.
* Example:

  ```cpp
  int add(int a, int b) {
      return a + b; // returns the sum of a and b to where the function was called
  }
  ```

### return Statement

* `return` is used to send a value back from the function to where it was called.
* Once `return` is executed, the function ends immediately.
* If the function has a return type (like `int`), you must return a value of that type.
* Example:

  ````cpp
  int square(int x) {
      return x * x;
  }
  ````
* Define functions to organize your program better.
* Example:

  ```cpp
  int add(int a, int b) {
      return a + b;
  }
  ```

### Function Calling

* Call a function by its name and pass arguments:

  ```cpp
  int result = add(3, 4); // Output: 7
  ```

---

## Built-in Functions

### cmath Library

* Math functions like `sqrt()`, `pow()`, `abs()`, `ceil()`, `floor()`, `round()`, etc.
* Include the library:

  ```cpp
  #include <cmath>
  cout << sqrt(16); // Output: 4
  cout << pow(5,3); // Output: 125
  cout << abs(-2); // Output: 2
  cout << ceil(2.1); // Output: 3
  cout << floor(4.8); // Output: 4
  cout << round(7.3) << round(7.8); // Output: 7 8
  ```

### algorithm Library

* Useful for sorting, finding max/min, reversing arrays, etc.
* Common functions:

  * `sort(arr, arr + n)`
  * `reverse(arr, arr + n)`
  * `max(a,b)`, `min(a,b)`
  * `find(arr, arr + n, target)`
* Example:

  ```cpp
  #include <algorithm>
  int arr[] = {3, 1, 4};
  sort(arr, arr + 3);
  ```

### cctype Library

* Useful for checking and converting characters.
* Include the library:

  ```cpp
  #include <cctype>
  ```
* Common functions:

  * `isdigit(c)` → checks if `c` is a digit.
  * `isalpha(c)` → checks if `c` is a letter.
  * `islower(c)` → checks if `c` is lowercase.
  * `isupper(c)` → checks if `c` is uppercase.
  * `tolower(c)` → converts to lowercase.
  * `toupper(c)` → converts to uppercase.
* Example:

  ```cpp
  char ch = 'A';
  if (isupper(ch)) cout << tolower(ch); // Output: a
  ```
<br>

"The only way to learn a new programming language is by writing programs in it."
— Dennis Ritchie
<br>
<br>

---

<br>

© 2025 Pathline Training Academy | Made with 💙 by Omar Khalifa  
[Back to Top](#top)
