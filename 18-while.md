```python
# Tính 2 mũ 5 bằng vòng lặp while
number = 2
power = 5

result = 1

while power > 0:
    result *= number
    power -= 1

assert result == 32    
```