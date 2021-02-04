Lệnh "try" được dùng để xử lý các ngoại lệ.

Khi có lỗi xảy ra, hoặc một ngoại lệ như cách chúng ta gọi nó, Python thường sẽ dừng chương trình và đưa ra một thông báo lỗi. Ta có thể chủ động xử lý những ngoại lệ này bằng lệnh "try".

Lệnh try gồm nhiều khối:

- Khối "try" cho phép bạn kiểm tra một khối lệnh xem có lỗi hay không.
- Khối "except" cho phép bạn xử lý lỗi xuất hiện ở khối "try".
- Khối "else" cho phép bạn chạy mã nào đó khi không có lỗi xuất hiện.
- Khối "finally" cho phép bạn chạy mã nào đó dù có lỗi hay không có lỗi.

```python
# Khối try này sẽ sinh một lỗi, bởi vì x chưa được định nghĩa
exception_has_been_caught = False

try:
    print(not_existing_variable)
except NameError:
    exception_has_been_caught = True

assert exception_has_been_caught

# Bạn có thể định nghĩa nhiều khối except, để xử lý từng loại lỗi cụ thể
exception_message = ''

try:
    print(not_existing_variable)
except NameError:
    exception_message = 'Variable is not defined'

assert exception_message == 'Variable is not defined'

# Bạn có thể định nghĩa khối else để chạy các đoạn mã khi không có lỗi xảy ra
message = ''

try:
    message += 'Success.'
except NameError:
    message += 'Something went wrong.'
else:
    message += 'Nothing went wrong.'

assert message == 'Success.Nothing went wrong.'

# Khối finally, rất đặc biệt, vì nó luôn được chạy dù khối try có gây
# ra lỗi hay không
message = ''
try:
    print(not_existing_variable)
except NameError:
    message += 'Something went wrong.'
finally:
    message += 'The "try except" is finished.'

assert message == 'Something went wrong.The "try except" is finished.'
```