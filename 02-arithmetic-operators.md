Các toán tử số học được sử dụng với các giá trị số và thực hiện các phép tính số học thông thường.

```python
# Phép cộng
assert 5 + 3 == 8

# Phép trừ
assert 5 - 3 == 2

# Phép nhân
# Nhân hai số nguyên tạo ra một số nguyên
assert 5 * 3 == 15
assert isinstance(5 * 3, int)
# Nhân với số thực tạo ra số thực
assert 5 * 3.0 == 15.0
assert isinstance(5 * 3.0, float)

# Phép chia
# Phép chia luôn tạo ra một số thực
assert 5 / 3 == 1.6666666666666667
assert 8 / 4 == 2
assert isinstance(5 / 3, float)
assert isinstance(8 / 4, float)

# Phép chia lấy phần nguyên
# Kết quả phép chia được làm tròn tới số nguyên nhỏ hơn gần nhất
assert 5 // 3 == 1 # 1.6666666666666667 -> 1
assert 6 // 3 == 2 # 2.0 -> 2
assert 7 // 3 == 2 # 2.3333333333333335 -> 2
assert 9 // 3 == 3 # 3.0 -> 3
# Chú ý với số âm
assert 5 // -3 == -2 # -1.6666666666666667 -> -2
# Kết quả luôn là một số nguyên
assert isinstance(5 // 3, int)

# Phép chia lấy số dư
assert 5 % 3 == 2 # 5 chia 3 dư 2
# Thuật toán
# Trước tiên tính 5 // 3
assert 5 // 3 == 1
# Sau đó lấy kết quả này nhân với số chia
assert 1 * 3 = 3
# Cuối cùng lấy số bị chia trừ kết quả trên
assert 5 - 3 == 2
# Một ví dụ với số âm
assert 5 % -3 == -1
# Thuật toán
# Bước 1
assert 5 // -3 == -2
# Bước 2
assert -2 * -3 == 6
# Bước 3
assert 5 - 6 == -1

# Lũy thừa
assert 5 ** 3 == 125 # 5 mũ 3
assert 2 ** 3 == 8
assert 2 ** 4 == 16
assert 2 ** 5 == 32
assert 2 ** 0.5 == 1.4142135623730951
assert -2 ** 0.5 == -1.4142135623730951
assert isinstance(5 ** 3, int)
assert isinstance(2 ** 0.5, float)
```