Các toán tử bitwise hoạt động với các số ở cấp độ từng bit.

```python
# AND
# Đặt bit thành 1 nếu cả hai bit là 1
#
# Ví dụ:
# 5 = 0b0101
# 3 = 0b0011
assert 5 & 3 == 1  # 0b0001

# OR
# Đặt bit thành 1 nếu một trong hai bit là 1
#
# Ví dụ:
# 5 = 0b0101
# 3 = 0b0011
assert 5 | 3 == 7  # 0b0111

# NOT
# Đảo tất cả các bit
# ~n = -(n+1)
assert ~5 == -6

# XOR
# Đặt bit thành 1 nếu chỉ một trong hai bit là 1
#
# Ví dụ:
# 5 = 0b0101
# 3 = 0b0011
number = 5  # 0b0101
number ^= 3  # 0b0011
assert 5 ^ 3 == 6  # 0b0110

# Dịch sang phải n bit
# n bit ngoài cùng bên phải bị cắt đi
# n bit 0 được thêm vào đầu bên trái
#
# Ví dụ:
# 5 = 0b0101
assert 5 >> 1 == 2  # 0b0010
assert 5 >> 2 == 1  # 0b0001

# Dịch sang trái n bit
# n bit ngoài cùng bên trái bị cắt đi
# n bit 0 được thêm vào đầu bên phải
#
# Ví dụ:
# 5 = 0000 0101
assert 5 << 1 == 10  # 0b1010
assert 5 << 2 == 20  # 0b10100
```

