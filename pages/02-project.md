# Project

- Một project trong .NET C# chứa mã nguồn, tài nguyên và các tệp cấu hình cần thiết cho ứng dụng hoặc thư viện.

<v-clicks>

1. Project chứa **tất cả các tệp mã nguồn** và thư mục liên quan đến ứng dụng, giúp bạn dễ dàng truy cập.
2. Tệp được **sắp xếp theo cấu trúc rõ ràng**, giúp bạn dễ dàng tìm kiếm và bảo trì mã.
3. Ngoài mã, Project còn bao gồm các **tệp cấu hình, hình ảnh, âm thanh** và các tài nguyên khác cần thiết cho ứng dụng.

</v-clicks>

---

# Tạo Chương Trình Đầu Tiên

<v-clicks>

1. Chọn Thư Mục Lưu Trữ Project
2. Gõ lệnh sau vào terminal để tạo một ứng dụng console mới.

```sh
dotnet new console -n HelloWorld
```

- `dotnet`: làm việc với **dotnet CLI** luôn luôn bắt đầu bằng từ khóa này.
- `new`: Chỉ ra rằng tạo một chương trình mới.
- `console`: kiểu chương trình muốn tạo mới. Trong trường hợp này là `console application`.
- `-n HelloWorld`: Đặt tên cho dự án của mình cụ thể là **HelloWorld**.

3. Thực thi chương trình:

```bash
cd HelloWorld                       # Sử dụng lệnh sau để di chuyển vào thư mục chứa project
dotnet run                          # Chạy chương trình
```

</v-clicks>

---

# Cấu trúc Project

<v-clicks>

1. **File `HelloWorld.csproj`**: Đây là tệp cấu hình project, nơi lưu trữ thông tin về cách **tổ chức** và **cấu hình** project của bạn. Tệp này giúp .NET biết cách xây dựng và chạy ứng dụng.
2. **File `Program.cs`**: Tệp này chứa mã nguồn cho ứng dụng console của bạn. Nó thường bao gồm phương thức Main, nơi bắt đầu chương trình của bạn. Đây là nơi bạn sẽ viết mã để thực hiện các chức năng của ứng dụng.
3. **Thư mục `bin` và `obj`**:
   - `bin`: Thư mục này chứa các tệp tin đã được **biên dịch** và sẵn sàng để chạy. Đây là nơi bạn tìm thấy các tệp thực thi của ứng dụng.
   - `obj`: Thư mục này chứa các tệp tin **tạm thời** và thông tin liên quan đến quá trình biên dịch. Nó giúp quá trình xây dựng ứng dụng diễn ra nhanh hơn.

</v-clicks>

---

# File `HelloWorld.csproj`

<v-clicks>

- Đây là tệp cấu hình cho project của bạn, được viết bằng **XML** (Extensible Markup Language), giúp định nghĩa cách .NET xây dựng và chạy ứng dụng.

```ts
<Project Sdk="Microsoft.NET.Sdk"> <!--Xác định phiên bản SDK mà project sẽ sử dụng-->

  <PropertyGroup> <!--Chứa các thuộc tính và cài đặt project-->
    <OutputType>Exe</OutputType> <!--Ứng dụng sẽ được biên dịch thành một tệp thực thi (executable)-->
    <TargetFramework>net9.0</TargetFramework> <!--Phiên bản .NET sử dụng để thực thi chương trình-->
    <ImplicitUsings>enable</ImplicitUsings> <!--Tự động thêm các thư viện phổ biến mà không dùng using-->
    <Nullable>enable</Nullable> <!--Bật tính năng quản lý giá trị null để tránh lỗi do null gây ra-->
  </PropertyGroup>

</Project>
```

</v-clicks>

---

# File `Program.cs`

<v-clicks>

- Đây là nơi bạn sẽ viết mã C# cho ứng dụng của mình. Tất cả các tệp có phần mở rộng là `.cs` đểu chứa mã nguồn C#.
- Tệp `Program.cs` chính là điểm khởi đầu cho chương trình của bạn. Mọi thứ sẽ bắt đầu từ đây!

1. Hãy thử thay đổi mã trong `Program.cs` như sau:

```ts
// See https://aka.ms/new-console-template for more information
Console.WriteLine("Hello, World!");
```

2. Để chạy chương trình, bạn chỉ cần thực hiện lệnh sau trong terminal

```bash
dotnet run
```

- Khi bạn chạy chương trình, **C# compiler** sẽ biên dịch mã của bạn trước, sau đó thực thi chương trình. Điều này đảm bảo rằng mọi thứ hoạt động như mong đợi!

</v-clicks>

---

# Thư mục `bin` và `obj`

<v-clicks>

- `bin/`: Đây là nơi lưu trữ các tệp thực thi mà bạn có thể chạy sau khi biên dịch. Bạn sẽ tìm thấy tệp `.exe` ở đây!
- `obj/`: Thư mục này chứa các tệp tạm thời và tài nguyên cần thiến cho quá trình biên dịch. Chúng giúp hỗ trợ quá trình biên dịch nhưng không cần thiết cho việc chạy chương trình.
- Mỗi khi bạn biên dịch hoặc chạy chương trình, cả `bin` và `obj` sẽ tự động được cập nhật để phản ánh các thay đổi mới nhất.

1. Thử thay đổi mã trong `Program.cs` như sau:

```ts
Console.WriteLine("Hello, Guys!");
Console.ReadKey(); // Chờ người dùng nhấn phím bất kỳ
```

2. Biên dịch chương trình bằng lệnh `build`

```sh
dotnet build
```

3. Hãy kiểm tra ngày tạo của các tệp và thư mục trong `bin` và `obj` để thấy sự khác biệt.
4. Mở thư mục `bin`, tìm tệp `.exe` và double click để chạy chương trình. Hãy xem kết quả trên màn hình!

</v-clicks>

---

# Console application

<v-clicks>

- Ứng dụng Console là loại chương trình chạy trên giao diện dòng lệnh, cho phép người dùng nhập lệnh và nhận kết quả dưới dạng văn bản.
- **Tệp .exe**:
  - Là tệp thực thi của ứng dụng Console.
  - Khi bạn chạy tệp này, hệ điều hành sẽ thực hiện mã nguồn đã được biên dịch.
- Cách tạo tệp .exe:
  1. **Biên dịch ứng dụng Console**: Khi bạn biên dịch, hệ thống sẽ tạo ra tệp .exe trong thư mục `bin`.
  2. **Chạy trực tiếp**: Tệp .exe có thể được chạy trên máy tính mà không cần môi trường phát triển.

</v-clicks>

---

# Intermediate Language

<v-clicks>

- Khi code C# được biên dịch chúng được chuyển đổi thành **Intermediate Language** trước khi thực thi.

1. Tìm kiếm từ khóa **"Developer Command Prompt for VS 2022"** trên máy tính và nhập

```sh
ILDASM
```

2. **Mở tệp DLL**:

- Trong của sổ ILDASM, chọn menu **File > Open**.
- Điều hướng đến thư mục dự án của bạn: `\bin\Debug\net9.0`.
- Chọn tệp `HelloWorld.dll`. Bạn sẽ thấy nội dung của tệp này.
- Tệp `.dll` là viết tắt của **Dynamic Link Library** và đây là kết quả mà trình biên dịch C# tạo ra khi chuyển đổi mã nguồn sang ngôn ngữ trung gian.

</v-clicks>

---

# Push chương trình đầu tiên lên gitlab

<v-clicks>

1. Khởi tạo Git local
2. Bỏ qua các thư mục không cần thiết với .gitignore

```ts
bin/
obj/
.vs/
```

</v-clicks>
