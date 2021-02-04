```python
# Danh sách này chứa các số chẵn trong khoảng
even_numbers = []
# Danh sách này chứa những số khác (số lẻ) trong khoảng
rest_of_the_numbers = []

for number in range(0, 10):
    if number % 2 == 0:
        even_numbers.append(number)
        continue

    rest_of_the_numbers.append(number)

assert even_numbers == [0, 2, 4, 6, 8]
assert rest_of_the_numbers == [1, 3, 5, 7, 9]
```