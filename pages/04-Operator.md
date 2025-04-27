# Operator

<v-clicks>

- Toán tử là các **ký tự đặc biệt** giúp bạn thực hiện các phép tính hoặc so sánh giữa các giá trị.
- Chúng giúp bạn làm những việc như: **cộng**, **trừ**, **so sánh** hoặc **gán giá trị** cho biến.

</v-clicks>

---

# Arithmetic Operators (Toán Tử Số Học)

<v-clicks>

- Là các **toán tử** giúp bạn thực hiện các phép tính số học cơ bản như: **cộng**, **trừ**, **nhân**, **chia** và **chia lấy phần dư** trong lập trình.

```csharp
using System;

int a = 10;
int b = 5;

// Thực hiện các phép toán số học
int tong = a + b;        // Toán tử cộng
int hieu = a - b;        // Toán tử trừ
int tich = a * b;        // Toán tử nhân
int thuong = a / b;      // Toán tử chia nguyên
int du = a % b;          // Toán tử chia lấy dư

// In kết quả
Console.WriteLine("\nKết quả các phép toán:");
Console.WriteLine($"{a} + {b} = {tong}");
Console.WriteLine($"{a} - {b} = {hieu}");
Console.WriteLine($"{a} * {b} = {tich}");
Console.WriteLine($"{a} / {b} = {thuong} (chia nguyên)");
Console.WriteLine($"{a} % {b} = {du} (phần dư)");
```

</v-clicks>

---

# Thực Hành: Tính chu vi Hình Chữ Nhật

- Viết chương trình cho phép người dùng nhập chiều dài và chiều rộng của hình chữ nhật (dưới dạng số thập phân). Sau đó, chương trình sẽ tính toán và hiển thị chu vi của hình chữ nhật.

1. **Nhập dữ liệu từ người dùng**:
   - Yêu cầu người dùng nhập chiều dài và chiều rộng của hình chữ nhật.
2. **Công thức tính chu vi**: `Chu Vi = 2 * (Chiều Dài + Chiều Rộng)`.
3. Sau khi tính toán, in ra chu vi của hình chữ nhật theo đúng định dạng.

- Ví dụ:

```md
Nhập chiều dài của hình chữ nhật: 5.5
Nhập chiều rộng của hình chữ nhật: 3.25

Chu vi của hình chữ nhật là: 17.5
```

---

# Code Tham Khảo

```cs
using System;

Console.Write("Nhập chiều dài của hình chữ nhật: ");
double chieuDai = double.Parse(Console.ReadLine());

Console.Write("Nhập chiều rộng của hình chữ nhật: ");
double chieuRong = double.Parse(Console.ReadLine());

// Tính chu vi hình chữ nhập
double chuVi = 2 * (chieuDai + chieuRong);

Console.WriteLine($"\nChu vi của hình chữ nhật là: {chuVi}");
```

---

# Increment Operator (Toán Tử Tăng)

<v-clicks>

- **Toán tử tăng** (`++`) được sử dụng để **tăng giá trị của biến** lên 1 đơn vị.

1. Sử dụng toán tử `++` sau biến:

```cs
int a = 5;
int b = a++;    // Sử dụng toán tử sau biến

Console.WriteLine($"a = {a}");
Console.WriteLine($"b = {b}");
```

- Giá trị hiện tại của `a` (5) được gán cho `b`, sau đó `a` mới được tăng lên 6.

2. Sử dụng toán tử `++` trước biến:

```cs
int a = 5;
int b = ++a;    // Sử dụng toán tử trước biến

Console.WriteLine($"a = {a}");
Console.WriteLine($"b = {b}");
```

- `a` được tăng lên 6 trước, sau đó giá trị mới của `a` mới được gán cho `b`.

</v-clicks>

---

# Decrement Operator (Toán Tử Giảm)

<v-clicks>

- **Toán tử tăng** (`--`) được sử dụng để **giảm giá trị của biến** đi 1 đơn vị.

1. Sử dụng toán tử `--` sau biến:

```cs
int a = 5;
int b = a--;    // Sử dụng toán tử sau biến

Console.WriteLine($"a = {a}");
Console.WriteLine($"b = {b}");
```

- Giá trị hiện tại của `a` (5) được gán cho `b`, sau đó `a` mới được giảm xuống 4.

2. Sử dụng toán tử `--` trước biến:

```cs
int a = 5;
int b = --a;    // Sử dụng toán tử trước biến

Console.WriteLine($"a = {a}");
Console.WriteLine($"b = {b}");
```

- `a` được giảm xuống 4 trước, sau đó giá trị mới của `a` mới được gán cho `b`.

</v-clicks>

---
zoom: 0.6
---

# Compare Operator (Toán tử So Sánh)

<v-click>

- **Toán tử so sánh** đucợ sử dụng để so sánh hai giá trị và trả về kết quả là `true` hoặc `false`.

</v-click>

<v-clicks>

1. **Bằng** (==): Kiểm tra xem hai giá trị có bằng nhau không.

   - Ví dụ: `5 == 5` 👉 **Kết quả**: `true`.
   - Ví dụ: `4 == 5` 👉 **Kết quả**: `false`.

2. **Khác (!=)**: Kiểm tra xem hai giá trị có khác nhau không.
   - Ví dụ: `5 != 4` 👉 **Kết quả**: `true`.
   - Ví dụ: `5 != 5` 👉 **Kết quả**: `false`.

3. **Lớn hơn (>)**: Kiểm tra xem giá trị bên trái có lớn hơn giá trị bên phải không.
    - Ví dụ: `7 > 5` 👉 **Kết quả**: `true`.
    - Ví dụ: `3 > 4` 👉 **Kết quả**: `false`.

4. **Nhỏ hơn (<)**: Kiểm tra xem giá trị bên trái có nhỏ hơn giá trị bên phải không.
    - Ví dụ: `3 < 5` 👉 **Kết quả**: `true`.
    - Ví dụ: `6 < 2` 👉 **Kết quả**: `false`.

5. **Lớn hơn hoặc bằng (>=)**: Kiểm tra xem giá trị bên trái có lớn hơn hoặc bằng giá trị bên phải không.
    - Ví dụ: `5 >= 5` 👉 **Kết quả**: `true`.
    - Ví dụ: `4 >= 5` 👉 **Kết quả**: `false`.

6. **Nhỏ hơn hoặc bằng (<=)**: Kiểm tra xem giá trị bên trái có nhỏ hơn hoặc bằng giá trị bên phải không.
    - Ví dụ: `3 <= 5` 👉 **Kết quả**: `true`.
    - Ví dụ: `5 <= 4` 👉 **Kết quả**: `false`.

</v-clicks>

---

# Toán tử Bằng (==)

<v-clicks>

- **Toán tử Bằng (`==`)** được sử dụng để kiểm tra xem hai giá trị có bằng nhau hay không. Kết quả trả về là `true` nếu chúng bằng nhau và `false` nếu không.

1. Kiểm tra số nguyên:

```cs
int a = 5;
int b = 5;
Console.WriteLine(a == 5);  // Kết quả: true
```

2. Kiểm tra só nguyên không bằng nhau:

```cs
int a = 4;
int b = 5;
Console.WriteLine(a == 5);  // Kết quả: false
```

3. Kiểm tra chuỗi bằng nhau:

```cs
string a = "Hello";
string b = "Hello";

Console.WriteLine(a == b);  // Kết quả: true
```

</v-clicks>

---

# Toán tử Khác (!=)

<v-clicks>

- **Toán tử khác (`!=`)** được sử dụng để kiểm tra xem hai giá trị có khác nhau hay không. Kết quả trả về là `true` nếu chúng khác nhau và `false` nếu không.

1. Kiểm tra số nguyên:

```cs
int a = 5;
int b = 4;
Console.WriteLine(a != 5);  // Kết quả: true
```

2. Kiểm tra só nguyên không bằng nhau:

```cs
int a = 5;
int b = 5;
Console.WriteLine(a != 5);  // Kết quả: false
```

3. Kiểm tra chuỗi bằng nhau:

```cs
string a = "Hello";
string b = "World";

Console.WriteLine(a != b);  // Kết quả: true
```

</v-clicks>