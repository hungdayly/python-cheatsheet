Tập hợp gồm nhiều phần tử không lặp lại, không được sắp xếp và không được đánh chỉ mục. Trong Python các tập hợp được viết giữa hai dấu ngoặc `{...}`.

Các tập hợp trong Python biểu diễn khái niệm tập hợp trong Toán học, nó hỗ trợ ta thực hiện các phép toán tập hợp như: giao, hợp, hiệu,...

```python
"""Tạo tập hợp"""

# Tạo tập hợp bằng {...}
fruits_set = {"apple", "banana", "cherry"}
assert isinstance(fruits_set, set)

# Tạo tập hợp bằng set()
fruits_set_via_constructor = set(("apple", "banana", "cherry"))
assert isinstance(fruits_set_via_constructor, set)

"""Các phương thức và hàm"""

fruits_set = {"apple", "banana", "cherry"}

# Kiểm tra bằng toán tử in và not in
assert "apple" in fruits_set
assert "pineapple" not in fruits_set

# Sử dụng len() để biết số phần tử của tập hợp
assert len(fruits_set) == 3

# Sử dụng phương thức add() để thêm phần tử vào tập hợp
fruits_set.add("pineapple")
assert "pineapple" in fruits_set
assert len(fruits_set) == 4

# Sử dụng phương thức remove() để xóa một phần tử
fruits_set.remove("pineapple")
assert "pineapple" not in fruits_set
assert len(fruits_set) == 3

"""Các phép toán"""

# Sử dụng hạp tập hợp sau làm minh họa
first_char_set = set('abracadabra')
second_char_set = set('alacazam')

assert first_char_set == {'a', 'r', 'b', 'c', 'd'}  # loại bỏ kí tự trùng lặp
assert second_char_set == {'a', 'l', 'c', 'z', 'm'}  # loại bỏ kí tự trùng lặp

# Kí tự trong từ thứ nhất nhưng không có trong từ thứ hai
assert first_char_set - second_char_set == {'r', 'b', 'd'}

# Kí tự trong từ thứ nhất hoặc trong từ thứ hai
assert first_char_set | second_char_set == {'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}

# Kí tự chung của hai từ
assert first_char_set & second_char_set == {'a', 'c'}

# Kí tự chỉ thuộc từ thứ nhất hoặc chỉ thuộc từ thứ hai
assert first_char_set ^ second_char_set == {'r', 'd', 'b', 'm', 'z', 'l'}

"""Comprehensions"""

word = {char for char in 'abracadabra' if char not in 'abc'}
assert word == {'r', 'd'}
```