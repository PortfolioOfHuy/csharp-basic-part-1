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

```bash
bin/
obj/
.vs/
```

3. Push code lên remote

```bash
git add .                                           # Thêm tất cả các tệp vào git
git commit -m "Initial commit"                      # Lưu lại thay đổi
git remote add origin <remote_repository_url>       # Thêm đường dẫn đến kho chứa Gitlab
git push -u origin master                           # Đẩy mã lên nhánh chính (master)
```

4. Kiểm tra mã sau khi clone về

```bash
git clone remote_repository_url                     # clone source code
cd repository_folder                                # di chuyển vào repository
dotnet build                                        # build chương trình để sinh ra thư mục bin/ và obj
dotnet run                                          # run chương trình
```

</v-clicks>

---

# Cấu trúc một chương trình

<v-clicks>

- Một chương trình bao gồm nhiều câu lệnh được sắp xếp theo thứ tự để thực hiện một nhiệm vụ cụ thể, như chuyển tiền, quản lý bãi xe, ....

1. Câu lệnh (statement):
   - Đây là một dòng mã thực hiện một hành động cụ thể.
   - Các câu lệnh thường được viết theo thứ tự và kết thúc bằng dấu chấm phẩy.

```ts
Console.WriteLine("Hello, Guys!");
```

- Khi bạn xóa dấy chấm phẩy chương trình sẽ không biên dịch thành công và nhận được thông báo lỗi.

2. Sử dụng nhiều câu lệnh:

```ts
Console.WriteLine("Xin chào");
Console.WriteLine("Chúc mừng");
Console.WriteLine();
Console.WriteLine("Goobjob!!");
```

- `Console.WriteLine` được sử dụng để in dữ liệu lên màn hình và tự động xuống dòng sau khi in xong.

</v-clicks>

---

# Hiển thị Tiếng Việt trong Console

<v-clicks>

- Để Console hiển thị đúng Tiếng Việt và các ký tự đặc biệt (như emoji), cần thiết lập Encoding cho đầu ra:

```ts
Console.OutputEncoding = System.Text.Encoding.UTF8; // hiện icon và tiếng việt
Console.WriteLine("Xin chào 🙌");
Console.WriteLine("Chúc mừng 🔫🔫");
Console.WriteLine();
Console.WriteLine("Goobjob!!");
```

- Với dòng lệnh này, `Console` của bạn sẽ hiển thị Tiếng Việt cùng với các biểu tượng như emoji một cách chính xác.

</v-clicks>

---

# In ra nhưng không xuống dòng

<v-clicks>

```ts
Console.OutputEncoding = System.Text.Encoding.UTF8; // hiện icon và tiếng việt
Console.Write("Xin chào 🙌");
Console.Write("Chúc mừng 🔫🔫");
Console.Write();
Console.Write("Goobjob!!");
```

- `Console.Write` in ra màn hình mà không có dòng mới nào được thêm vào sau đó.

</v-clicks>

---

# Escape character

<v-clicks>

- **Escape character** là các ký tự đặc biệt được sử dụng trong chuỗi để biểu diễn các ký tự không thể để trực tiếp vào chuỗi. Chúng bắt đầu bằng dấu gạch chéo ngược (`\`).

```ts
Console.OutputEncoding = System.Text.Encoding.UTF8; // hiện icon và tiếng việt
Console.WriteLine('Dấu ngoặc kép " để biểu diễn ký tự ngoặc kép.');
Console.WriteLine("Dấu gạch chéo \\ để biểu diễn ký tự gạch chéo.");
Console.WriteLine("Tab \t để tạo khoảng trống trắng ngang.");
Console.WriteLine("Xuống dòng \n để tạo dòng mới.");
```

- `\"`: Dấu ngoặc kép.
- `\\`: Dấu gạch chéo.
- `\t`: Tạo khoảng trắng ngang (tab).
- `\n`: Tạo dòng mới (xuống dòng).

</v-clicks>

---

# Comment

<v-clicks>

- Sử dụng để chèn các lưu ý, giải thích hoặc mô tả vào trong code mà không ảnh hưởng đến logic của code.

1. Nhận xét trên một dòng:

```ts
// comment trên 1 dòng
Console.WriteLine("Hello, World!");
// Sau khi code thực thi
```

2. Nhận xét trên nhiều dòng:

```ts
/*
  Comment nhiều dòng
*/
Console.OutputEncoding = System.Text.Encoding.UTF8; // hiện icon và tiếng việt
Console.WriteLine("Xin chào 🙌");
Console.WriteLine("Chúc mừng 🔫🔫");
Console.WriteLine();
Console.WriteLine("Goobjob!!");
```

</v-clicks>

---

# Solution (file `.sln`)

<v-clicks>

- Khi phát triển ứng dụng .NET, bạn có thể có nhiều project khác nhau (như ứng dụng chính, thư viện, ...).
- **Solution** (.sln) giúp quản lý các project này một cách có tổ chức và hiệu quả.

1. Tạo 1 folder mới tên là `DemoSolution`
2. Tạo project console tên `Hello` trong thư mục này:

```bash
dotnet new console -n Hello
```

3. Tạo solution có tên là `HiSolution` ở thư mục root của folder `DemoSolution`

```sh
dotnet new sln -n HiSolution
```

4. Mở file `HiSolution.sln` để xem cấu trúc.
5. Thêm project `Hello.csproj` vào solution `HiSolution.sln`

```sh
dotnet sln HiSolution.sln add Hello\Hello.csproj
```

6. Mở file `HiSolution.sln` xem sự thay đổi

</v-clicks>

---

# Các thành phần cơ bản của Visual Studio

<v-clicks>

1. **Solution Explorer**:
   - Quản lý các tệp và project của bạn trong một cấu trúc cây dễ hiểu.
   - Giúp bạn dễ dàng truy cập và chỉnh sửa các tệp, thư viện trong project.
2. **Editor**:
   - Nơi bạn viết và chỉnh sửa mã nguồn.
   - Hỗ trợ đánh dấu cú pháp, gợi ý lệnh và công cụ kiểm tra lỗi.
3. **Output Window**: Hiển thị thông tin quá trình biên dịch, thông báo lỗi và các thông tin các khi chạy ứng dụng.
4. **Error List**: Hiển thị danh sách các lỗi trong project, giúp bạn dễ dàng xác định và sửa chửa.
5. **Toolbar**: Chứa các nút lệnh phổ biến như chạy chương trình (Run), dừng chương trình (Stop) và biên dịch (Build).

</v-clicks>

---

# Một vài loại project

<v-clicks>

1. **Windows Forms Application Project**: Dùng để phát triển các ứng dụng Windows truyền thống với giao diện dựa trên Windows Forms.
2. **Console Application Project**: Dùng để phát triển các ứng dụng dòng lệnh, cho phép người dùng nhập lệnh và nhận kết quả từ cửa sổ dòng lệnh.
3. **ASP.NET Web Application Project**: Dùng để phát triển các ứng dụng web ASP.NET, xây dựng trang web và dịch web trên nền tảng .NET.
4. **Class Library Project**: Dùng để phát triển các thư viện lớp, module hoặc thành phần có thể tái sử dụng.
5. **Unit Test Project**: Dùng để viết và chạy các bộ kiểm thử (unit tests) để đảm bảo chất lượng mã nguồn.
6. **WPF Application Project**: Dùng để phát triển các ứng dụng Windows với giao diện đồ họa hiện đại bằng **Windows Presentation Foundation**(WPF).
7. **Maui Project**: Dùng để phát triển các ứng dụng đa nền tảng chạy trên Windows, Android, iOS và macOS bằng **.NET MAUI**.

</v-clicks>

---

# Thêm mới project vào Solution

<v-clicks>

1. **Thêm Project mới**:
   - Chuột phải vào solution trong **Solution Explorer**.
   - Chọn **Add > New Project**...
2. **Chọn loại project**:
   - Trong cửa sổ **New Project**, chọn loại project bạn muốn thêm (Console, Web, Class Library,...).
   - Đặt tên và chọn thư mục chứa project, rồi bấm **Create**.
3. **Kiểm tra Project mới**:
   - Sau khi tạo, project mới sẽ xuất hiện trong **Solution Explorer** và bạn có thể bắt đầu làm việc với nó.

</v-clicks>

---

# Startup Project trong Solution Nhiều Project

<v-clicks>

- **Startup Project** là dự án sẽ chạy khi bạn nhấn "Start" hoặc "Debug" trong Visual Studio.

1. **Mở Solution Explorer**:
   - Tìm cửa sổ **Solution Explorer** trong Visual Studio.
2. **Chọn dự án**:
   - Nhấp chuột phải vào dự án bạn muốn chạy.
3. **Chọn "Set as Startup Project"**:
   - Từ menu hiện ra, chọn "**Set as Startup Project**".

</v-clicks>

---
zoom: 0.9
---

# Tạo mới Project và Solution với Visual Studio

<v-clicks>

1. **Mở Visual Studio**:
    - Chọn **Create a new project** từ màn hình chính khi mở Visual Studio.
2. **Chọn loại project**:
    - Trong cửa sổ **Create a new project**, chọn loại project bạn muốn tạo, ví dụ: **Console Application**, **ASP.NET Web Application** hoặc **Class Library**.
    - Bấm **Next**.
3. **Đặt tên và chọn ví trị lưu project**:
    - Đặt tên cho project và chọn vị trí lưu trên máy tính.
    - Đảm bảo chọn hộp kiểm **Place solution and project in the same directory** nếu bạn muốn tạo cả solution mới.
    - Bấm **Create**.
4. **Xem Solution và Project**:
    - Sau khi tạo, bạn sẽ thấy solution và project trong **Solution Explorer**. Bây giờ bạn có thể bắt đầu viết mã.

</v-clicks>

---
zoom: 0.9
---

# Thực hành Tạo Solution

1. **Tạo solution mới**:
    - Tạo một solution đặt tên là **"PoetrySolution"**.
2. **Tạo các Project**:
    - Tạo 3 Console Application với tên:
        - `Poem1Console`, `Poem3Console`, `Poem3Console`.
    - Mỗi project in một bài thơ của Nguyễn Bính.
    - Tạo 2 **Windows Forms Application** với tên:
        - `Poem1WinForms`, `Poem2WinForms`.
3. **Chạy từng project**:
    - Chạy riêng từng project để kiểm tra kết quả.
4. **Chạy toàn bộ project**:
    - Thiết lập để chạy đồng thời tất cả các project trong solution.

---
zoom: 0.9
---

# Thực hành Tạo Solution - Bài 2

1. **Tạo solution mới**:
    - Đặt tên Solution là **"LetCodeExercise"**.
2. **Thêm các Project Console Application**:
    - Tạo Project `BasicCalculator` và lập trình để in ra Console: `Hello BasicCalculator`.
    - Tạo Project `ScientificCalculator` và lập trình để in ra Console: `Hello ScientificCalculator`.
3. **Thêm Project kiểu Class Library**:
    - Tạo một Project kiểu Class Library trong Solution.
4. **Chạy và kiểm tra**:
    - Thiết lập từng Project Console làm Startup Project để chạy và kiểm tra kết quả trên Console.
5. **Tạo file .gitignore**:
    - Thêm file **.gitignore** vào Solution để loại bỏ các thư mục không cần thiết như `bin`, `obj`, `.vs`.
    - Push toàn bộ Solution đã tạo lên GitLab để lưu trữ.
    - Lấy đường link của Public Repository trên GitLab và ghi vào file bài tập để nộp.

---
zoom: 0.9
---

# Phím tắt cơ bản trên Visual Studio

1. **Lệnh `Console.WriteLine()`**:
    - Sử dụng `cw` + `tab` để nhánh chóng gọi `Console.WriteLine()`.
2. **Phím tắt comment và uncomment**:
    - `Ctrl + K + C` để comment đoạn code đã bôi đen.
    - `Ctrl + K + U` để bỏ comment đoạn code đã bôi đen.
3. **Nhân đôi dòng code**:
    - Sử dụng `Ctrl + D` để nhân đôi dòng code hiện tại.
4. **Build toàn bộ solution**:
    - `Ctrl + B`để biên dịch project hiện tại.
    - `Ctrl + Shift + B` để biên dịch toàn bộ solution.
5. **Phím tắt chạy chương trình**:
    - Sử dụng `F5` để bắt đầu chế độ Debug.
    - Sử dụng `Ctrl + F5` để chạy chương trình mà không qua chế độ Debug.

---

# OpenSource

<v-clicks>

- Open Source (Mã nguồn mở) là phần mềm hoặc dự án mà mã nguồn (code) của nó được công khai và có sẵn cho mọi người sử dụng, xem xét, chỉnh sửa và phát triển.
- **.NET**: [https://github.com/microsoft/dotnet](https://github.com/microsoft/dotnet)
- **Git**: [https://github.com/git/git](https://github.com/git/git)
- **Linux Kernel**: [https://github.com/torvalds/linux](https://github.com/torvalds/linux)

</v-clicks>

---
zoom: 0.85
---

# Cách Nộp Bài Tập

- Từ giờ, khi nộp bài tập, bạn hãy làm theo các bước sau:
1. **Tạo Nhánh mới**: Từ nhánh chính, tạo một nhánh mới cho bài tập của bạn.
    - Tạo nhánh: `Lecture-số-bài-tên-bài-tập`.
    - **Nhớ**: Mỗi nhánh chỉ dùng cho **một bài tập duy nhất**.
2. **Tạo Project mới**: Trong nhánh này, bạn tạo project mới cho bài tập.
3. **Lập Trình**: Tiến hành code trong project mới.
4. **Push lên GitLab**: Đưa nhánh của bạn lên GitLab để mọi người xem.
5. **Tạo Pull Request**: Sau khi push, hãy tạo một pull request để nhận xét.
6. **Tự kiểm Tra**: Kiểm tra lại code và để lại nhận xét trong pull request.
7. **Chụp Hình Chương Trình**: Lấy vài ví dụ chạy code vừa thực hành sau đó in ra console và chụp lại kết quả.
8. **Nhờ nhận xét**: Hãy nhờ các bạn xem xét code của bạn trong pull request.
9. **Approve và Merge**: khi nhận được sự đồng ý, bạn tự merge code qua giao diện pull request (Squash merge).
- Việc nhận xét và phản hồi lẫn nhau rất quan trọng giúp bạn học hỏi và cải thiện kỹ năng lập trình!

---
zoom: 0.6
---

# Chi tiết tạo Pull Request cho mỗi bài tập

1. **Chuẩn bị nhánh `master` mới nhất**:
    - Trước khi bắt đầu làm bài mới, đảm bảo nhánh `master` của bạn đã được cập nhật bằng cách pull code mới nhất từ remote.
2. **Tạo nhánh mới cho bài tập**:
    - Đứng trên `master`, tạo một nhánh mới cho bài tập hiện tập (ví dự: `feature/baitap1`).
    - Trong nhánh này, tạo project, làm bài tập và commit các thay đổi liên quan đến bài tập này.
3. **Push và tạo Pull Request**:
    - Push nhánh mới của bài tập lên remote.
    - Sau đó, tạo Pull Request (PR) từ nhánh bài tập vào `master`.
4. **Kiểm tra và tự đánh giá**:
    - **Chạy chương trình** với nhiều bộ dữ liệu khác nhau để kiểm tra tính chính xác của code.
    - **Chụp ảnh kết quả (output)** từ console của chương trình và dán vào phần comment của PR để người review có thể xem dễ dàng.
    - **Tự review lại code**: Kiểm tra các đoạn code xem có đoạn nào cần tối ưu hóa hoặc đoạn nào chưa rõ ràng.
5. **Hoàn tất PR và chờ review**:
    - Sau khi đã đảm bảo bài tập hoàn thiện, copy URL của PR và lưu vào file bài tập để tiện theo dõi.
    - Chờ phản hồi từ người review.
6. **Chuyển sang bài tập mới**:
    - Sau khi hoàn thành một bài tập, quay lại nhánh `master`.
    - Pull code mới nhất từ remote để đảm bảo `master` luôn được cập nhật.
    - Tiếp tục lặp lại quy trình trên cho bài tập tiếp theo.
- Lưu ý bổ sung:
    - **Giữ PR sạch sẽ**: Mỗi PR chỉ chứa code thay đổi của một bài tập để việc review dễ dàng và tránh xung đột không cần thiết.
    - **Đảm bảo code rõ ràng và tối ưu**: Kiểm tra lại từng đoạn code, cố gắng làm rõ ý đồ và tối ưu hóa các đoạn xử lý phức tạp trước khi gửi đi review.
    - **Đính kèm hình ảnh kết quả**: Dám ảnh output trực tiếp vào phần comment của PR giúp người review nhanh chóng nắm bắt kết quả và đánh giá tính chính xác của chương trình.