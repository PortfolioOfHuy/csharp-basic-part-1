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

---

# Toán tử Lớn hơn (>)

<v-click>

- **Toán tử Lớn hơn `(>)`** được sử dụng để kiểm tra xem giá trị bên trái có lớn hơn giá trị bên phải hay không. Kết quả trả về là `true` nếu điều kiện đúng, và `false` nếu không.

</v-click>

<v-clicks>

1. Kiểm tra số nguyên:

```cs
int a = 5;
int b = 4;
Console.WriteLine(a > b);   // Kết quả: true
```

2. Kiểm tra số nguyên không lớn hơn:

```cs
int a = 3;
int b = 4;
Console.WriteLine(a > b);   // Kết quả: false
```

3. Kiểm tra số thập phân:

```cs
int a = 5.5;
int b = 5.0;
Console.WriteLine(a > b);   // Kết quả: true
```

</v-clicks>

---

# Toán tử Nhỏ hơn (<)

<v-click>

- **Toán tử Nhỏ hơn `(<)`** được sử dụng để kiểm tra xem giá trị bên trái có nhỏ hơn giá trị bên phải hay không. Kết quả trả về là `true` nếu điều kiện đúng, và `false` nếu không.

</v-click>

<v-clicks>

1. Kiểm tra số nguyên:

```cs
int a = 3;
int b = 4;
Console.WriteLine(a < b);   // Kết quả: true
```

2. Kiểm tra số nguyên không nhỏ hơn:

```cs
int a = 5;
int b = 4;
Console.WriteLine(a < b);   // Kết quả: false
```

3. Kiểm tra số thập phân:

```cs
int a = 2.5;
int b = 3.0;
Console.WriteLine(a < b);   // Kết quả: true
```

</v-clicks>

---

# Toán tử Lớn hơn hoặc bằng (>=)

<v-click>

- **Toán tử Lớn hơn hoặc bằng `(>=)`** được sử dụng để kiểm tra xem giá trị bên trái có lớn hơn hoặc bằng giá trị bên phải hay không. Kết quả trả về là `true` nếu điều kiện đúng, và `false` nếu không.

</v-click>

<v-clicks>

1. Kiểm tra số nguyên:

```cs
int a = 5;
int b = 5;
Console.WriteLine(a >= b);   // Kết quả: true
```

2. Kiểm tra số nguyên lớn hơn:

```cs
int a = 6;
int b = 4;
Console.WriteLine(a >= b);   // Kết quả: true
```

3. Kiểm tra số nguyên nhỏ hơn:

```cs
int a = 4;
int b = 5;
Console.WriteLine(a >= b);   // Kết quả: false
```

</v-clicks>

---

# Toán tử nhỏ hơn hoặc bằng (<=)

<v-click>

- **Toán tử nhỏ hơn hoặc bằng `(<=)`** được sử dụng để kiểm tra xem giá trị bên trái có nhỏ hơn hoặc bằng giá trị bên phải hay không. Kết quả trả về là `true` nếu điều kiện đúng, và `false` nếu không.

</v-click>

<v-clicks>

1. Kiểm tra số nguyên:

```cs
int a = 5;
int b = 5;
Console.WriteLine(a <= b);   // Kết quả: true
```

2. Kiểm tra số nguyên nhỏ hơn:

```cs
int a = 4;
int b = 5;
Console.WriteLine(a <= b);   // Kết quả: true
```

3. Kiểm tra số nguyên không nhỏ hơn:

```cs
int a = 6;
int b = 5;
Console.WriteLine(a <= b);   // Kết quả: false
```

</v-clicks>

---

# Thực Hành: Toán Tử So Sánh

1. cho a = 7 và b = 3. a > b => đáp án là?
2. cho a = 10 và b = 15. a <= b => đáp án là?
3. cho a = 7 và b = 3. a == b => đáp án là?
4. cho a = 7 và b = 3. a != b => đáp án là?
5. cho a = 7 và b = 3. a >= b => đáp án là?

> Bạn hãy kiểm tra và xác định đáp án cho mỗi câu hỏi dựa trên các phép so sánh đã cho.

---

# Expressions (biểu thức)

<v-click>

- Expression là một đoạn mã trong lập trình mà khi được thực hiện sẽ trả về một giá trị.

</v-click>

<v-clicks>

1. Ví dụ cụ thể:

```cs
int a = 7;
int b = 3;
bool c = a > b;     // Expression so sánh và trả về true
Console.WriteLine(c);
```

2. Expression với String Interpolation

```cs
int x = 5;
int y = 3;
Console.WriteLine($"Tổng của x và y là: {x + y}");      // Kết quả: ?
```

3. Kiểm tra số chẵn:

```cs
int x = 10;
bool isEven = (x % 2 == 0);     // Kiểm tra xem x có phải là số chẵn không
Console.WriteLine($"X có phải là số chẵn không? {isEven}");     // Kết quả: true
```

</v-clicks>

---

# Toán tử Logic (Logical Operators)

<v-clicks>

- **Toán tử logic** được sử dụng để kết hợp các biểu thức boolean và trả về kết quả là `true` hoặc `false`.
- **AND (&&):** Trả `true` nếu cả hai biểu thức đều là `true`.
    - Ví dụ: `true && false` -> Kết quả: **false**
- **OR (||):** Trả về `true` nếu ít nhất một trong hai biểu thức là `true`.
    - Ví dụ: `true || false` -> Kết quả: **true**
- **NOT (!):** Đảo ngược giá trị boolean của biểu thức. Nếu biểu thức là `true`, nó sẽ trả về `false` và ngược lại.
    - Ví dụ: `!true` -> Kết quả: **false**

</v-clicks>

---

# Toán tử AND (&&)

<v-click>

- **Toán tử AND (&&)** được sử dụng để kết hợp hai biểu thức boolean. Kết quả của toán tử này sẽ là `true` chỉ khi cả hai biểu thức đều là `true`. Nếu một trong hai biểu thức là `false`, kết quả là `false`.

</v-click>

<v-clicks>

1. Ví dụ minh họa:

```cs
Console.WriteLine($"true && true: {true && true}");     // Output: True
Console.WriteLine($"true && false: {true && false}");     // Output: False
Console.WriteLine($"false && true: {false && true}");     // Output: False
Console.WriteLine($"false && false: {false && false}");     // Output: False
```

2. Kết hợp nhiều expression
```cs
int a = 5;
int b = 10;

bool result = (a < b) && (b > 0);   // Tìm xem cả hai điều kiện đều đúng hay không

Console.WriteLine($"a = {a}, b = {b}");
Console.WriteLine($"a < b && b > 0: {result}");     // Output: ?
```

</v-clicks>

---

# Toán tử OR (||)

<v-click>

- **Toán tử OR (||)** được sử dụng để kết hợp hai biểu thức boolean. Kết quả của toán tử này sẽ là `true`, nếu ít nhất một trong hai biểu thức là `true`. Nếu cả hai biểu thức là `false`, kết quả là `false`.

</v-click>

<v-clicks>

1. Ví dụ minh họa:

```cs
Console.WriteLine($"true || true: {true || true}");     // Output: True
Console.WriteLine($"true || false: {true || false}");     // Output: True
Console.WriteLine($"false || true: {false || true}");     // Output: True
Console.WriteLine($"false || false: {false || false}");     // Output: False
```

2. Kết hợp nhiều expression
```cs
bool isSunny = true;
bool haveCharcoal = false;

bool canHaveBBQ = isSunny || haveCharcoal;

Console.WriteLine($"Can Have BBQ: {canHaveBBQ}");     // Output: ?
```

</v-clicks>

---

# Toán tử NOT (!)

<v-click>

- **Toán tử NOT (!)** là một toán tử đơn được sử dụng để đảo ngược giá trị boolean của một biểu thức. Nếu biểu thức là `true`, toán tử NOT sẽ trả về `false`, và ngược lại.

</v-click>

<v-clicks>

1. Kết quả của các phép toán NOT:

```cs
Console.WriteLine($"!true: {!true}");     // Output: false
Console.WriteLine($"!false: {!false}");     // Output: true
Console.WriteLine($"!!false: {!!false}");     // Output: false
Console.WriteLine($"!!!false: {!!!false}");     // Output: true
```

2. Ví dụ sử dụng trong code:
```cs
bool isRaining = true;

bool canGoOutside = !isRaining;

Console.WriteLine($"Is Raining: {isRaining}");     // Output: ?
Console.WriteLine($"Can Go Outside: {canGoOutside}");     // Output: ?
```

</v-clicks>

---

# Assignment Operators (Toán Tử Gán)

<v-clicks>

- **Toán tử gán (`=`)** được sử dụng để gán giá trị cho một biến. Ngoài toán tử gán cơ bản, còn có các toán tử gán kết hợp, giúp thực hiện phép tính và gán kết quả vào biến một cách ngắn gọn.
- **Toán tử gán cơ bản (`=`):** Gán giá trị cho biến.
    - Ví dụ: `a = 10` -> Gán giá trị 10 cho biến `a`.
- **Cộng và gán (`+=`):** Cộng giá trị vào biến và gán kết quả.
    - Ví dụ: `a += 5` tương đương với `a = a + 5`.
- **Trừ và gán (`-=`):** Trừ giá trị và gán kết quả.
    - Ví dụ: `a -= 5` tương đương với `a = a - 5`.
- **Nhân và gán (`*=`):** Nhân giá trị và gán kết quả.
    - Ví dụ: `a *= 5` tương đương với `a = a * 5`.
- **Chia và gán (`/=`):** Chia giá trị và gán kết quả.
    - Ví dụ: `a /= 5` tương đương với `a = a / 5`.

</v-clicks>

---

# Ví Dụ Assignment Operators

```cs
int a = 10;            // Toán tử gán cơ bản
Console.WriteLine("Giá trị ban đầu của a: " + a);

a += 5;                // a = a + 5
Console.WriteLine("Sau a += 5, a = " + a);

a -= 3;                // a = a - 3
Console.WriteLine("Sau a -= 3, a = " + a);

a *= 2;                // a = a * 2
Console.WriteLine("Sau a *= 2, a = " + a);

a /= 4;                // a = a / 4
Console.WriteLine("Sau a /= 4, a = " + a);
```

---

# null

<v-clicks>

- **null** là một giá trị đặc biệt trong lập trình, dùng để biểu thị rằng "không có giá trị" hoặc "không có dữ liệu".
- Khi một biến được gán là `null`, điều đó có nghãi là biến đó KHÔNG CHỨA GIÁ TRỊ.

1. Ví dụ với kiểu chuỗi (string):

```cs
string name = null;     // Biến name hiện không có giá trị
```

- Ở đây, name không chứa giá trị nào, vì nó được gán là `null`.

</v-clicks>

<v-clicks>

2. **Tại sao cần dùng `null`:**
    - Khi chưa có thông tin để lưu vào biến.
    - Để chỉ ra rằng một giá trị không tồn tại hoặc chưa được khởi tạo.
    - Giúp kiểm tra xem một biến có được gán giá trị chưa.

3. **Lưu ý quan trọng:**
- Các kiểu dữ liệu cơ bản như `int`, `char`, `double`, ... không thể chứa giá trị `null` trực tiếp.

```cs
int age = null;     // Báo lỗi vì kiểu int không cho phép null
byte a = null;      // Báo lỗi vì kiểu byte không cho phép null
```

</v-clicks>

---

# Kiểm tra giá trị `null`

<v-clicks>

1. Kiểm tra giá trị `null` bằng toán tử so sánh (==)

```cs
string name = null;

Console.WriteLine($"name == null: {name == null}")
```

- Ở đây, `name` không có giá trị, nên biểu thức `name == null` sẽ trả về **true**.

2. Lưu ý: chuỗi có giá trị "null" là khác với `null`:

```cs
string name = "null";

Console.WriteLine($"name == null: {name == null}")
```

- Dù chứa chữ "null", nhưng đây vẫn là một chuỗi, không phải giá trị `null`.

3. Kiểm tra không phải `null` bằng toán tử (!=):

```cs
string name = null;

Console.WriteLine($"name != null: {name != null}")
```

- Nếu giá trị của `name` là `null`, biểu thức `name != null` sẽ trả về **false**.

</v-clicks>

---

# Kiểm tra giá trị `null` với toán tử `is`

<v-clicks>

1. **Sử dụng toán tử `is` để kiển tra `null`:**

```cs
string name = null;

Console.WriteLine($"name is null: {name is null}")
```

- Ở đây, toán tử `is` được sử dụng để kiểm tra xem `name` có phải là `null` không. Kết quả trả về **true** nếu `name` là `null`.

2. **Ví dụ khác với giá trị không phải `null`:**

```cs
string name = "Hello";

Console.WriteLine($"name is null: {name is null}")
```

- Trong trường hợp này, `name` chứa chuỗi `Hello`, nên biểu thức `name is null` sẽ trả về **false**.

3. **`is not` là phủ định của `is`:**

```cs
string name = null;

Console.WriteLine($"name is not null: {name is not null}")
```

- Nếu giá trị của `b` là `null`, biểu thức `b is not null` sẽ trả về **false**.

</v-clicks>

---

# nullable

<v-clicks>

- Nullable cho phép các kiểu dữ liệu như `int`, `char`, `double`,... có thể chứa giá trị `null`. Điều này rất hữu ích khi bạn cần biểu thị rằng một biến có thể không có giá trị.

1. Khai báo kiểu dữ liệu nullable
    - Sử dụng dấu hỏi (`?`) sau kiểu dữ liệu để khai báo biến nullable.

```cs
int? a = null;
Console.WriteLine($"a is null {a is null}");

char? b = null;
Console.WriteLine($"b is null {b is null}");

double? c = null;
Console.WriteLine($"c is null {c is null}");
```

2. Kiểm tra xem biến có giá trị hay không
    - Sử dụng thuộc tính `HasValue` để kiểm tra xem biến nullable có chứa giá trị hay không.

```cs
int? x = null;
Console.WriteLine($"x.HasValue: {x.HasValue}");
```

- Nếu `x` có giá trị, `x.HasValue` sẽ trả về **true**; nếu không, né sẽ trả về **false**.

</v-clicks>

---

# Toán tử Null-Coalescing (`??`)

<v-clicks>

- **Null-Coalescing (`??`)** cho phép cung cấp một giá trị mặc định nếu biến nullable có giá trị là `null`.

1. Ví dụ

```cs
int? age = null;
int displayedAge = age ?? 18;

Console.WriteLine($"Tuổi hiển thị: {displayedAge}");
```

- Ở đây, nếu `age` là `null`, giá trị 18 sẽ được sử dụng làm giá trị mặc định.

2. Ví dụ với chuỗi:

```cs
string name = "Huy Lê";
string displayedName = name ?? "Người dùng chưa đăng nhập";

Console.WriteLine(displayedName);
```

- Trong trường hợp này, vì `name` không phải là `null`, nên kết quả hiển thị sẽ là giá trị của biến `name`.

</v-clicks>

---

# Giả thuật (Algorithms)

<v-clicks>

- **Giải thuật** là tập hợp các hướng dẫn cụ thể giúp bạn giải quyết một vấn đề nào đó.
- Bạn có thể tưởng tượng nó như một "công thức" để tìm ra lời giải cho một bài toán.
- **Ví dụ: Bài toán luộc trứng lòng đào**
1. Chuẩn bị 3 quả trứng cần luộc.
2. Đổ nước lạnh vào nồi sao cho nước ngập trứng.
3. Bật bếp và đun sôi nước.
4. Khi nước sôi, giảm lửa xuống mức trung bình.
5. Nấu trứng trong khoảng 6 phút.
6. Sau khi nấu xong, lấy trứng ra khỏi nồi.
7. Đặt trứng vào nước lạnh để làm nguội nhanh và ngừng quá trình nấu chín.
> Các bước trên được gọi là **Mã giả (Pseudo code)**.

</v-clicks>

---

# Mã giả (Pseudo code)

<v-clicks>

- Mã giả là cách để mô tả thuật toán bằng ngôn ngữ dễ hiểu và không bị ràng buộc bởi cú phấp của một ngôn ngữ lập trình cụ thể.
- Điều này giúp bạn dễ dàng diễn đạt ý tưởng và logic của thuật toán mà không cần lo lắng về cách việt code chính xác.
- **Quy tắc cơ bản của mã giả:**
1. **Ngắn gọn và dễ hiểu:** Trình bày một cách đơn giản và rõ ràng.
2. **Chú thích:** Đặt lời giả thích để người đọc dễ hiểu.
3. **Bước đi rõ ràng:** Chia nhỏ các bước theo thứ tự logic.
4. **Tập trung vào ý tưởng:** Không cần quan tâm đến cú pháp lập trình.

</v-clicks>

---

# Ví dụ

```sql
BEGIN
    DECLARE a = 5
    DECLARE b = 3
    DECLARE sum

    sum = a + b

    PRINT "Tổng là: " + sum
END

```

---

# Các bước giải quyết một bài toán

1. **Hiểu rõ bài toán:** Đọc kỹ yêu cầu và xác định thông tin cần thiết như đầu vào và đầu ra.
2. **Thiết kế thuật toán:** Chọn phương pháp giải quyết vấn đề và phân tích các bước thực hiện.
3. **Triển khai code:** Viết code dựa trên thiết kế thuật toán đã có.
4. **Kiểm tra và sửa lỗi:** Kiểm tra mã để đảm bảo hoạt động đúng, sửa lỗi nếu có và cải thiện khi cần thiết.

---

# Math class

<v-click>

- **Math class** cung cấp nhiều phương thức giúp thực hiện các phép tính số học từ cơ bản đến nâng cao.

</v-click>

<v-clicks>

1. `Math.PI`: Hằng số Pi (π), giá trị xấp xỉ 3.14 được sử dụng trong các tính toán liên quan đến hình tròn.
2. `Math.Abs()`: Phương thức này trả về giá trị tuyệt đối của một số. Ví dụ, nếu bạn nhập -5, kết quả sẽ là 5.
3. `Math.Floor()`: Làm tròn xuống. Phương thức này trả về số nguyên lớn nhất nhỏ hơn hoặc bằng số thập phân bạn nhập. Ví dụ, nếu bạn nhập 4.7, kết quả sẽ là 4.
4. `Math.Ceiling()`: Làm tròn lên. Phương thức này trả về số nguyên nhỏ nhất lớn hơn hoặc bằng số thập phân bạn nhập. Ví dụ, nếu bạn nhập 4.7, kết quả sẽ là 5.
5. `Math.Min()`: Tìm giá trị nhỏ nhất giữa hai số. Ví dụ, `Math.Min(3, 7)` sẽ trả về 3.
6. `Math.Max()`: Tìm giá trị lớn nhất giữa hai số. Ví dụ, `Math.Max(3, 7)` sẽ trả về 7.
7. `Math.Pow()`: Tính lũy thừa của một số. Ví dụ, `Math.Pow(2, 3)` sẽ trả về 8, vì 2 lũy thừa 3 bằng 2 * 2 * 2.
8. `Math.Round()`: Làm tròn số thập phân. Ví dụ, `Math.Round(4.5)` sẽ trả về 5.
9. `Math.Sqrt()`: Tính căn bậc hai của một số. Ví dụ, `Math.Sqrt(16)` sẽ trả về 4, vì 4 * 4 = 16.

</v-clicks>

---

# Math.PI

<v-clicks>

- **Math.PI**: Lấy giá trị hằng số Pi(π) được định nghĩa trong lớp Math, giá trị xấp xỉ 3.14, thường được sử dụng trong các phép tính liên quan đến hình tròn.

```cs
double piValue = Math.PI;
Console.WriteLine("Math.PI: " + piValue);
```

**Thực hành**:

1. Nhập bán kính `r` của đường tròn.
2. Tính diện tích hình tròn: Diện tích = π x r^2
3. Hiển thị diện tích lên màn hình.

```cmd
Nhập bán kính của đường tròn: 5
Diện tích hình tròn là: 78.53981633974483
```

</v-clicks>

---

# Math.Abs()

<v-clicks>

- **Math.Abs()**: Phương thức này trả về giá trị tuyệt đối của một số, tức là giá trị dương của số đó, giúp loại bỏ dấu âm nếu có.

```cs
int absoluteValue = Math.Abs(-10);
Console.WriteLine("Math.Abs(-10): " + absoluteValue);
```

**Thực hành**:
1. Nhập một số từ bàn phím.
2. Tính giá trị tuyệt đối của số đó và hiển thị kết quả.

```cmd
Nhập một số từ bàn phím: -7.8
Giá trị tuyệt đối của -7.8 là: 7.8
```

</v-clicks>

---

# Math.Floor()

<v-clicks>

- **Math.Floor()**: Phương thức này làm tròn xuống một số thập phân đến số nguyên lớn nhất nhỏ hơn hoặc bằng số đó.

```cs
double number = 7.8;
double flooredValue = Math.Floor(number);
Console.WriteLine("Math.Floor(7.8): " + flooredValue);
```

**Thực hành**:
1. Nhập số thập phân từ bàn phím.
2. Sử dụng phương thức `Math.Floor()` để làm tròn xuống và hiển thị kết quả.

```cmd
Nhập một số thập phân: 5.3
Giá trị làm tròn xuống của 5.3 là: 5
```

</v-clicks>

---

# Math.Ceiling()

<v-clicks>

- **Math.Ceiling()**: Phương thức này làm tròn lên một số thập phân đến số nguyên nhỏ nhất lớn hơn hoặc bằng số đó.

```cs
double number = 7.8;
double ceilingValue = Math.Ceiling(number);
Console.WriteLine("Math.Ceiling(7.8): " + ceilingValue);
```

**Thực hành**:
1. Nhập số thập phân từ bàn phím.
2. Sử dụng phương thức `Math.Ceiling()` để làm tròn lên và hiển thị kết quả.

```cmd
Nhập một số thập phân: 4.7
Giá trị làm tròn lên của 4.7 là: 5
```

</v-clicks>

---

# Math.Round()

<v-clicks>

- **Math.Round()**: Phương thức này làm tròn một số thập phân đến số nguyên gần nhất. Nếu phần thập phân là 0.5 hoặc lớn hơn, nó sẽ làm tròn lên; nếu nhỏ hơn 0.5, nó sẽ làm tròn xuống.

```cs
double roundedValue = Math.Round(4.455, 2);
Console.WriteLine("Math.Round(4.455, 2): " + roundedValue);

double roundedValue2 = Math.Round(4.446, 1);
Console.WriteLine("Math.Round(4.446, 1): " + roundedValue2);
```

**Thực hành**:
1. Nhập số thập phân từ bàn phím.
2. Sử dụng phương thức `Math.Round()` để làm tròn số thập phân đến số nguyên gần nhất.
3. Hiển thị kết quả lên màn hình.

```cmd
Nhập một số thập phân từ bàn phím: 3.78500
Kết quả làm tròn 2 chữ số sau dấu phẩy: 3.79
Kết quả làm tròn 3 chữ số sau dấu phẩy: 3.785
Kết quả làm tròn 4 chữ số sau dấu phẩy: 3.785
```

</v-clicks>

---

# Math.Max()

<v-clicks>

- **Math.Max()**: Phương thức này trả về giá trị lớn nhất trong hai số được truyền vào.

```cs
int maxValue = Math.Max(10, 20);
Console.WriteLine("Math.Max(10, 20): " + maxValue);
```

**Thực hành**:
1. Nhập 3 số nguyên từ bàn phím.
2. Tìm giá trị lớn nhất trong ba số đó. Hiển thị kết quả lên màn hình

```cmd
Nhập ba số nguyên từ bàn phím:
Nhập số thứ nhất: 5
Nhập số thứ hai: 8
Nhập số thứ ba: 3
Giá trị lớn nhất trong ba số là: 8
```

</v-clicks>

---

# Math.Min()

<v-clicks>

- **Math.Min()**: Phương thức này trả về giá trị nhỏ nhất trong hai số được truyền vào.

```cs
int minValue = Math.Min(10, 20);
Console.WriteLine("Math.Min(10, 20): " + minValue);
```

**Thực hành**:
1. Nhập 3 số nguyên từ bàn phím.
2. Tìm giá trị nhỏ nhất trong ba số đó. Hiển thị kết quả lên màn hình

```cmd
Nhập ba số nguyên từ bàn phím:
Nhập số thứ nhất: 5
Nhập số thứ hai: 8
Nhập số thứ ba: 3
Giá trị nhỏ nhất trong ba số là: 3
```

</v-clicks>

---

# Math.Pow()

<v-clicks>

- **Math.Pow()**: Phương thức này tính lũy thừa của một số, trong đó tham số đầu tiên là số cần tính và tham số thứ hai là số mũ.

```cs
double powerValue = Math.Pow(2, 3);
Console.WriteLine("Math.Pow(2, 3): " + powerValue);
```

**Thực hành**:
1. Nhập cơ số và số mũ từ bàn phím.
2. Sử dụng `Math.Pow()` để tính lũy thừa và hiển thị kết quả.

```cmd
Nhập cơ số: 3
Nhập số mũ: 4
Giá trị 3^4 là: 81
```

</v-clicks>

---

# Math.Sqrt()

<v-clicks>

- **Math.Sqrt()**: Phương thức này tính căn bậc hai của một số, chỉ nhận giá trị không âm.

```cs
double squareRootValue = Math.Sqrt(16);
Console.WriteLine("Math.Sqrt(16): " + squareRootValue);
```

**Thực hành**:
1. Nhập một số không âm từ bàn phím.
2. Sử dụng `Math.Sqrt()` để tính căn bậc hai và hiển thị kết quả.

```cmd
Nhập một số không âm: 25
Căn bậc hai của 25 là: 5
```

</v-clicks>

---
zoom: 0.8
---

# Tổng Kết: Toán Tử (Operators)

<v-clicks>

- **Toán tử** là các ký hiệu được sử dụng để thực hiện các phép toán trên biến và giá trị trong lập trình. Toán tử giúp chúng ta thao tác và xử lý dữ liệu một cách hiệu quả.
- **Các loại toán tử chính:**
    - **Toán tử số học:**
        - `+` (Cộng), `-` (Trừ), `*` (Nhân), `/` (Chia), `%` (Chia lấy dư).
    - **Toán tử so sánh:**
        - `==` (Bằng), `!=` (Khác), `>` (Lớn hơn), `<` (Nhỏ hơn), `>=` (Lớn hơn hoặc bằng), `<=` (Nhỏ hơn hoặc bằng).
    - **Toán tử logic:**
        - `&&` (Và), `||` (Hoặc), `!` (Không).
    - **Toán tử gán:**
        - `==` (Gán giá trị), `+=`, `-=`, `*=`, `/=`, `%=` (Gán kết hợp).
    - **Toán tử tăng/giảm:**
        - `++` (Tăng một), `--` (Giảm một).
- **Null và Nullable:**
    - **Null:** Giá trị đặc biệt cho biết biến không có giá trị.
    - **Nullable:** Cho phép kiểu giá trị nhận giá trị `null` bằng cách sử dụng `?`, ví dụ: `int? myNullableInt;`

</v-clicks>

---

# Tính diện tích và chu vi hình chữ nhật

- Viết một chương trình trong C# để tính diện tích và chu vi của một hình chữ nhật.
1. Yêu cầu người dùng nhập vào chiều dài và chiều rộng của hình chữ nhật từ bàn phím.
2. Tính diện tích bằng công thức: dt = cd x cr
3. Tính chu vi bằng công thức: cv = 2 x (cd + cr)
4. In kết quả diện tích và chu vi ra màn hình.
5. Kết quả console trông như sau:

```cmd
Nhập chiều dài của hình chữ nhật: 5
Nhập chiều rộng của hình chữ nhật: 3
Diện tích của hình chữ nhật là: 15
Chu vi của hình chữ nhật là: 16
```

---

# Khoảng cách giữa hai điểm

<v-clicks>

- Viết một chương trình để tính khoảng cách giữa hai điểm trong mặt phẳng 2D với tọa độ (x1, y1) và (x2, y2).
- Để tính khoảng cách giữa hai điểm, bạn có thể sử dụng công thức sau:
    - Khoảng cách = Math.Sqrt((x2 - x1)^2 + (y2 - y1)^2)
- Chương trình có gia diện như sau:

```cmd
Nhập tọa độ điểm 1:
X1: 3
Y1: 4
Nhập tọa độ điểm 2:
X2: 6
Y2: 8
Khoảng cách giữa điểm (3, 4) và điểm (6, 8) là: 5
```

</v-clicks>

---

# Hoán đổi giá tị của hai biến

- Viết một chương trình để hoán đổi giá trị của hai biến `a` và `b` mà không cần sử dụng biến trung gian