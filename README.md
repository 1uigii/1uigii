Writing low-level application code is very nice.

Reach me at 1uigi@protonmail.com (note the _one_)

```c++
struct luigi_t {
public:
    constexpr luigi_t(const luigi_t&) = default;
    friend constexpr luigi_t operator""uigi(unsigned long long value);
    static constexpr bool is_true(const luigi_t& l) {
        return l.value == 1;
    }

private:
    unsigned long long value;
    constexpr luigi_t(unsigned long long value) : value(value) { }
};

constexpr luigi_t operator""uigi(unsigned long long value) {
    return luigi_t { value };
}

constexpr luigi_t luigi = 1uigi;
static_assert(luigi_t::is_true(luigi));
```

<!---
1uigii/1uigii is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
