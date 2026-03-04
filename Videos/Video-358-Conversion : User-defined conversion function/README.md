Video 359 – Conversion : User-defined conversion function

Video : https://youtube.com/your-link



1️⃣ What is User-defined conversion function ?

<details> <summary>✅ Show Answer</summary> <br>

Its a function with a special syntax for conversion ( Syntax must be learned ).<br> 
Enables implicit conversion or explicit conversion from a class type to another type.<br>
    
Example:
```

```
</details>

2️⃣ User-defined conversion functions has explicit and implicit conversion. Explain that.

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
<details> <summary>✅ Show Answer</summary>   
Example:
</details>
</details>

🔁 Navigation

⬅ Previous Practice: (link)
➡ Next Practice: (link)
