Tập hợp là các cặp giá trị có dạng: "khóa": "giá trị" (`key: value`) được đặt giữa `{...}`. Các giá trị trong từ điển không có thứ tự, không được đánh chỉ mục, có thể thay đổi và xóa bỏ.

```python
# Tạo từ điển
fruits_dictionary = {
    'cherry': 'red',
    'apple': 'green',
    'banana': 'yellow',
}
assert isinstance(fruits_dictionary, dict)

# Tạo từ điển bằng hàm dict()
dictionary_via_constructor = dict([('sape', 4139), ('guido', 4127), ('jack', 4098)])
assert dictionary_via_constructor['sape'] == 4139
assert dictionary_via_constructor['guido'] == 4127
assert dictionary_via_constructor['jack'] == 4098

dictionary_for_string_keys = dict(sape=4139, guido=4127, jack=4098)
assert dictionary_for_string_keys['sape'] == 4139
assert dictionary_for_string_keys['guido'] == 4127
assert dictionary_for_string_keys['jack'] == 4098

# Tạo bằng Dict Comprehensions
dictionary_via_expression = {x: x**2 for x in (2, 4, 6)}
assert dictionary_via_expression[2] == 4
assert dictionary_via_expression[4] == 16
assert dictionary_via_expression[6] == 36

# Chúng ta truy cập các phần tử qua khóa của nó, giá trị của phần tử được trả về.
assert fruits_dictionary['apple'] == 'green'
assert fruits_dictionary['banana'] == 'yellow'
assert fruits_dictionary['cherry'] == 'red'

# Kiểm tra từ điển có chứa hoặc không chứa khóa nào không?
assert 'apple' in fruits_dictionary
assert 'pineapple' not in fruits_dictionary

# Có thể thay đổi giá trị của một phần tử
fruits_dictionary['apple'] = 'red'

# Có thể thêm một phần tử mới vào từ điển
fruits_dictionary['pineapple'] = 'yellow'
assert fruits_dictionary['pineapple'] == 'yellow'

# Hàm list() khi áp dụng lên từ điển, danh sách thu được chỉ là các khóa của từ điển
assert list(fruits_dictionary) == ['cherry', 'apple', 'banana', 'pineapple']

# Tương tự với hàm sorted() nhưng các khóa đã được sắp xếp
assert sorted(fruits_dictionary) == ['apple', 'banana', 'cherry', 'pineapple']

# Có thể xóa một phần tử bằng del
del fruits_dictionary['pineapple']
assert list(fruits_dictionary) == ['cherry', 'apple', 'banana']
```