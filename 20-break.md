```python
# Kết thúc vòng lặp nếu tìm thấy số ta cần trong khoảng
# từ 0 đến 100
number_to_be_found = 42
# biến này ghi lại bao nhiều vòng lặp được chạy
number_of_iterations = 0

for number in range(100):
    if number == number_to_be_found:
        break
    else:
        number_of_iterations += 1

assert number_of_iterations == 42
```