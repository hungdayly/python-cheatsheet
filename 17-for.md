```python
"""Vòng lặp for"""

# Tính tổng chiều dài nhiều chuỗi
words = ['cat', 'window', 'defenestrate']
words_length = 0

for word in words:
    words_length += len(word)
assert words_length == (3 + 6 + 12)

# Nếu trong vòng lặp for bạn cần thay đổi dãy đang lặp, bạn nên
# tạo một bản sao trước khi thao tác.
for word in words[:]:
    if len(words) > 6:
        words.insert(0, word)
assert words == ['defenestrate', 'cat', 'window', 'defenestrate']

# Nếu cần lặp một dãy số, nên sử dụng hàm range()
iterated_numbers = []

for number in range(5):
    iterated_numbers.append(number)
assert iterated_numbers == [0, 1, 2, 3, 4]

# Để lặp qua các chỉ số của phần tử trong dãy, bạn có thể kết hợp range() và len() như sau:
words = ['Mary', 'had', 'a', 'little', 'lamb']
concatenated_string = ''

for word_index in range(len(words)):
    concatenated_string += words[word_index] + ' '

assert concatenated_string == 'Mary had a little lamb '

# hoặc đơn giản hơn là sử dụng hàm enumerate()
concatenated_string = ''

for word_index, word in enumerate(words):
    concatenated_string += word + ' '

assert concatenated_string == 'Mary had a little lamb '

# Khi lặp qua từ điển, khóa và giá trị tương ứng có thể
# được lặp cùng lúc nhờ phương thức items()
knights_names = []
knights_properties = []

knights = {'gallahad': 'the pure', 'robin': 'the brave'}
for key, value in knights.items():
    knights_names.append(key)
    knights_properties.append(value)

assert knights_names == ['gallahad', 'robin']
assert knights_properties == ['the pure', 'the brave']

# Khi lặp qua một dãy hỗ trợ đánh chỉ mục (như danh sách, tuple),
# vị trí và giá trị tương ứng có thể được lặp cùng lúc nhờ hàm enumerate()
indices = []
values = []
for index, value in enumerate(['tic', 'tac', 'toe']):
    indices.append(index)
    values.append(value)

assert indices == [0, 1, 2]
assert values == ['tic', 'tac', 'toe']

# Để lặp trên hai hay nhiều dãy cùng lúc, các mục của từng dãy được ghép
# cặp với nhau nhờ hàm zip()
questions = ['name', 'quest', 'favorite color']
answers = ['lancelot', 'the holy grail', 'blue']
combinations = []

for question, answer in zip(questions, answers):
    combinations.append('What is your {0}?  It is {1}.'.format(question, answer))

assert combinations == [
    'What is your name?  It is lancelot.',
    'What is your quest?  It is the holy grail.',
    'What is your favorite color?  It is blue.',
]

"""Hàm range

Khi cần lặp lại một danh sách các số, đặc biệt là danh sách gồm rất nhiều số,
bạn nên sử dụng hàm tích hợp sẵn là range().

Hàm range() tạo nên một đối tượng có thể lặp (iterable).

Cú pháp range(start, end, step): tạo ra dãy số bắt đầu từ "start" đến (không
bao gồm) "end", khoảng cách giữa hai số liên tiếp là "step"
"""

assert list(range(5)) == [0, 1, 2, 3, 4]

assert list(range(5, 10)) == [5, 6, 7, 8, 9]
assert list(range(0, 10, 3)) == [0, 3, 6, 9]
assert list(range(-10, -100, -30)) == [-10, -40, -70]
```