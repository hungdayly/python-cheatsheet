Chuyển đổi kiểu trong Python được thực hiện thông qua các hàm tạo:

- `int()` - tạo số nguyên
- `float()` - tạo số thực
- `str()` - tạo chuỗi

```python
# Chuyển đổi thành số nguyên
assert int(1) == 1
assert int(2.8) == 2
assert int('3') == 3

# Chuyển đổi thành số thực
assert float(1) == 1.0
assert float(2.8) == 2.8
assert float("3") == 3.0
assert float("4.2") == 4.2

# Chuyển đổi thành chuỗi
assert str("s1") == 's1'
assert str(2) == '2'
assert str(3.0) == '3.0'
```