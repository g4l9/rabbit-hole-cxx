# Template condition

[🔙 to README](README.md)

## Constraint definition

```c++
template<class Tp>
inline constexpr bool is_signed_integral_v =
        std::is_integral<Tp>::value && std::is_signed<Tp>::value;
```
constexpr `_v` style constraint

```c++
template<class Tp>
inline constexpr bool is_signed_integral_v =
        std::is_integral_v<Tp> && std::is_signed_v<Tp>;
```

concept style constraint

```c++
template<class T>
concept signed_integral = std::is_integral_v<T> && std::is_signed_v<T>;
```