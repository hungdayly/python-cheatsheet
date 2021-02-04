Các toán tử đồng nhất được dùng để so sánh hai đối tượng, không phải kiểm tra nội dung mà kiểm tra xem chúng có thực sự cùng là một đối tượng, với cùng địa chỉ trong bộ nhớ không.

```python
# Ta mô tả các toán tử đồng nhất dựa trên các danh sách sau
first_fruits_list = ["apple", "banana"]
second_fruits_list = ["apple", "banana"]
third_fruits_list = first_fruits_list

# Toán tử: is
# Trả về True nếu hai toán hạng là cùng một đối tượng

# Ví dụ:
# first_fruits_list và third_fruits_list là cùng một đối tượng
assert first_fruits_list is third_fruits_list

# Toán tử: is not
# Trả về True nếu hai toán hạng là hai đội riêng biệt

# Ví dụ:
# first_fruits_list và second_fruits_list là hai đối tượng riêng biệt
# dù chúng có cùng nội dung
assert first_fruits_list is not second_fruits_list

# Sự khác nhau giữa "is" và "=="
# "==" trả về True nếu hai toán hạng có cùng nội dung
assert first_fruits_list == second_fruits_list
```