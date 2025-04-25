# Constants (Hằng số)

<v-clicks>

- **Hằng số** là giá trị không thay đổi trong suốt quá trình thực thi của chương trình (run-time).

```cs
const int MONTHS = 12;
const int DAYS = 31;
const int DAYS_OF_YEAR = 365;
```

1. **Thay đổi giá trị của hằng số thì sao?**

```cs
const int MONTHS = 12;
MONTHS = 13;    // dòng này sẽ báo lỗi vì hằng số khong thể thay đổi giá trị
```

- Nếu bạn cố gắng thay đổi giá trị của một hằng số sau khi đã khai báo, chương trình sẽ báo lỗi.

2. Ví dụ về Constants

```cs
const int MAX_CONNECTIONS = 100;    // Số kết nối tối đa
const double GRAVITY = 9.8; // Gia tốc trọng trường
const string API_KEY = "your_api_key_here"; // khóa API
const string DEFAULT_USERNAME = "guest";    // Tên người dùng mặc định
const bool IS_DEBUGGING_ENABLED = true; // Chế độ gỡ lỗi có bật không
const decimal TAX_RATE = 0.08m; // Tỷ lệ thuế
```

</v-clicks>

---

# Type Conversion (Chuyển đổi kiểu)

<v-clicks>

- **Chuyển đổi kiểu** (Type Conversion) là quá trình chuyển đổi giữa các kiểu dữ liệu khác nhau trong lập trình, cho phép sử dụng giá trị của một kiểu dữ liệu trong một kiểu dữ liệu khác.
- Việc chuyển đổi kiểu thường cần thiết khi bạn làm việc với các kiểu dữ liệu khác nhau và muốn đảm bảo rằng các phép toán, so sánh hoặc truyền tham số giữa các kiểu này hoạt động chính xác.
- Chuyển đổi kiểu có thể được chia thành hai loại chính:

1. **Implicit Conversions** (Chuyển đổi ngầm định): Tự động diễn ra khi chuyển từ kiểu dữ liệu nhỏ hơn sang kiểu dữ liệu lớn hơn mà không mất mát dữ liệu.
2. **Explicit Conversions** (Chuyển đổi tường minh): Cần phải chỉ định rõ ràng vì có nguy cơ mất dữ liệu hoặc độ chính xác.

</v-clicks>

---

# Implicit Conversions (Chuyển đổi ngầm định)

<v-clicks>

- Là quá trình tự động chuyển giá trị từ kiểu dữ liệu nhỏ hơn sang kiểu dữ liệu lớn hơn mà không cần sự can thiệp của người lập trình. Điều này giúp bạn dễ dàng làm việc với nhiều kiểu dữ liệu mà không phải lo lắng về việc mất mát dữ liệu.

```cs
sbyte a = 100;  // Kiểu sbyte: có giá trị từ -128 đến 127
Console.WriteLine(a);

short b = a;    // Chuyển đổi từ sbyte sang short: có giá trị từ -32,768 đến 32,767
Console.WriteLine(b);

int c = b;  // Chuyển đổi từ short sang int: có giá trị từ -2,147,483,648 đến 2,147,483,647
Console.WriteLine(c);
```

- Khi bạn chuyển từ kiểu dữ liệu nhỏ sang lớn, bạn không cần lo lắng về việc mất mát dữ liệu, vì kiểu dữ liệu lớn hơn luôn có khả năng chứa tất cả các giá trị của kiểu trước đó.

</v-clicks>

---

# Explicit Conversions (Chuyển đổi tường minh)

<v-clicks>

- Là quá trình chuyển đổi giá trị từ kiểu dữ liệu lớn hơn sang kiểu dữ liệu nhỏ hơn, trong đó có thể xảy ra nguy cơ mất mát dữ liệu. Do đó, người lập trình cần thực hiện các thao tác chuyển đổi một cách rõ ràng.

```cs
double x = 1234.7;
Console.WriteLine(x);

int y = (int)x; // Chuyển đổi từ double sang int: cần chỉ định rõ ràng
Console.WriteLine(y);
```

- Trong ví dụ trên, khi bạn chuyển đổi từ kiểu **double** sang **int**, phần thập phân sẽ bị loại bỏ. Điều này có thể dẫn đến mất mát dữ liệu, vì vậy bạn cần phải chú ý khi thực hiện chuyển đổi.
- Để thực hiện chuyển đổi tường minh, bạn cần sử dụng toán tử cast (ví dụ: `(int)`) để chỉ định rõ ràng kiểu dữ liệu mà bạn muốn chuyển đổi tới.

```cs
double x = 1234.7;
Console.WriteLine(x);

byte y = (byte)x; // Chuyển đổi từ double sang byte: cần chỉ định rõ ràng
Console.WriteLine(y);   // Đáp án sẽ khến bạn ngạc nhiên đấy
```

</v-clicks>

---

# Thử nghiệm Chuyển đổi Kiểu

<v-clicks>

1. **Thử nghiệm**

```cs
double x = 3_000_000_000;   // Khai báo biến kiểu double với giá trị lớn
int y = (int)x; // Chuyển đổi tường minh (Explicit conversions)
Console.WriteLine(y);   // Giá trị của y là ?
Console.WriteLine(int.MaxValue);    // In ra giá trị lớn nhất của kiểu int
Console.WriteLine(int.MinValue);    // In ra giá trị nhỏ nhất của kiểu int
```

2. **Giải thích**

- **Giới hạn của Kiểu `int`**: Kiểu `int` có phạm vi giá trị từ `-2,147,483,648` đến `2,147,483,647`. Điều này có nghĩa là nó chỉ có thể lưu trữ các số trong khoảng này.
- **Giá trị `x`**: Giá trị của `x` là `3,000,000,000`, vượt quá giới hạn trên của kiểu `int`.
- **Tràn số (Overflow)**: Khi bạn ép kiểu `x` thành `int`, nó dẫn đến hiện tượng tràn số và giá trị kết quả của `y` sẽ trở thành một số âm do giới hạn của kiểu `int`.

</v-clicks>

---

# Hàm `.Parse()`

<v-clicks>

- Được sử dụng để chuyển đổi chuỗi (string) thành các kiểu dữ liệu khác, như số nguyên (int), số thực (double) và ngày tháng (DateTime).

1. Ví dụ chuyển đổi chuỗi thành số nguyên

```cs
string numberString = "12345";
int number = int.Parse(numberString);
Console.WriteLine(number);  //12345
```

2. Ví dụ chuyển đổi chuỗi thành double

```cs
string doubleString = "123.45";
double number = double.Parse(doubleString);
Console.WriteLine(number);  //123.45
```

3. Ví dụ chuyển đổi chuỗi thành DateTime

```cs
string dateString = "2024-10-16";
DateTime dateValue = DateTime.Parse(dateString);
Console.WriteLine(dateValue);   // 10/16/2024 12:00:00 AM
```

> Hàm Parse rất tiện lợi để chuyển đổi chuỗi thành các kiểu dữ liệu mong muốn.

</v-clicks>

---

# Chuỗi không hợp lệ với Hàm Parse

<v-clicks>

1. Sử dụng `int.Parse()` với chuỗi không hợp lệ

```cs
string a = "abc";
int b = int.Parse(a);   // Gây ra FormatException
Console.WriteLine(b);
```

- Trong đoạn mã này, chúng ta cố gắng chuyển đổi chuỗi `"abc"` thành số nguyên. Tuy nhiên, điều này sẽ gây ra một lỗi gọi là `FormatException` và chương trình sẽ không thể tiếp tục thực thi.

2. Giải thích lỗi
    - Khi chúng ta cố gắng chuyển đổi chuỗi `"abc"` thành kiểu `int`, một lỗi `FormatException` sẽ xảy ra.
    - Nguyên nhân chính là vì chuỗi `"abc"` không có định dạng số nguyên hợp lệ, nên không thể thực hiện việc chuyển đổi.

</v-clicks>

---

# Sử dụng `.TryParse()` để xử lý ngoại lệ

<v-clicks>

```cs
string b = "100b";
int num;
bool isSuccess = int.TryParse(b, out num);
Console.WriteLine(isSuccess);   // Kết quả: False
Console.WriteLine(num); // Kết quả: 0
```

- Phương thức `int.TryParse()` giúp chúng ta chuyển đổi một chuỗi thành số nguyên mà không gây ra lỗi.
- Nếu việc chuyển đổi thành công, biến `isSuccess` sẽ nhận giá trị `true` và giá trị số nguyên sẽ được lưu trong biến `num`.
- Nếu không thành công, `isSuccess` sẽ là `false` và `num` sẽ có giá trị mặc định là `0`.

> Sử dụng `TryParse()` giúp chương trình của bạn an toàn hơn, tránh việc dừng lại đột ngột khi gặp lỗi chuyển đổi.

</v-clicks>

---

# Giới thiệu về `Conert.To`

<v-clicks>

- Sử dụng để chuyển đổi các kiểu dữ liệu khác nhau một cách linh hoạt và an toàn. Nó có thể chuyển đổi giữa các kiểu dữ liệu như chuỗi (string), số nguyên (int), số thực (double) và nhiều kiểu khác.

1. **Chuyển đổi chuỗi thành số nguyên**:

```cs
string numberString = "12345";
int number = Convert.ToInt32(numberString);
Console.WriteLine("Giá trị số nguyên: " + number);  // Kết quả: 12345
```

2. **Chuyển đổi chuỗi thành số thực**:

```cs
string numberString = "123.45";
double number = Convert.ToDouble(numberString);
Console.WriteLine("Giá trị số thực: " + number);  // Kết quả: 123.45
```

3. **Chuyển đổi chuỗi thành DateTime**:

```cs
string dateString = "2024-10-16";
DateTime dateValue = Convert.ToDateTime(dateString);
Console.WriteLine("Giá trị ngày tháng: " + dateValue.ToString("dd/MM/yyyy"));  // Kết quả: ?
```

</v-clicks>

---

# Chuỗi không hợp lệ với hàm `Convert.To`

<v-clicks>

- Khi bạn cố gắng chuyển đổi chuỗi không hợp lệ sang kiểu dữ liệu khác bằng `Parse` hoặc `Convert.To`, điều này có thể dẫn đến lỗi.

```cs
string invalidString = "abc";
int number = Convert.ToInt32(invalidString);    // Gây ra FormatException
```

- Tương tự như `Parse`, việc chuyển đổi chuỗi không hợp lệ bằng `Convert.ToInt32` cũng sẽ gây ra `FormatException`.
- Điều này xảy ra khi chuỗi không thể được chuyển đổi thành kiểu dữ liệu mong muốn.

</v-clicks>

---

# Đọc Giá Trị Từ Bàn Phím

<v-clicks>

```cs
Console.OutputEncoding = System.Text.Encoding.UTF8; // Thiết lập để hỗ trợ tiếng Việt

Console.Write("Tên của bạn là gì: ");   // Yêu cầu người dùng nhập tên
string name = Console.ReadLine();   // Đọc tên từ bàn phím

Console.Write("Hê lô: " + name);    // Hiển thị lời chào cùng với tên
```

- Dòng `string name = Console.ReadLine();` sẽ chờ người dùng nhập dữ liệu từ bàn phím. Khi người dùng nhấn phím Enter, chuỗi nhập vào sẽ được lưu vào biến `name`.

</v-clicks>

---

# Tổng Kết: Biến và Kiểu Dữ Liệu

<v-clicks>

- **Biến**: Là **tên** đại diện cho vùng nhớ để lưu trữ dữ liệu. Biến giúp chương trình dễ dàng thao tác với dữ liệu.
    - Mỗi biến phải được **khai báo** với một **tên** và **kiểu dữ liệu** cụ thể.
- **Kiểu dữ liệu**: Xác định loại giá trị mà biến có thể lưu trữ và các phép toán có thể thực hiện trên biến.
    - **Kiểu dữ liệu cơ bản**: `int`, `float`, `char`, `bool`, `string`.
    - **Kiểu dữ liệu phức tạp**: `array`, `class`, `enum`, `struct`.
- **Lưu ý**:
    - Chọn kiểu dữ liệu phfu hợp để tối ưu bộ nhớ và hiệu năng.
    - Hiểu rõ sự khác biệt giữa các kiểu dữ liệu để tránh lỗi khi xử lý dữ liệu.

</v-clicks>