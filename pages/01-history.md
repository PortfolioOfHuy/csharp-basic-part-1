# Các Framework của .NET

| Framework          | Mục tiêu                                                 |
| ------------------ | -------------------------------------------------------- |
| **.NET Framework** | Phát triển ứng dụng trên Windows                         |
| **Mono**           | Phát triển ứng dụng trên hệ điều hành khác ngoài Windows |
| **Xamarin**        | Phát triển ứng dụng di động (Android, IOS)               |
| **.NET Core**      | Phát triển ứng dụng đa nền tảng (Linux, Windows, macOS)  |
| **.NET Standard**  | Chuẩn hóa để code chạy trên mọi nền tảng .NET            |

---

# .NET Platform

<v-click>

- .NET Platform là một hệ sinh thái phát triển ứng dụng do Microsoft phát triển, hỗ trợ nhiều loại ứng dụng và đa nền tảng.

</v-click>

<v-click>

1. **Ứng dụng Desktop:** Phát triển phần mềm chạy trên hệ điều hành Windows và macOS.
2. **Ứng dụng Web:** Xây dựng các ứng dụng web hiện đại, bảo mật và hiệu suất cao.
3. **Ứng dụng Di động:** Tạo ứng dụng cho Android, iOS và Windows thông qua Xamarin.
4. **Ứng dụng IoT (Internet of Things):** Phát triển giải phát cho các thiết bị thông minh và kết nối mạng.

</v-click>

---

# Thành phần quan trọng .NET

| Thành phần                        | Mô tả                                                                           |
| --------------------------------- | ------------------------------------------------------------------------------- |
| **Common Language Runtime (CLR)** | Môi trường thực thi (runtime) cho các chương trình, quản lý bộ nhớ và luồng.    |
| **.NET Base Class Library (BCL)** | Thư viện cơ sở với các hàm và giao diện hỗ trợ phát triển ứng dụng.             |
| **.NET Development Tools**        | Bộ công cụ hỗ trợ viết, gỡ lỗi và triển khai ứng dụng (VD: Visual Studio, CLI). |
| **.Nhiều Frameworks**             | Các frameworks khác nhau phục vụ nhiều loại ứng dụng (Web, Desktop, Mobile).    |
| **Programming Languages**         | Hỗ trợ nhiều ngôn ngữ như C#, F#, VB.NET để phát triển ứng dụng.                |

---

# [.NET SDK](https://dotnet.microsoft.com/en-us/download/visual-studio-sdks)

- **.NET SDK** (Software Development Kit) là bộ công cụ cần thiết để phát triển ứng dụng .NET. Nó bao gồm mọi thứ bạn cần để xây dựng, biên dịch và chạy ứng dụng.

<v-clicks>

1. **Biên dịch viên (Compiler):**
   - Chuyển đổi mã nguồn thành mã máy hoặc mã trung gian (IL).
2. **Thư viện .NET:**
   - Cung cấp các hàm và lớp để phát triển ứng dụng dễ dàng hơn.
3. **Công cụ dòng lệnh:**
   - Giúp tạo, xây dựng và chạy ứng dụng từ dòng lệnh (CLI).
4. **Templates:**
   - Các mẫu ứng dụng để giúp bạn bắt đầu nhanh chóng với các loại dự án khác nhau.

</v-clicks>

---

# Compile (biên dịch)

- Compile là quá trình chuyển mã nguồn từ ngôn ngữ lập trình cấp cao (như C#, Java) sang mã máy để CPU có thể thực thi trực tiếp.

<v-clicks>

1. **Quy trình Compile thông thường**

2. **.NET Compiler**

- Đầu tiên biên dịch mã C# thành **mã trung gian (IL)**.
- Sau đó IL được chuyển thành **mã máy** thông qua JIT (Just-In-Time).

</v-clicks>

---

# Compile-time vs Run-time

<v-click>

1. **Compile-time (Thời gian biên dịch):**
   - Là lúc chương trình được chuyển từ **mã nguồn** thành **mã máy** hoặc **mã trung gian**.
   - Các lỗi cú pháp sẽ được kiểm tra trong giai đoạn này.

</v-click>

<v-click>

2. **Run-time (Thời gian chạy):**
   - Là lúc chương trình **thực sự chạy** trên máy tính sau khi đã biên dịch xong.
   - Lúc này, chương trình tương tác với người dùng, dữ liệu và hệ thống.

</v-click>

<v-click>

3. **Tóm lại:**
   - **Compile-time:** Chuyển đổi và kiểm tra mã nguồn.
   - **Run-time:** Thực thi chương trình và xử lý các tác vụ thực tế.

</v-click>

---

# Common Language Runtime (CLR)

<v-clicks>

1. **CLR** là môi trường giúp **chạy ứng dụng .NET**.
2. Bạn có thể viết ứng dụng bằng **nhiều ngôn ngữ khác nhau** như C#, F#, VB.NET.
3. **CLR** tự động **quản lý bộ nhớ** cho bạn nhờ vào tính năng **Garbage Collection** (thu gom rác).
4. **Biên dịch mã trung gian (IL)** thành mã máy **khi chạy chương trình** bằng **Just-In-Time Compilation**.
5. Đảm bảo ứng dụng an toàn với **các cơ chế bảo mật** tích hợp.

</v-clicks>

---

# .NET Base Class Library

- **.NET Base Class Library (BCL)** là bộ sưu tập các thư viện cung cấp các chức năng cơ bản cho việc phát triển ứng dụng .NET.

<v-click>

1. `Console`: nhập/xuất dữ liệu thông qua màn hình console.
2. `String`: làm việc với chuỗi ký tự.
3. `DateTime`: làm việc với thời gian và ngày tháng.
4. `Math`: Chứa các phương thức toán học cơ bản như: max, min, v.v.
5. `File` và `Directory`: thao tác với tệp và thư mục trên hệ thống tệp.
6. `StreamReader` và `StreamWriter`: đọc và ghi dữ liệu vào các luồng.
7. `Exception`: xử lý các ngoại lệ (exceptions) trong ứng dụng. Và còn nhiều hơn nữa.

</v-click>

<v-click>

- Tại sao BCL quan trọng?
  - **Tiết kiệm thời gian**: Cung cấp nhiều chức năng sẵn có, giúp lập trình viên không phải viết lại từ đầu.
  - **Đảm bảo chất lượng**: Các thư viện đã được kiểm tra và tối ưu hóa, giảm thiểu lỗi trong ứng dụng.
  - **Tính nhất quán**: Đảm bảo các thành phần của ứng dụng hoạt động đồng bộ và hiệu quả.

</v-click>

---

# Công cụ phát triển ứng dụng .NET

<v-click>

1. **[.NET CLI](https://learn.microsoft.com/en-us/dotnet/core/tools/)**: Công cụ dòng lệnh giúp bạn tạo, xây dựng và quản lý ứng dụng .NET dễ dàng.
2. **[Visual Studio](https://visualstudio.microsoft.com/)**: Một phần mềm tuyệt vời để viết mã và gỡ lỗi ứng dụng .NET. Nó rất phổ biến và mạnh mẽ!
3. **[Visual Studio Code](https://code.visualstudio.com/)**: Một trình soạn thảo mã nhẹ và miễn phí, rất tốt cho những ai thích đơn giản và nhanh chóng.
4. **[NuGet](https://www.nuget.org/)**: Công cụ giúp bạn **cài đặt và quản lý thư viện** cho ứng dụng, giúp việc phát triển dễ dàng hơn.

</v-click>

---

# Programing language - ngôn ngữ lập trình

<v-clicks>

- Là hệ thống quy tắc và cú pháp dùng để viết code cho máy tính. Tạo ra các chương trình và ứng dụng.
- Ngôn ngữ lập trình phổ biến: C#, C, C++, java, Python, JavaScript,...
- C# đọc là CSharp: Là một ngôn ngữ lập trình phát triển bởi Microsoft. Phát triển ứng dụng web, desktop, di động và trò chơi.

</v-clicks>

---

# Một vài thuật ngữ

<v-clicks>

1. IDE viết tắt của Integrated Development Environment. Là phần mềm cung cấp môi trường giúp bạn phát triển ứng dụng dàng hơn: [Visual Studio](https://visualstudio.microsoft.com/), [Visual Studio Code](https://code.visualstudio.com/).
2. [.NET SDK(Software Development Kit)](https://dotnet.microsoft.com/en-us/download/visual-studio-sdks): là bộ công cụ cần thiết để phát triển ứng dụng .NET, bao gồm các thư viện và công cụ hỗ trợ.
3. .NET CLI (Command Line Interface): Tập hợp câu lệnh cho phép bạn tạo, xây dựng, chạy và quản lý ứng dụng .NET. Đi kèm cùng .NET SDK.

- **Cách kiểm tra SDK trên máy tính:**

1. Mở terminal bằng: 🪟 + X và chọn `terminal (admin)` đối với window 11 và `powershell (admin)` đối với window 10.
2. Gõ lệnh kiểm tra phiên bản .net sdk

```sh
dotnet --version
```

3. Kiểm tra danh sách SDK đã cài trên máy

```sh
dotnet --list-sdks
```

</v-clicks>
