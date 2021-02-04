Một tuple giống hệt danh sách nhưng ta ta không thể thay đổi nội dung của một tuple được. Trong Python một tuple được viết giữa hai dấu ngoặc đơn.

Các tuple có những thuộc tính sau đây:
- Bạn không thể thay đổi các giá trị trong tuple.
- Bạn không thể xóa các giá trị trong tuple.

```python
"""Các tuple"""

# Tạo bằng danh sách đặt trong ()
fruits_tuple = ("apple", "banana", "cherry")

assert isinstance(fruits_tuple, tuple)
assert fruits_tuple[0] == "apple"
assert fruits_tuple[1] == "banana"
assert fruits_tuple[2] == "cherry"

# Tạo bằng hàm tuple()
fruits_tuple_via_constructor = tuple(("apple", "banana", "cherry"))
assert isinstance(fruits_tuple_via_constructor, tuple)

# Hàm len() trả về số phần tử của tuple
assert len(fruits_tuple_via_constructor) == 3

# Có thể bỏ qua dấu ngoặc đơn khi tạo tuple
another_tuple = 12345, 54321, 'hello!'
assert another_tuple == (12345, 54321, 'hello!')

# Tuple có thể lồng nhau
nested_tuple = another_tuple, (1, 2, 3, 4, 5)
assert nested_tuple == ((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))

# Tạo tuple trống
empty_tuple = ()
assert len(empty_tuple) == 0

# Tạo tuple có một phần từ, cần thêm dấu phảy chờ ở cuối
singleton_tuple = 'hello',  # <-- dấu phảy chờ
assert len(singleton_tuple) == 1
assert singleton_tuple == ('hello',)

# Tạo tuple không dùng dấu ngoặc còn được gọi là tuple packing
# tức nén nhiều giá trị vào một tuple
packed_tuple = 12345, 54321, 'hello!'

# Ngược lại có giải nén một tuple thành nhiều phần tử.
first_tuple_number, second_tuple_number, third_tuple_string = packed_tuple
assert first_tuple_number == 12345
assert second_tuple_number == 54321
assert third_tuple_string == 'hello!'

# Nén/giải nén một tuple có thể dùng để hoán đổi giá trị hai biến.
# Trong ví dụ này, một tuple trung gian được tạo ra.
first_number = 123
second_number = 456
first_number, second_number = second_number, first_number

assert first_number == 456
assert second_number == 123
```