Có 3 kiểu số trong Python:

1. `int`: số nguyên (ví dụ, `2`, 4`, `20`)
    - `bool`: kiểu lôgic thực ra là kiểu nguyên với `True` được xem là `1` và `False` được xem là `0`.
2. `float`: số thực dấu chấm động (ví dụ, `5.0`, `1.6`)
3. `complex`: số phức (ví dụ, `5+6j`, `4-3j`)

```python
"""Kiểu số nguyên

Int, hoặc integer, là một số nguyên, có thể dương hoặc âm,
có chiều dài không giới hạn
"""

positive_integer = 1
negative_integer = -3255522
big_integer = 35656222554887711

assert isinstance(positive_integer, int)
assert isinstance(negative_integer, int)
assert isinstance(big_integer, int)

"""Kiểu lôgic

Kiểu lôgic biểu diễn các giá trị chân lý True và False. Kiểu lôgic
là kiểu con của kiểu số nguyên và các giá trị lôgic được coi như 0
và 1. True được coi là 1 còn False được coi là 0.

Trong các biểu thức số học True được chuyển thành 1 còn False được
chuyển thành 0. Nhưng khi chuyển thành chuỗi thì True thành "True"
còn False thành "False"
"""

true_boolean = True
false_boolean = False

assert true_boolean
assert not false_boolean

assert isinstance(true_boolean, bool)
assert isinstance(false_boolean, bool)

# Chuyển đổi kiểu lôgic sang chuỗi
assert str(true_boolean) == "True"
assert str(false_boolean) == "False"

"""Kiểu số thực

Kiểu số thực, hay số thực dấu chấm động là một số dương hoặc âm,
có phần lẻ sau dấu chấm.
"""

float_number = 7.0
# Cách khác là sử dụng hàm float()
float_number_via_function = float(7)
float_negative = -35.59

assert float_number == float_number_via_function
assert isinstance(float_number, float)
assert isinstance(float_number_via_function, float)
assert isinstance(float_negative, float)

# Có thể dùng "e" để viết các số rất lớn hoặc rất nhỏ,
# "e" ám chỉ lũy thừa của 10

# Có thể dùng "e" hoặc "E"
float_with_small_e = 35e3
float_with_big_e = 12E4
assert float_with_small_e == 35000
assert float_with_big_e == 120000

# Viết các số rất lớn
mass_of_earth = 6e24
assert isinstance(mass_of_earth, float)

# Viết các số rất nhỏ
fundamental_unit_of_charge = 1.6e-19
assert isinstance(fundamental_unit_of_charge, float)

"""Kiểu số phức

Số phức có dạng a + bj, trong đó a là phần thực, còn b là phần ảo,
j là đơn vị ảo.

Ta có thể thực hiện các phép toán cơ bản với số phức như phép cộng,
và phép nhân.
"""

complex_number_1 = 5 + 6j
complex_number_2 = 3 - 2j

assert isinstance(complex_number_1, complex)
assert isinstance(complex_number_2, complex)
assert complex_number_1 * complex_number_2 == 27 + 8j
```