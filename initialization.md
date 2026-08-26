# Initialization

[🔙 to README](README.md)

<div align="center">
    <img src="assets/initialization_cxx.gif" alt="example_1">
</div>


```c++
int x;                  // Default initialization: uninitialized (garbage value)
int x{};                // Value initialization: 0
int x = {};             // Value initialization (with equals): 0
int x = int();          // Value initialization (creates temporary, then copy): 0
int x = 10;             // Copy initialization: 10
int x = int(10);        // Copy initialization (creates temporary, then copy): 10
int x = (1, 0);         // Copy initialization (comma operator evaluates to rightmost): 0
int x(10);              // Direct initialization: 10
int x{10};              // Direct list (uniform) initialization: 10
int x = {10};           // Copy list initialization: 10
auto x = 10;            // Type deduction: int, value 10
auto x{10};             // Type deduction: int, value 10 (since C++17, earlier was std::initializer_list<int>)
auto x = {10};          // Type deduction: std::initializer_list<int> with one element 10
auto x = int{10};       // Type deduction: int, value 10
auto x = (1, 0);        // Type deduction: int, value 0 (comma operator)

Point p = {1, 2};                       // Aggregate initialization
Point p = {.x = 1, .y = 2};             // Designated initialization (C++20/23)
auto [a, b] = std::pair{1, 2};          // Structured binding initialization
std::vector<int> v = {1, 2, 3};         // std::initializer_list initialization
auto* p = new MyClass{1, 2};            // Dynamic allocation with brace init
constexpr int x = 42;                   // Constant expression initialization
auto f = [x = 42]() { return x; };      // Lambda init-capture
foo({1, 2});                            // Braced initializer as function arg
```

[🔙 to README](README.md)