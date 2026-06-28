
# Tổng Hợp Cú Pháp Python (Python for Everybody)

## 1. Cơ Bản & Biểu Thức (Basics & Expressions)

- **Gán giá trị:** Sử dụng dấu `=` để gán giá trị cho biến.
- **Nhập dữ liệu:** `input()` trả về một chuỗi (string).
- **Xuất dữ liệu:** `print()` dùng để hiển thị kết quả.
- **Chú thích (Comments):** Sử dụng dấu `#` cho các dòng ghi chú.
- **Toán tử số học:**
    - `+`, `-`, `*`, `/` (Cộng, trừ, nhân, chia).
    - `**` (Lũy thừa), `%` (Chia lấy dư).
- **Ép kiểu & Kiểm tra kiểu:**
    - `type()`: Kiểm tra kiểu dữ liệu của biến.
    - `int()`, `float()`, `str()`: Chuyển đổi giữa các kiểu dữ liệu.

## 2. Câu Lệnh Điều Kiện (Conditionals)

- **Cấu trúc If/Elif/Else:**

```python
if x < 10:
    print('Small')
elif x < 20:
    print('Medium')
else:
    print('Large')
```

- **Toán tử so sánh:** `==`, `!=`, `<`, `>`, `<=`, `>=`.
- **Xử lý lỗi (Try/Except):** Giúp chương trình không bị dừng đột ngột khi gặp lỗi.

```python
try:
    ival = int(rawstr)
except:
    ival = -1
```

## 3. Hàm (Functions)

- **Định nghĩa hàm:** Sử dụng từ khóa `def`.
- **Giá trị trả về:** Sử dụng `return` để gửi kết quả từ hàm ra ngoài.
- **Hàm tích hợp (Built-in):** `max()`, `min()`, `len()`, `sum()`.

## 4. Vòng Lặp (Iterations)

- **Vòng lặp `while`:** Lặp không xác định cho đến khi điều kiện sai.
- **Vòng lặp `for`:** Lặp xác định qua một tập hợp hoặc chuỗi.
- **Điều khiển vòng lặp:**
    - `break`: Thoát khỏi vòng lặp ngay lập tức.
    - `continue`: Bỏ qua phần còn lại của lần lặp hiện tại và bắt đầu lần lặp tiếp theo.
- **Toán tử logic:** `is`, `is not` (mạnh hơn `==`), `None` (hằng số đại diện cho sự trống rỗng).
#### Vòng lặp lồng nhau
```python
	for i in range(3):
		print("Vong for ngoai khi i = ", i)
		for j in range(2):
		print(i, j)
```
Output:
```text
Vong for ngoai khi i = 0  
0 0  
0 1  
Vong for ngoai khi i = 1  
1 0  
1 1  
Vong for ngoai khi i = 2  
2 0  
2 1
```
## 5. Chuỗi (Strings)

- **Chỉ số (Indexing):** `s` lấy ký tự đầu tiên.
- **Cắt chuỗi (Slicing):** `s[start:end]` (lấy từ start đến sát end).
- **Kiểm tra sự tồn tại:** `in` trả về True/False.
- **Phương thức chuỗi:**
    - `.lower()`, `.upper()`: Chuyển đổi hoa/thường.
    - `.find()`: Tìm vị trí chuỗi con.
    - `.replace(old, new)`: Thay thế nội dung.
    - `.strip()`, `.lstrip()`, `.rstrip()`: Loại bỏ khoảng trắng.
    - `.startswith()`: Kiểm tra tiền tố.

## 6. Tệp Tin (Files)

- **Mở tệp:** `handle = open(filename, mode)` (mode 'r' là đọc, 'w' là ghi).
- **Ký tự dòng mới:** `\n`.
- **Đọc tệp:**
    - Dùng vòng lặp `for line in handle:` để đọc từng dòng.
    - `handle.read()` để đọc toàn bộ tệp vào một chuỗi đơn.

## 7. Danh Sách (Lists)

- **Đặc điểm:** Biến đổi được (mutable) và có thứ tự.
- **Thao tác:**
    - `.append(value)`: Thêm phần tử vào cuối.
    - `.sort()`: Sắp xếp danh sách tại chỗ.
    - `range(len(list))`: Tạo chỉ số để lặp.
    - `.split()`: Chia chuỗi thành danh sách (rất quan trọng để xử lý dữ liệu).
    - `+`: Nối hai danh sách.

## 8. Từ Điển (Dictionaries)

- **Đặc điểm:** Lưu trữ cặp `key:value`, không có thứ tự.
- **Thao tác:**
    - `.get(key, default)`: Lấy giá trị của key, nếu không có trả về giá trị mặc định (tránh lỗi `KeyError`).
    - `.keys()`, `.values()`, `.items()`: Lấy danh sách khóa, giá trị hoặc cặp (key, value).

## 9. Tuple

- **Đặc điểm:** Không thể biến đổi (immutable), hiệu quả hơn List.
- **Gán gộp (Assignment):** `(x, y) = (4, 'fred')`.
- **So sánh:** So sánh từng phần tử từ trái qua phải cho đến khi tìm thấy sự khác biệt.

## 10. Lập Trình Hướng Đối Tượng (OOP)

- **Lớp & Đối tượng:** `class` là bản thiết kế, `object` là thực thể.
- **Hàm khởi tạo:** `def __init__(self, ...):` dùng để thiết lập thuộc tính ban đầu.
- **Tính đóng gói (Encapsulation):**
    - `_attribute`: Protected (truy cập trong class và subclass).
    - `__attribute`: Private (truy cập nội bộ class).
- **Tính kế thừa (Inheritance):** `class Child(Parent):`.
- **Sử dụng `super()`:** Gọi hàm từ lớp cha.
- **Đa hình (Polymorphism):** Các đối tượng khác nhau phản hồi cùng một lời gọi hàm theo cách riêng.
- **Trừu tượng (Abstraction):** Sử dụng module `abc` và `@abstractmethod` để định nghĩa giao diện.

