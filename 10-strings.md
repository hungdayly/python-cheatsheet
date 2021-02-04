Bên cạnh số,Python cũng có thể làm việc với các chuỗi. Chuỗi có thể được biểu diễn bằng nhiều cách. Chúng có thể đặt giữa hai dấu nháy đơn (`'...'`) hoặc dấu nháy kép (`"..."`).

```python
# Chuỗi giữa hai dấu nháy kép
name_1 = "John"
# Chuỗi giữa hai dấu nháy đơn
name_2 = 'John'
# Kết quả của hai cách tạo hoàn toàn giống nhau
assert name_1 == name_2
assert isinstance(name_1, str)
assert isinstance(name_2, str)

# \ có thể dùng để chèn các dấu nháy
# \' dùng đề chèn dấu nháy đơn
single_quote_string = 'doesn\'t'
double_quote_string = "doesn't"
assert single_quote_string == double_quote_string

# \n nghĩa là xuống dòng
multiline_string = 'First line.\nSecond line.'

# Các chuỗi có thể được lập chỉ mục, với kí tự đầu tiên có chỉ số 0.
# Không có kiểu kí tự; một kí tự đơn giản là chuỗi có kích thước bằng 1.
# Vì -0 giống như 0, nên chỉ số âm được bắt đầu bằng -1

# | P | y | t | h | o | n |
#   0   1   2   3   4   5  
#  -6  -5  -4  -3  -2  -1

word = 'Python'
assert word[0] == 'P'  # Kí tự đầu tiên
assert word[5] == 'n'  # Kí tự thứ năm
assert word[-1] == 'n'  # Kí tự cuối cùng
assert word[-2] == 'o'  # Kí tự thứ hai từ cuối lên
assert word[-6] == 'P'  # Kí tự thứ sáu từ cuối lên

assert isinstance(word[0], str)

# Các chuỗi cũng hỗ trợ cắt lát. Trong khi lập chỉ mục
# cho phép lấy các kí tự độc lập, cắt lát cho phép lấy
# ra một chuỗi con

#  +---+---+---+---+---+---+
#  | P | y | t | h | o | n |
#  +---+---+---+---+---+---+
#  0   1   2   3   4   5   6
# -6  -5  -4  -3  -2  -1

assert word[0:2] == 'Py'
assert word[2:5] == 'tho'

# Nếu không có chỉ số đầu tiên, thì giá trị mặc định là 0
assert word[:2] == 'Py'  # lấy từ đầu chuỗi
# Nếu không có chỉ số thứ hai, thì giá trị mặc định là chiều dài chuỗi
assert word[4:] == 'on'  # lấy tới cuối chuỗi

# Nó khiến cho s[:i] + s[i:] luôn bằng s
assert word[:2] + word[2:] == 'Python'
assert word[:4] + word[4:] == 'Python'

# Chuỗi có thể trải trên nhiều dòng bằng cách sử dụng ba dấu nháy: """...""'
# hoặc '''...'''.
multi_line_string = '''
    First line
    Second line
'''

"""Các toán tử cơ bản

Các chuỗi có thể nối với nhau bằng toán tử +
và lặp lại với toán tử *: 3 lần 'un', sau đó là 'ium'
"""

assert 3 * 'un' + 'ium' == 'unununium'

# 'Py' 'thon'
python = 'Py' 'thon'
assert python == 'Python'

# Tính năng này đặc biệt hữu ích khi bạn muốn
# chia nhỏ một chuỗi dài
 text = (
    'Put several strings within parentheses '
    'to have them joined together.'
)
assert text == 'Put several strings within parentheses to have them joined together.'

# Nếu bạn muốn nối các biến hoặc một biến với một chuỗi, sử dụng +:
prefix = 'Py'
assert prefix + 'thon' == 'Python'

"""Các phương thức và hàm

Các hàm nhận đối số là một chuỗi và trả về một thông tin gì đó của chuỗi này.

Các phương thức được gọi từ chuỗi, và trả về một chuỗi mới chứ không thay đổi chuỗi hiện tại.
"""

hello_world_string = "Hello, World!"

# Phương thức strip() xóa các khoảng trắng ở đầu và cuối của chuỗi.
string_with_whitespaces = " Hello, World! "
assert string_with_whitespaces.strip() == "Hello, World!"

# Hàm len() trả về chiều dài của chuỗi
assert len(hello_world_string) == 13

# Phương thức lower() trả về chuỗi dưới dạng chữ thường
assert hello_world_string.lower() == 'hello, world!'

# Phương thức upper() trả về chuỗi dưới dạng viết hoa
assert hello_world_string.upper() == 'HELLO, WORLD!'

# Chuyển kí tự đầu thành chữ hoa
assert 'low letter at the beginning'.capitalize() == 'Low letter at the beginning'

# Chuyển kí tự đầu của mỗi từ thành chữ hoa
assert 'Welcome to my world'.title() == 'Welcome To My World'

# Trả về True nếu tất cả kí từ đều viết hoa
assert 'ABC'.isupper()
assert not 'AbC'.isupper()

# Trả về True nếu tất cả các kí tự là chữ cái
assert 'CompanyX'.isalpha()
assert not 'Company 23'.isalpha()

# Trả về True nếu tất cả các kí tự là chữ số
assert '1234'.isdecimal()
assert not 'a21453'.isdecimal()

# Phương thức replace() thay một chuỗi con, kí tự bằng một
# chuỗi con, kí tự khác
assert hello_world_string.replace('H', 'J') == 'Jello, World!'
assert 'I like bananas'.replace('bananas', 'apples') == 'I like apples'

# Phương thức split() chia chuỗi thành các chuỗi con nhờ một separator
assert hello_world_string.split(',') == ['Hello', ' World!']

# Nối các phần tử của một đối tượng có thể lặp với nhau với
# chuỗi đóng vai trò là separator
my_tuple = ('John', 'Peter', 'Vicky')
assert ', '.join(my_tuple) == 'John, Peter, Vicky'

# Tìm vị trí đầu tiên xuất hiện chuỗi con
assert 'Hello, welcome to my world'.find('welcome') == 7

# Trả về số lần xuất hiện của một chuỗi con
assert 'low letter at the beginning'.count('t) == 4

"""Định dạng chuỗi"""

# f-string
year = 2018
event = 'conference'
assert f'Results of the {year} {event}' == 'Results of the 2018 conference'

pi_value = 3.14159
assert f'The value of pi is {pi_value:.3f}.' == 'The value of pi is 3.142.'

table_data = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 7678}
table_string = ''
for name, phone in table_data.items():
    table_string += f'{name:7}==>{phone:7d}'

assert table_string == ('Sjoerd ==>   4127'
                        'Jack   ==>   4098'
                        'Dcab   ==>   7678')

# str.format()
assert 'We are {} who say "{}!"'.format('knights', 'Ni') == 'We are knights who say "Ni!"'

assert '{0} and {1}'.format('spam', 'eggs') == 'spam and eggs'
assert '{1} and {0}'.format('spam', 'eggs') == 'eggs and spam'

formatted_string = 'This {food} is {adjective}.'.format(
    food='spam',
    adjective='absolutely horrible'
)
assert formatted_string == 'This spam is absolutely horrible.'

formatted_string = 'The story of {0}, {1}, and {other}.'.format(
    'Bill',
    'Manfred',
    other='Georg'
)
assert formatted_string == 'The story of Bill, Manfred, and Georg.'

yes_votes = 42_572_654  # equivalent of 42572654
no_votes = 43_132_495   # equivalent of 43132495
percentage = yes_votes / (yes_votes + no_votes)
assert '{:-9} YES votes  {:2.2%}'.format(yes_votes, percentage) == ' 42572654 YES votes  49.67%'
```