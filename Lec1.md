#### 🌍 Translations
- [🇸🇦 Arabic](https://translate.google.com/translate?hl=ar&sl=en&u=https://github.com/okhalifa-official/CP_Course.Lv1/blob/main/Lec%231.md/)
- [🇫🇷 French](https://translate.google.com/translate?hl=fr&sl=en&u=https://github.com/okhalifa-official/CP_Course.Lv1/blob/main/Lec%231.md/)
- [🇪🇸 Spanish](https://translate.google.com/translate?hl=es&sl=en&u=https://github.com/okhalifa-official/CP_Course.Lv1/blob/main/Lec%231.md/)

# Introduction to Competitive Programming (CP)

## Online Judge

An **Online Judge** is a platform where you can solve coding problems and get **instant** feedback on your solutions.

### How it works

1. You pick a problem.
2. You write your code in your favorite language.
3. You submit your code.
4. The system checks it with hidden test cases.
5. You get a verdict (Correct ✅, Wrong ❌, or other errors).

Popular online judges: [Codeforces](https://codeforces.com), [LeetCode](https://leetcode.com), [HackerRank](https://www.hackerrank.com/), [AtCoder](https://atcoder.jp/).
We use [VJudge](https://vjudge.net/) to build custom sheets from all the online judges stated above.

---

### How to read the problem

* **Input:** What the program will receive.
* **Output:** What your program should print.
* **Constraints:** The limits (like size or range of inputs).
* **Examples:** Always check the sample inputs and outputs to understand what’s expected.

*Tip: Read the problem at least twice before coding!*

---

### How to submit answers

* Write your solution code.
* Run it with sample input to test.
* Submit it on the platform.
* Wait for the judge to give a result.

---

## Data Types

Data types are the building blocks of variables. They define what kind of data you can store and manipulate.

### Logic Gates

These are basic concepts from electronics that help in understanding binary logic in programming (like `AND`, `OR`, `NOT`).

Example in code:

**AND Gate (&&)**
| A | B | Result |
|---|---|--------|
| 0 | 0 |   0    |
| 0 | 1 |   0    |
| 1 | 0 |   0    |
| 1 | 1 |   1    |

**OR Gate (||)**

| A | B | Result |
|---|---|--------|
| 0 | 0 |   0    |
| 0 | 1 |   1    |
| 1 | 0 |   1    |
| 1 | 1 |   1    |

**NOT Gate (!)**

| A | Result |
|---|--------|
| 0 |   1    |
| 1 |   0    |


---

### Variables

Variables are names you give to data so you can reuse and work with them later.

```cpp
int age = 18;
long long int distance = 9 * 10^18;
char letter = 'a';
float rating = 4.8;
double pi = 3.14159265359;
```

---

### Types of Data

* `int`: Whole numbers
* `long long int`: Very large numbers
* `float` / `double`: Decimal numbers
* `char`: Single characters (like 'A', 'b')
* `bool`: true or false

#### Range of Data
* `int`:  
  **Typical range:** -2,147,483,648 to 2,147,483,647 (32-bit signed)
  **Simplified Range: -10^9 : 10^9**
  <br>
* `long long int`:    
  **Typical range:** -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 (64-bit signed)
  **Simplified Range: -10^18 : 10^18**
---

### Casting

Casting is changing one data type into another.

```cpp
float pi = 3.14;
int rounded = (int)pi;  // Now rounded is 3
```
```cpp
char letter = 'a';
int decimal_representation = (int)letter;  // Now decimal_representation is 64
```

---

### Overflow

Overflow happens when a number is too big for the data type to store.

```cpp
int big = 1000000000 * 1000; // Might overflow!
```

Use larger types like `long long` when needed.

---

## Control Program Flow

Conditions let your program **make decisions**.

### Booleans

Booleans store either `true` or `false`.

```cpp
bool isEven = (num % 2 == 0);
```

---

### If Statements

If something is true, do this.

```cpp
if (x > 10) {
   cout << "Greater than 10";
}
```

If something is true, do this.
If it's not true, do that.
```cpp
if (x > 10) {
    cout << "Greater than 10";
} else {
    cout << "10 or less";
}
```

If true, do plan A.
else, do plan B.
else, do plan C.
...
```cpp
if (x > 10) {
    cout << "Greater than 10";
} else if (x == 10) {
    cout << "Exactly 10";
} else {
    cout << "Less than 10";
}

```

---

### Nested Ifs

You can place if-statements inside others to check multiple conditions.

```cpp
if (x > 0) {
   if (x < 10) {
      cout << "Between 1 and 9";
   }
}
```

---

## Loops

Loops help you **repeat** tasks without rewriting code.

### For Loop

Used when you know how many times to repeat.

```cpp
for (int i = 0; i < 5; i++) {
   cout << i << " ";
}
```

---

### 🔁 While Loop

Repeats while a condition is true.

```cpp
int i = 0;
while (i < 5) {
   cout << i << " ";
   i++;
}
```

---

### Infinite Loops

Be careful! If your condition **never becomes false**, your loop will run forever.

```cpp
while (true) {
   // This never stops
}
```

Don't forget to break out of the infinite loops.
```cpp
while (true) {
   // Stop when a condition is true
   if(condition){
        break;
   }
}
```

---

### Nested Loops

A loop inside another loop - often used for working with grids or pairs.

```cpp
for (int i = 0; i < 3; i++) {
   for (int j = 0; j < 3; j++) {
      cout << "(" << i << "," << j << ") ";
   }
}
```

---

🎉 **You're off to a great start!**
Keep practicing and solving problems — that’s the best way to learn.
