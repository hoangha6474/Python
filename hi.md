
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
- Là một phương pháp lập trình tổ chức và thiết kế phần mềm dựa trên cách đối tượng (objects). Các đối tượng này là sự kết hợp của dữ liệu ( thuộc tính ) và các phương thức ( thao tác trên dữ liệu đó. OOP giúp mã nguồn dễ duy trì, mở rộng và tái sử dụng)

- **Lớp & Đối tượng:** `class` là bản thiết kế, `object` là thực thể.
- **Hàm khởi tạo:** `def __init__(self, ...):` dùng để thiết lập thuộc tính ban đầu.
- **Tính đóng gói (Encapsulation):**
    - `_attribute`: Protected (truy cập trong class và subclass).
    - `__attribute`: Private (truy cập nội bộ class).
- **Tính kế thừa (Inheritance):** `class Child(Parent):`.
- **Sử dụng `super()`:** Gọi hàm từ lớp cha.
- **Đa hình (Polymorphism):** Các đối tượng khác nhau phản hồi cùng một lời gọi hàm theo cách riêng.
- **Trừu tượng (Abstraction):** Sử dụng module `abc` và `@abstractmethod` để định nghĩa giao diện.

#### 1. Thành phần cơ bản

- **[[Class]] (Lớp):** Là một bản thiết kế (blueprint) để tạo ra các đối tượng.
	# Ví dụ: Một công ty có rất nhiều nhân viên ( Employee)
		- Employe:
			+ First_name
			+ last_name
			+ age
			+ salary

- **[[Object]] (Đối tượng):** Là một thực thể (instance) cụ thể được tạo ra từ lớp. Ví dụ: Lớp `Student` có thể tạo ra các đối tượng như `"Nam (AI19b02)"`.
- **[[Object Lifecycle]] (Vòng đời đối tượng):**
    1. **Creation (Khởi tạo):** Sử dụng phương thức `__init__`.
    2. **Usage (Sử dụng):** Truy cập thuộc tính và gọi phương thức.
    3. **Destruction (Hủy bỏ):** Kích hoạt phương thức `__del__` khi đối tượng bị xóa hoặc nằm ngoài phạm vi.

#### 2. Bốn cột trụ của OOP

###  [[Encapsulation]] (Tính đóng gói)

> [!info] Mục đích Gom nhóm dữ liệu và phương thức vào một đơn vị duy nhất, đồng thời hạn chế quyền truy cập trái phép.

- **Access Modifiers (Cấp độ truy cập):**
    - `Public`: Truy cập ở mọi nơi (ví dụ: `self.name`).
    - `_Protected`: Truy cập trong lớp và các lớp con (ví dụ: `self._grade`).
    - `__Private`: Chỉ truy cập được trong nội bộ lớp (ví dụ: `self.__balance`).
- **[[Getters và Setters]]:** Phương thức để truy cập và sửa đổi dữ liệu an toàn.
- **`@property` Decorator:** Kiểm soát truy cập dữ liệu nâng cao.

### 🧩 [[Abstraction]] (Tính trừu tượng)

- Tập trung vào việc ẩn đi các chi tiết triển khai phức tạp và chỉ hiển thị các tính năng thiết yếu.
- **Triển khai:** Sử dụng module `abc` (Abstract Base Classes) và `@abstractmethod`.

### 🌳 [[Inheritance]] (Tính kế thừa)

- Cho phép lớp con (child class) nhận lại các đặc điểm và hành vi của lớp cha (parent class).
- **Cú pháp:** `class Child(Parent):`.
- **[[Method Overriding]]:** Định nghĩa lại một phương thức của lớp cha ngay tại lớp con để thay đổi hành vi.
- **`super()`:** Dùng để gọi phương thức từ lớp cha (thường dùng trong `__init__`).

### 🎭 [[Polymorphism]] (Tính đa hình)

- Cho phép các đối tượng khác nhau phản hồi cùng một lời gọi hàm theo những cách riêng biệt của chúng.
- **Ví dụ:** Các lớp `GraduateStudent` và `UndergraduateStudent` đều có phương thức `details()`, nhưng mỗi lớp trả về nội dung khác nhau khi được gọi trong cùng một vòng lặp.

---

#### 3. Quản lý và Thiết kế hệ thống

- **Quản lý nhiều đối tượng:** Sử dụng các bộ sưu tập như **Lists** để lưu trữ và lặp qua các đối tượng nhằm thực hiện các thao tác hàng loạt.
- **[[Modular Design]] (Thiết kế mô-đun):** Chia chương trình thành các phần nhỏ giúp tái sử dụng mã (50%), dễ bảo trì (30%) và gỡ lỗi (20%).
- **[[Design Patterns]] (Mẫu thiết kế):** Các giải pháp mẫu cho vấn đề phổ biến như: Singleton (Khởi tạo), Adapter (Cấu trúc), Observer (Hành vi).

---

#### 4. Ví dụ Hệ thống Thư viện (Library System)

> [!example] Code minh họa

```python
class LibraryItem: # Lớp cha
    def __init__(self, title, item_id):
        self.__title = title # Private attribute
        self.__item_id = item_id

    def get_details(self): # Phương thức cơ sở
        return f"Title: {self.__title}, ID: {self.__item_id}"

class Book(LibraryItem): # Kế thừa
    def __init__(self, title, item_id, author):
        super().__init__(title, item_id) # Gọi lớp cha
        self.__author = author

    def get_details(self): # Ghi đè (Overriding)
        return super().get_details() + f", Author: {self.__author}"
```
