Các toán tử gán được dùng để gán giá trị cho biến.

```python
# Toán tử gán: =
number = 5
assert number == 5

# Gán nhiều giá trị cho nhiều biến
first_variable, second_variable = 0, 1
assert first_variable == 0
assert second_variable == 1

# Hoán đổi giá trị hai biến
first_variable, second_variable = second_variable, first_variable
assert first_variable == 1
assert second_variable == 0

# Các toán tử kết hợp với toán tử số học
# Toán tử: +=
number = 5
number += 3  # tương đương number = number + 3
assert number == 8

# Toán tử: -=
number = 5
number -= 3  # tương đương number = number - 3
assert number == 2

# Toán tử: *=
number = 5
number *= 3  # tương đương number = number * 3
assert number == 15

# Toán tử: /=
number = 8
number /= 4  # tương đương number = number / 4
assert number == 2

# Toán tử: %=
number = 5
number %= 3  # tương đương number = number % 3
assert number == 2

# Toán tử: //=
number = 5
number //= 3  # tương đương number = number // 3
assert number == 1

# Toán tử: **=
number = 5
number **= 3  # tương đương number = number ** 3
assert number == 125

# Toán tử: &=
number = 5  # 0b0101
number &= 3  # 0b0011
assert number == 1  # 0b0001

# Toán tử: |=
number = 5  # 0b0101
number |= 3  # 0b0011
assert number == 7  # 0b0111

# Toán tử: ^=
number = 5  # 0b0101
number ^= 3  # 0b0011
assert number == 6  # 0b0110

# Toán tử: >>=
number = 5
number >>= 3
assert number == 0  # (((5 // 2) // 2) // 2)

# Toán tử: <<=
number = 5
number <<= 3
assert number == 40  # 5 * 2 * 2 * 2
```

