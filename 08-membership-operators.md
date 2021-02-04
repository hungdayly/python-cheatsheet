Các toán tử thành viên được dùng để kiểm tra một đối tượng có thuộc một dãy nào đó không.

```python
# Sử dụng danh sách sau để mô tả hoạt động của toán tử thành viên
fruit_list = ["apple", "banana"]

# Toán tử: in
# Trả về True nếu một dãy có chứa đối tượng

# Trả về True vì fruit_list chứa chuỗi "banana"
assert "banana" in fruit_list

# Toán tử: not in
# Trả về True nếu dãy không chứa đối tượng

# Trả về True vì fruit_list không chứa chuỗi "pineapple"
assert "pineapple" not in fruit_list
```