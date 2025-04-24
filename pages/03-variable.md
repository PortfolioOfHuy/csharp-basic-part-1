# Variable & Data type

<v-clicks>

- **Biến** dùng để chứa **dữ liệu** mà bạn muốn lưu trữ và sử dụng trong chương trình của mình.
- **Kiểu dữ liệu** xác định loại dữ liệu mà biến có thể lưu trữ.

</v-clicks>

---
zoom: 0.9
---

# Các Giá Trị Đơn Giảm Có Thể Biểu Diễn

<v-clicks>

1. **Chuỗi (String)**: Được bao bọc bởi dấu nháy đôi ("). Ví dụ: `"Xin chào!"`, `"Hồ Chí Minh"`.
2. **Số Nguyên (Integet)**: Là giá trị số không có phần thập phân. Ví dụ: `25`, `-10`.
3. **Số thực (Floating-point)**: Có phần thập phân, dùng dấu chấm (.) để phân tách. Ví dụ: `19.99`, `3.14`.
4. **Boolean**: Có hai trạng thái: đúng (true) hoặc sai (false). Ví dụ: `true`, `false`.
5. **Ký Tự (Character)**: Được bao bọc bởi dấu nháy đơn (') và chứa một ký tự duy nhất. Ví dụ: `'A'`, `'b'`.

</v-clicks>

---

# Variables (biến)

<v-clicks>

- Biến là một "hộp" trong bộ nhớ máy tính, nơi bạn có thể lưu trữ dữ liệu. Điều này giúp chương trình của bạn có thể ghi nhớ và xử lý thông tin một cách dễ dàng.
- Mỗi biến có mọt kiểu dữ liệu, cho biết loại thông tin mà nó có thể chứa, như số, văn bản hay giá trị đúng/sai.
- **Kiểu Dữ Liệu**:
    - **Số nguyên (int)**: Lưu trữ số nguyên, ví dụ: `25`, `-10`.
    - **Số Thực (float, double)**: Lưu trữ số có phần thập phần, ví dụ: `19.99`, `3.14`.
    - **Chuỗi (string)**: Lưu trữ văn bản, ví dụ: `"Xin chào!"`.
    - **Boolean (bool)**: Chỉ có hai giá trị: đúng (true) hoặc sai (false).

</v-clicks>

---
zoom: 0.9
---

# Khai báo biến

<v-clicks>

1. Để khai báo một biến, bạn sử dụng cú pháp như sau:

```bash
kiểu_dữ_liệu tên_biến;
```

2. Khai báo biến và gán giá trị cho nó trong cùng một bước:

```bash
kiểu_dữ_liệu tên_biến = giá_trị_ban_đầu;
```

3. Khai báo một biến có tên là `hello` với kiểu dữ liệu là `sbyte` (chứa giá trị từ -128 đến 127):

```cs
sbyte hello = 123;
```

4. Thay đổi giá trị của biến:

```cs
sbyte hello = 123;                      // Khai báo và gán giá trị ban đầu
Console.WriteLine(hello);               // In ra 123
hello = 100;                            // Gán giá trị mới
Console.WriteLine(hello);               // In ra 100
hello = -50;                            // Gán giá trị âm
Console.WriteLine(hello);               // In ra -50
```

- Kiểu dữ liệu `sbyte` sử dụng 8 bit để lưu trữ thông tin, cho phép biểu diễn 256 giá trị khác nhau từ -128 đến 127!

</v-clicks>

---
zoom: 0.9
---

# Các Loại Kiểu Dữ Liệu (Datatypes)

<v-clicks>

1. **Built-in Types**: Các kiểu dữ liệu cơ bản có sẵn trong C#, giúp lập trình viên dễ dàng làm việc với dữ liệu.
    - **Số Nguyên (int)**: Ví dụ: `25`, `-10`.
    - **Số Thực (double)**: Ví dụ: `3.14`, `19.99`.
    - **Ký Tự (char)**: Ví dụ: `'A'`, `'B'`.
    - **Giá Trị Đúng/Sai (bool)**: Giá trị là đugns (`true`) hoặc sai (`false`).
2. **User-defined Types**: Kiểu dữ liệu do lập trình viên tự định nghĩa theo nhu cầu cụ thể.
    - **Class**: Định nghĩa cho đối tượng với thuộc tính và phương thức.
    - **Struct**: Kiểu dữ liệu tổng hợp chứa nhiều loại dữ liệu khác nhau.
    - **Enum**: Tập hợp các hằng số liên quan, giúp mã nguồn rõ ràng hơn.

- **Lưu ý**: Việc hiểu rõ các kiểu dữ liệu giúp lập trình viên chọn lựa và sử dụng chúng hiệu quả hơn trong quá trình phát triển phần mềm.

</v-clicks>

---
zoom: 0.9
---

# Built-in Types - Kiểu Số Nguyên

<v-clicks>

- Kiểu số nguyên (Integer types) dùng để lưu trữ các giá trị số nguyên (không có phần thập phân).
- **Các Kiểu Dữ Liệu Số Nguyên**:
    - **sbyte**: -128 đến 127 (8 bit)
    - **byte**: 0 đến 255 (8 bit)
    - **short**: -32,768 đến 32,767 (16 bit)
    - **ushort**: 0 đến 65,535 (16 bit)
    - **int**: -2,147,483,648 đến 2,147,483,647 (32 bit)
    - **uint**: 0 đến 4,294,967,295 (32 bit)
    - **long**: -9,223,372,036,854,775,808 đến 9,223,372,036,854,775,807 (64 bit)
    - **ulong**: 0 đến 18,446,744,073,709,551,615 (64 bit)
- Các kiểu dữ liệu có tiền tố "u" (như `uint`, `ulong`, `ushort`) là **unsigned** (không dấu), chỉ chứa các giá trị không âm (từ 0 trở lên).

</v-clicks>

---
zoom: 0.9
---

# Khai Báo và Gán Giá Trị cho Các Số Nguyên

<v-clicks>

```cs
sbyte smallValue = -128;                // Giá trị trong khoảng từ -128 đến 127
Console.WriteLine(smallValue);

byte byteValue = 255;                   // Giá trị trong khoảng từ 0 đến 255
Console.WriteLine(byteValue);

short shortValue = 32767;               // Giá trị trong khoảng từ -32,768 đến 32,767
Console.WriteLine(shortValue);

ushort ushortValue = 65535;             // Giá trị trong khoảng từ 0 đến 65,535
Console.WriteLine(ushortValue);

int intValue = -2147483648;             // Giá trị trong khoảng từ -2,147,483,648 đến 2,147,483,647
Console.WriteLine(intValue);

uint uintValue = 4294967295;            // Giá trị trong khoảng từ 0 đến 4,294,967,295
Console.WriteLine(uintValue);
```

- Hãy thử thách bản thân bằng cách thay đổi giá trị của các biến này ra ngoài khoảng cho phép có thể chứa.
- Ví dụ, bạn có thể thử gán `sbyte` một giá trị như `130` hoặc `-130`, hoặc với `uint`, hãy thử gán `-1`.
- Khi bạn làm điều này, **compiler** sẽ phát hiện và báo lỗi ngay lập tức!

</v-clicks>

---

# In Dữ Liệu Đẹp Mắt Hơn

<v-clicks>

- Khi bạn muốn hiển thị giá trị của một biến, việc sử dụng `Console.WriteLine` là một cách tuyệt với để đưa thông tin đến người dùng.
- Dưới đây là cách sử dụng phương thức này để in giá trị của biến `smallValue`:

```cs
sbyte smallValue = -128;                                // Giá trị trong khoảng từ -128 đến 127
Console.WriteLine("smallValue: " + smallValue);
```

- Trong câu lệnh `"smallValue: " + smallValue`, phần chuỗi `"smallValue: "` mô tả tên biến và dấu `+` kết hợp nó với giá trị của biến `smallValue`, tạo ra một thông điệp rõ ràng khi in ra.

</v-clicks>

---

# Built-int types - Thường Sử Dụng

<v-click>

```cs
string greeting = "Xin chào";   // Chuỗi văn bản, được bao quanh bởi nháy đôi.

char initial = 'A'; // Ký tự Unicode, được bao quanh bởi nháy đơn.

bool isActive = true;   // Boolean, chỉ nhận giá trị true hoặc false.
bool isFinished = false;    // Boolean, chỉ nhận giá trị true hoặc false.

float piApproximation = 3.14f;  // Số thực 32-bit, chữ 'f' chỉ định kiểu float.

double eulerNumber = 2.71828;   // Số thực 64-bit.

decimal accountBalance = 1000.75m;  // Số thập phân 128-bit, chữ 'm' chỉ định kiểu decimal

// In ra giá trị của các biến để kiểm tra
Console.WriteLine("string: " + greeting);
Console.WriteLine("char: " + initial);
Console.WriteLine("bool: " + isActive);
Console.WriteLine("bool: " + isFinished);
Console.WriteLine("float: " + piApproximation);
Console.WriteLine("double: " + eulerNumber);
Console.WriteLine("decimal: " + accountBalance);
```

</v-click>

---

# Xác Định Kiểu Dữ Liệu cho Biến

<v-clicks>

- Thực hành xác định kiểu dữ liệu phù hợp cho các biến dựa trên giá trị mà chúng có thể chứa. Hãy khai báo các biến và gán giá trị cho chúng, sau đó xác định kiểu dữ liệu chính xác cho mỗi biến.
- Khai báo các biến sau và xác định kiểu dữ liệu phù hợp:
    - Một biến lưu trữ tên người dùng (ví dụ: "Nguyen Van A").
    - Một biến lưu trữ số tuổi (ví dụ: 25).
    - Một biến lưu trữ ký tự đầu tiên của tên (ví dụ: 'N').
    - Một biến kiểm tra xem người dùng có còn hoạt động hay không (ví dụ: true hoặc false).
    - Một biến lưu trữ số tiền trong tài khoản (ví dụ: 1000.50).
- Viết mã C# để khai báo và gán giá trị cho các biến.
- **Câu hỏi**:
    - Bạn đã chọn kiểu dữ liệu nào cho mỗi biến? Giải thích lý do tại sao bạn chọn kiểu đó.
    - Có kiểu dữ liệu nào khác mà bạn có thể sử dụng không?

</v-clicks>

---

# Code tham khảo

```cs
// Biến lưu trữ tên người dùng - kiểu string
string userName = "Nguyen Van A";

// Biến lưu trữ số tuổi - kiểu int
int age = 25;

// Biến lưu trữ ký tự đầu tiên của tên - kiểu char
char firstInitial = 'N';

// Biến kiểm tra người dùng có còn hoạt động hay không - kiểu bool
bool isActive = true;

// Biến lưu trữ số tiền trong tài khoản - kiểu double
double accountBalance = 1000.50;

// In ra màn hình các giá trị và kiểu dữ liệu
Console.WriteLine($"Tên người dùng: {userName} (kiểu: {userName.GetType().Name})");
Console.WriteLine($"Tuổi: {age} (kiểu: {age.GetType().Name})");
Console.WriteLine($"Ký tự đầu tiên: {firstInitial} (kiểu: {firstInitial.GetType().Name})");
Console.WriteLine($"Còn hoạt động: {isActive} (kiểu: {isActive.GetType().Name})");
Console.WriteLine($"Số dư tài khoản: {accountBalance} (kiểu: {accountBalance.GetType().Name})");

Console.ReadLine(); // Đợi người dùng nhấn phím để xem kết quả
```

---

# Strongly Typed

<v-clicks>

1. Trong C#, mỗi biến có kiểu dữ liệu cụ thể. Nếu bạn cố gắng gán giá trị không tương thích với kiểu dữ liệu, chương trình sẽ gặp lỗi. Ví dụ:

```cs
sbyte hello = 123;      // Đúng
hello = "Xin chào";     // Sai! Lỗi biên dịch
```

- Ở đây, việc gán một chuỗi cho biến `hello` sẽ gây ra lỗi vì `hello` đã được khai báo là kiểu `sbyte`.

2. **Khái Niệm "Strongly Typed"**: C# là một ngôn ngữ lập trình "strongly typed", có nghĩa là các kiểu dữ liệu của biến được kiểm tra chặt chẽ trong quá trình biên dịch. Điều này giúp:
    - **Ngăn ngừa lỗi**: Các lỗi gán giá trị không đúng sẽ được phát hiện sớm trước khi chương trình chạy.
    - **Tăng cường tính rõ ràng**: Giúp lập trình viên dễ dàng hiểu và quản lý loại dữ liệu mà họ đang làm việc.

3. Kể cả việc giá trị ngoài khoảng cho phép cũng sẽ bị compiler kiểm soát

```cs
sbyte hello = 500;  // Sai vì khoảng của sbyte không chứa được
```

</v-clicks>

---

# Kết luận: Biến và Kiểu Dữ Liệu

<v-clicks>

1. Biến là một vùng nhớ được đặt tên, dùng để lưu trữ dữ liệu trong chương trình. Mỗi biến cần được khai báo với một kiểu dữ liệu cụ thể.
2. Kiểu dữ liệu xác định loại dữ liệu mà biến có thể chứa, bao gồm:
    - **Built-in Types**: Các kiểu dữ liệu có sẵn như `int`, `float`, `bool`, `char`, ....
    - **User-defined Types**: Các kiểu dữ liệu do lập trình viên tự định nghĩa như `class`, `struct` và `enum`.
3. Tầm quan trọng của việc chọn kiểu dữ liệu:
    - **Khoảng Giá trị**: Mỗi kiểu dữ liệu có một khoảng giá trị nhất định. Việc chọn kiểu dữ liệu phù hợp giúp đảm bảo rằng biến có thể chứa giá trị mong muốn mà không gây ra lỗi.
    - **Số Vùng Nhớ Chiếm Dụng**: Các kiểu dữ liệu khác nhau yêu cầu số lượng bộ nhớ khác nhau (ví dụ: `int` chiếm 4 byte, `long` chiếm 8 byte). Việc lựa chọn kiểu dữ liệu ảnh hưởng đến hiệu suất của chương trình, đặc biệt khi xử lý lượng lớn dữ liệu.
4. *Kết luận*: Việc chọn kiểu dữ liệu chính xác không chỉ giúp tránh lỗi trong chương trình mà còn tối ưu hóa hiệu suất và sử dụng tài nguyên bộ nhớ hiệu quả. Hãy luôn xem xét nhu cầu của ứng dụng khi quyết định kiểu dữ liệu cho các biến.

</v-clicks>

---

# Lưu ý khi đặt tên biến

<v-clicks>

- Đặt tên biến sao cho mô tả được mục đích sử dụng của biến. Đảm bảo độ chính xác và tiết kiệm vùng nhớ.
- Quy tắc đặt tên theo Camel Case:
    - Bắt đầu bằng chữ cái thường.
    - Mỗi từ bắt đầu bằng chữ cái hoa, các từ sau không có khoảng trắng.
    - Ví dụ: firstName, lastName, numberOfStudents, isValidEmail.

```csharp
string fullName = "Nguyen Van A";
byte age = 25;
char firstLetterOfName = 'N';

// In thông tin ra màn hình
Console.WriteLine($"Họ tên: {fullName}");
Console.WriteLine($"Tuổi: {age}");
Console.WriteLine($"Ký tự đầu tiên: {firstLetterOfName}");
```

</v-clicks>

---

# Thực Hành: Đặt Tên Biến và In Giá Trị

1. **Đặt Tên Biến Theo Quy Tắc Cammel Case**:
    - Tạo các biến sau để lưu trữ thông tin cá nhân của bạn:
        - Tên của bạn
        - Tuổi của bạn
        - Số điện thoại của bạn
        - Địa chỉ email của bạn
        - Số tiền trong ví của bạn
2. **In Giá Trị của Biến ra Màn Hình**:
    - Sử dụng phương thức `Console.WriteLine()` để in giá trị của từng biến.
3. **Thực Hành Thay Đổi Giá Trị của Các Biến**:
    - Quan sát sự thay đổi giá trị khi in ra màn hình.
    - Đặt breakpoint (`F9`) để dừng chương trình ở các điểm quan trọng và sử dụng `F10` để đi qua từng dòng và xem sự thay đổi giá trị của biến.
    - Thêm các biến vào cửa sổ Watch để theo dõi giá trị của chúng trong quá trình debug.

---

# Thuật ngữ "Bug"

<v-clicks>

- Xuất hiện vào đầu năm 1940 bởi **[Grace Hopper](https://en.wikipedia.org/wiki/Grace_Hopper)**, một nhà khoa học máy tính tiên phong.
- Bà phát hiện ra một con **bọ** đã chui vào và làm hỏng một bộ phận của máy tính thời đó.
- Kể từ đó, "bug" trở thành từ dùng để chỉ những **lỗi kỹ thuật** trong máy móc và phần mềm

> **Bug** hiện nay được sử dụng để mô tả các lỗi hoặc sự cố khiến chương trình **không hoạt động đúng như mong muốn**.

</v-clicks>

---

# Ý tưởng của Debugging

<v-clicks>

- **Debugging** là quá trình tìm và sửa lỗi trong chương trình, giúp đảm bảo rằng mọi thử hoạt động đúng.
- **Xem giá trị biến**: Kiểm tra giá trị của các biến khi chương trình đang chạy để chắc chắn rằng chúng có đúng kết quả.
- **Theo dõi luồng thực thi**: Xem từng bước chương trình chạy để hiểu rõ nó hoạt động thế nào và phát hiện lỗi.
- **Sửa lỗi**: Tìm và sửa lỗi logic hoặc cú pháp trong mã để chương trình hoạt động đúng.
- **Kiểm tra điều kiện**: Đảm bảo rằng các câu lệnh điều kiện trong chương trình cho kết quả như mong đợi.

</v-clicks>

---

# Debugging trong Visual Studio: Breakpoint

<v-clicks>

- **Breakpoint (F9)** là điểm dừng chương trình, giúp bạn tạm dừng thực thi để kiểm tra giá trị biến và luồng thực thi.
- **Khi chạy chế độ Debug (F5)**, chương trình sẽ dừng tại Breakpoint, cho phép bạn kiểm tra và tìm ra lỗi dễ dàng.
- Sau khi dừng tại Breakpoint, bạn có thể:
    - **Xem giá trị biến** tại thời điểm đó.
    - **Theo dõi luồng thực thi** bằng **Step Over (F10)** hoặc **Step Into (F11)**.

</v-clicks>

---

# Bật debug lên

<v-clicks>

```cs
Console.OutputEncoding = System.Text.Encoding.UTF8;

decimal wallet = 50.0m; // Số tiền ban đầu trong ví là 50.0
Console.WriteLine("Giá trị ban đầu của ví: " + wallet);

wallet = 100.0m;    // Số tiền thay đổi thành 100.0
Console.WriteLine("Giá trị mới của ví: " + wallet);

wallet = 150.0m;    // Số tiền thay đổi thành 150.0
Console.WriteLine("Giá trị sau khi thay đổi lần 2 của ví: " + wallet);

wallet = 200.0m;    // Số tiền thay đổi thành 200.0
Console.WriteLine("Giá trị sau khi thay đổi lần cuối của ví: " + wallet);
```

- **Đặt Breakpoint (F9)**: Chọn dòng mà bạn muốn chương trình dừng lại (ví dụ: 1, 5, 8, 11).
- **Bắt đầu Debug (F5)**: Chạy chương trình trong chế độ Debug. Chương trình sẽ dừng tại Breakpoint cho phép bạn xem giá trị của biến `wallet`.
- **Sử dụng Watch**: Mở tab Watch để theo dõi giá trị của biến `wallet` và bất kỳ biểu thức nào khác bạn muốn.
- **Sử dụng Step Over (F10)**: Chạy từng dòng code một mà không đi vào các hàm. Điều này giúp bạn theo dõi giá trị `wallet` một cách dễ dàng.

</v-clicks>