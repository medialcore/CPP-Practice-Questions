Video 359 – Conversion : User-defined conversion function

📺 Watch the video here:
https://youtube.com/your-link

1. What is User-defined conversion function ?

<details> <summary>✅ Show Answer</summary> <br>

Its a function with a special syntax for conversion ( Syntax must be learned ).<br> 
Enables implicit conversion or explicit conversion from a class type to another type.<br>
    
Example:
```
struct X
{
    // implicit conversion
    operator int() const { return 7; }
 
    // explicit conversion
    explicit operator int*() const { return nullptr; }
 
    // Error: array operator not allowed in conversion-type-id
//  operator int(*)[3]() const { return nullptr; }
 
    using arr_t = int[3];
    operator arr_t*() const { return nullptr; } // OK if done through typedef
//  operator arr_t () const; // Error: conversion to array not allowed in any case
};
 
int main()
{
    X x;
 
    int n = static_cast<int>(x);   // OK: sets n to 7
    int m = x;                     // OK: sets m to 7
 
    int* p = static_cast<int*>(x); // OK: sets p to null
//  int* q = x; // Error: no implicit conversion
 
    int (*pa)[3] = x;  // OK
}
```



</details>
2️⃣ What is initialization?

Write the question here.

<details> <summary>✅ Show Answer</summary>

Initialization means assigning a value at the time of declaration.

Example:

int value = 10;
</details>
🟡 Intermediate Questions
3️⃣ What is scope?

Question text here.

<details> <summary>✅ Show Answer</summary>

Scope defines where a variable is accessible.

Example:

void function() {
    int local = 5;
}

local is only accessible inside the function.

</details>
🔴 Advanced Questions
4️⃣ Explain storage duration.

Question text here.

<details> <summary>✅ Show Answer</summary>

Storage duration determines how long a variable exists in memory.

Types:

Automatic

Static

Thread

Dynamic

</details>
🧠 Bonus Challenge

What will this program output?

#include <iostream>

int main() {
    int x = 5;
    std::cout << ++x;
}
<details> <summary>💡 Solution</summary>

Output: 6

++x increments before printing.

</details>
📚 Key Takeaways

Always initialize variables

Understand scope rules

Know lifetime and storage duration

🔁 Navigation

⬅ Previous Practice: (link)
➡ Next Practice: (link)
