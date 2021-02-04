Python có một số kiểu dữ liệu kết hợp, dùng để nhóm các giá trị với nhau. Kiểu thường dùng nhất là danh sách, được viết bằng cách liệt kê các phần tử giữa hai dấu ngoặc vuông. Danh sách có thể chứa các giá trị khác kiểu, nhưng thường thì chúng hay dùng để chứa các giá trị cùng kiểu hơn.

```python
# Danh sách rất giống mảng. Chúng có thể chứa bất cứ kiểu giá trị nào, và chứa
# bao nhiêu giá trị cũng được. Danh sách có thể lặp được một cách dễ dàng.
# Đây là ví dụ tạo một danh sách
squares = [1, 4, 9, 16, 25]
assert isinstance(squares, list)

# Danh sách cũng được lập chỉ mục và cắt lát như chuỗi
assert squares[0] == 1
assert squares[-1] == 25
assert squares[-3:] == [9, 16, 25]  # trả về danh sách con

# Tất cả các toán tử đều trả về một danh sách mới
# Lệnh sau trả về một bản sao chép của danh sách
assert squares[:] == [1, 4, 9, 16, 25]

# Danh sách cũng hỗ trợ toán tử nối
assert squares + [36, 49, 64, 81, 100] == [1, 4, 9, 15, 25, 36, 49, 64, 81, 100]

# Không như chuỗi, là bất biến, danh sách có thể biến đổi
# Ta có thể thay đổi nội dung của danh sách:
cubes = [1, 8, 27, 65, 125]  # sai phần tử thứ 4
cubes[3] = 64  # sửa lại
assert cubes == [1, 8, 27, 64, 125]

# Bạn cũng có thể thêm phần tử vào cuối chuỗi, bằng
# cách sử dụng phương thức append()
cubes.append(216)  # thêm 6 mũ 3
cubes.append(7 ** 3)  # thêm 7 mũ 3
assert cubes == [1, 8, 27, 64, 125, 216, 343]

# Có thể thay thế hoặc xóa cả một danh sách con
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
letters[2:5] = ['C', 'D', 'E']  # thay thế nhiều phần tử
assert letters == ['a', 'b', 'C', 'D', 'E', 'f', 'g']
letters[2:5] = []  # giờ xóa chúng
assert letters == ['a', 'b', 'f', 'g']
# Xóa toàn bộ phần tử của danh sách
letters[:] = []
assert letters == []

# Hàm len() trả về số phần tử của danh sách
letters = ['a', 'b', 'c', 'd']
assert len(letters) == 4

# Danh sách có thể nằm trong một danh sách khác
# ví dụ:
list_of_chars = ['a', 'b', 'c']
list_of_numbers = [1, 2, 3]
mixed_list = [list_of_chars, list_of_numbers]
assert mixed_list == [['a', 'b', 'c'], [1, 2, 3]]
assert mixed_list[0] == ['a', 'b', 'c']
assert mixed_list[0][1] == 'b'

"""Các phương thức"""

fruits = ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

# list.append(x)
# Thêm x vào cuối danh sách
fruits.append('grape')
assert fruits == ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana', 'grape']

# list.remove(x)
# Xóa phần tử x khỏi danh sách
fruits.remove('grape')
assert fruits == ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

# list.insert(i, x)
# Chèn x vào vị trị i, đẩy phần tử hiện tại ở vị trí i (nếu có) sang phải
fruits.insert(0, 'grape')
assert fruits == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

# list.index(x[, start[, end]])
# Tìm x trong đoạn start -> end-1 và trả về vị trí đầu tiên tìm thấy
assert fruits.index('grape') == 0
assert fruits.index('orange') == 1
assert fruits.index('banana') == 4
assert fruits.index('banana', 5) == 7

# list.count(x)
# Đếm số lần xuất hiện phần tử x trong danh sách
assert fruits.count('tangerine') == 0
assert fruits.count('banana') == 2

# list.copy()
# Trả về bản sao của danh sách
fruits_copy = fruits.copy()
assert fruits_copy == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']

# list.reverse()
# Đảo ngược danh sách
fruits_copy.reverse()
assert fruits_copy == [
    'banana',
    'apple',
    'kiwi',
    'banana',
    'pear',
    'apple',
    'orange',
    'grape',
]

# list.sort(key=None, reverse=False)
# Sắp xếp các phần tử trong danh sách
fruits_copy.sort()
assert fruits_copy == [
    'apple',
    'apple',
    'banana',
    'banana',
    'grape',
    'kiwi',
    'orange',
    'pear',
]

# list.pop([i])
# Xóa phần tử tại vị trí i và trả về phần tử bị xóa
# list.pop() xóa và trả về phần tử cuối cùng
assert fruits == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']
assert fruits.pop() == 'banana'
assert fruits == ['grape', 'orange', 'apple', 'pear', 'banana', 'kiwi', 'apple']

# list.clear()
# Xóa mọi phần tử khỏi danh sách
fruits.clear()
assert fruits == []

"""Lệnh del"""

numbers = [-1, 1, 66.25, 333, 333, 1234.5]

# del có thể được dùng để xóa phần tử khỏi danh sách
del numbers[0]
assert numbers == [1, 66.25, 333, 333, 1234.5]

del numbers[2:4]
assert numbers == [1, 66.25, 1234.5]

del numbers[:]
assert numbers == []

# del có thể được dùng để xóa danh sách
# sau lệnh này không thể truy cập biến numbers nữa
del numbers

"""List Comprehensions"""

# Ví dụ, giả sử bạn muốn tạo một danh sách các số chính phương, như sau:
squares = []
for number in range(10):
    squares.append(number ** 2)

assert squares == [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]   

# Cách trên tạo ra biến number, còn tồn tại sau khi vòng lặp kết thúc
# Cách sau không gây ra side effect như vậy:
squares = list(map(lambda x: x ** 2, range(10)))
assert squares == [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Nhưng thậm chí ngắn gọn hơn và dễ đọc hơn bằng list comprehensions:
squares = [x ** 2 for x in rang(10)]
assert squares == [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# List comprehension có thể mạnh mẽ hơn:
combinations = [(x, y) for x in [1, 2, 3] for y in [3, 1, 4] if x != y]
assert combinations == [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]

# nó tương đương hai vòng lặp lồng nhau như sau:
combinations = []
for first_number in [1, 2, 3]:
    for second_number in [3, 1, 4]:
        if first_number != second_number:
            combinations.append((first_number, second_number))

assert combinations == [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]

# Cùng xem một số ví dụ khác

vector = [-4, -2, 0, 2, 4]

# Tạo danh sách với các giá trị được nhân đôi
doubled_vector = [x * 2 for x in vector]
assert doubled_vector == [-8, -4, 0, 4, 8]

# Lọc các số âm
positive_vector = [x for x in vector if x >= 0]
assert positive_vector == [0, 2, 4]

# Gọi hàm với tất cả phần tử
abs_vector = [abs(x) for x in vector]
assert abs_vector == [4, 2, 0, 2, 4]

# Gọi phương thức với tất cả phần tử
fresh_fruit = ['  banana', '  loganberry ', 'passion fruit  ']
clean_fresh_fruit = [weapon.strip() for weapon in fresh_fruit]
assert clean_fresh_fruit == ['banana', 'loganberry', 'passion fruit']

# Tạo danh sách các tuple có dạng (number, square)
square_tuples = [(x, x ** 2) for x in range(6)]
assert square_tuples == [(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25)]

# Làm phẳng danh sách lồng nhau bằng hai "for"
vector = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flatten_vector = [num for elem in vector for num in elem]
assert flatten_vector == [1, 2, 3, 4, 5, 6, 7, 8, 9]

"""Nested List Comprehensions"""

# Xét ví dụ về một ma trận 3x4 tạo bằng danh sách chứa 3 danh sách kích thước 4
matrix = [
    [1, 2, 3, 4],
    [5, 6, 7, 8],
    [9, 10, 11, 12],
]

# Tạo ma trận chuyển vị
transposed_matrix = [[row[i] for row in matrix] for i in range(4)]
assert transposed_matrix == [
    [1, 5, 9],
    [2, 6, 10],
    [3, 7, 11],
    [4, 8, 12],
]

# nó tương đương với
transposed_matrix = []
for i in range(4):
    transposed_matrix.append([row[i] for row in matrix])

# hoặc chi tiết hơn, tương đương với:
transposed_matrix = []
for i in range(4):
    transposed_row = []
    for row in matrix:
        transposed_row.append(row[i])
    transposed_matrix.append(transposed_row)


# Thực tế, bạn nên sử dụng các tích hợp để thực hiện những dòng lệnh phức tạp
# Hàm zip() dùng rất tốt cho trường hợp này
assert list(zip(*matrix)) == [
    (1, 5, 9),
    (2, 6, 10),
    (3, 7, 11),
    (4, 8, 12),
]
```