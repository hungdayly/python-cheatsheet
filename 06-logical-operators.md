Các toán tử lôgic được dùng để kết hợp nhiều điều kiện với nhau.

```python
# Cùng làm việc với những số này để mô tả cách hoạt động của các toán tử lôgic
first_number = 5
second_number = 10

# Toán tử and
# Trả về True nếu cả hai điều kiện đều đúng
assert first_number > 0 and second_number < 20

# Toán tử or
# Trả về True nếu có ít nhất một điều kiện đúng
assert first_number > 5 or second_number < 20

# Toán tử not
# Đảo kết quả, trả về False nếu điều kiện đúng.
assert not first_number == second_number
assert first_number != second_numer
```