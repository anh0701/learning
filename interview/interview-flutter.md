# Interview

1. Flutter là gì?

- open-source UI software development kit do Google tạo ra. Nó có thể được sử dụng để tạo ứng dụng đa nền tảng.

2. Dart là gì?
  
- là ngôn ngữ lập trình được sử dụng để phát triển các ứng dụng Flutter.

3. Lợi ích khi sử dụng Flutter?

- Flutter giảm lượng mã thông qua tính năng Hot Reload, cho phép phát triển ứng dụng nhanh hơn.
- Nó hỗ trợ việc phát triển đa nền tảng, cho phép bạn viết mã cho cả IOS và Android
- Flutter tối ưu hóa tốt cho các ứng dụng di động 2D

4. Hạn chế của Flutter?

- Kích thước ứng dụng: lớn so với ứng dụng được viết bằng Kotlin hoặc Swift
- Thư viện bên thứ ba: Flutter đang phát triển nên có thể sẽ gặp khó khăn khi tìm kiếm các thứ viện bên thứ ba để tích hợp 
- hiệu suất: có thể sẽ chậm so với ứng dụng native
- học hỏi và chuyển ngôn ngữ: quen với java hoặc swift thì sẽ cần thời gian và công sức khi đổi sang học Dart

5. Hãy giải thích cấu trúc của Flutter?

- widget là cốt lõi: trong flutter mọi thứ đều là widget. widget là thành phần giao diện cơ bản nhất tạo nên toàn bộ giao diện người dùng của ứng dụng, bản thân ứng dụng cũng là một widget
- Cấu trúc thư mục: 
  - folder quan trọng nhất là lib (có file source code main.dart). Đây là nơi bạn tạo ra các file .dart và viết code
  - hai folder là android và ios dùng cho việc triển khai ứng dụng trên các nền tảng tương ứng

6. Kể cách tính năng quan trọng của Flutter?

- Hot reload: thay đổi mã nguồn có thể xem ngay kết quả không cần khởi động lại ứng dụng
- AOT Compiler: giúp biên dịch mã nguồn thành mã máy trước khi chạy ứng dụng
- giao diện người dùng linh hoạt: có thể tùy chỉnh các widget để thích nghi với nhiều thiết bị và kích thước màn hình khác nhau
- hỗ trợ nhiều widget
- đa nền tảng: phát triển được ứng dụn cho ios, android cùng một mã nguồn
- hiệu năng cao

7. Kể tên một số trình soạn thảo (editor) tốt nhất cho Flutter?

- vs code

8. Bạn hiểu thế nào về Streams

- 

9.  Kể tên một số loại hình khác nhau của Streams

-

10.   Bạn hiểu như nào về Flutter SDK

- là bộ công cụ phát triển giao diện người dùng đa nền tảng

11.  Sự khác nhau giữa Hot reload và hot restart

- Hot reload: không chạy lại hàm main(), initState(), sử dụng trong chế độ debug, cho phép thấy thay đổi ngay sau khi sửa lỗi, xây dựng giao diện người dùng và thêm tính năng mà không cần chạy lại ứng dụng từ đầu
- Hot restart: xóa trạng thái của ứng dụng, đặt lại trạng thái mặc định

12. Giải thích BuildContext là gì

- Trong Flutter, BuildContext là một khái niệm quan trọng, đại diện cho thông tin về vị trí của widget trong cây widget của ứng dụng. Nó chứa thông tin về vị trí của widget, cũng như cách truy cập đến các thuộc tính của các widget xung quanh. Mỗi widget trong Flutter đều có một BuildContext duy nhất mô tả vị trí của nó trong cây widget BuildContext cung cấp quyền truy cập đến các thuộc tính của widget, như màu sắc, kích thước, hình dạng, vị trí trong cây widget, và một số thông tin khác. Nó giống như một tham chiếu đến vị trí của widget trong cây widget, giúp xác định vị trí của widget trong widget tree

13. Làm thế nào để tạo Https request trong Flutter

- cài package, dùng http.get() để lấy get request

14. Kể tên 2 loại cơ sở dữ liệu thường dùng trong Flutter

- SQLite, Firebase

15. Bạn hiểu như nào về tween animation

- Trong Flutter, Tween là một lớp quan trọng để tạo hiệu ứng animation mượt mà. Nó giúp xác định đường đi của animation giữa hai giá trị - một giá trị ban đầu và một giá trị kết thúc. Khi bạn muốn tạo hiệu ứng animation cho một widget, Tween sẽ là công cụ bạn cần, định nghĩa khoảng giá trị mà animation sẽ diễn ra, ví dụ như giá trị từ 0.0 đến 1.0 để làm mờ một widget. Đồng thời, bạn cần sử dụng AnimationController để điều khiển thời gian của animation và áp dụng giá trị hiện tại của Tween vào thuộc tính bạn đang animation.

16. Phân biệt Stateless Widget và Stateful Widget
    - Stateless: không thay đổi trạng thái sau khi được tạo ra (VD: hiển thị văn bản tĩnh)
    - Stateful: có trạng thái và có thể thay đổi khi được tạo ra (VD: biểu mẫu đăng nhập)
17. Lifecycle của Widget là gì
    - gồm các giai đoạn: create, build, update, dispose
18. Kể tên một số widget thông dụng trong flutter
    - Container, Column, Text, Stack, Row, ListView, SingleChildScrollView, GridView

19.
- Atomic Design là một phương pháp thiết kế giao diện được sáng tạo bởi Brad Frost, một Web Designer đến từ Mỹ. Thay vì thiết kế một trang hoàn chỉnh, Atomic Design tập trung vào việc tạo từng thành phần (gọi là Component) riêng lẻ trên giao diện, sau đó kết hợp chúng thành một hệ thống phù hợp.
Trong Atomic Design, giao diện được chia thành 5 phần chính:
    1. Atoms: Là thành phần nhỏ nhất, ví dụ như các khối cơ bản như nút bấm, trường nhập liệu, checkbox, và liên kết. Chúng cũng có thể là các yếu tố trừu tượng như màu sắc và font chữ.
    2. Molecules: Gồm các Atoms kết hợp với nhau để tạo thành các phần tử bên ngoài, ví dụ như khung tìm kiếm.
    3. Organisms: Nhóm các Molecules giống nhau hoặc khác nhau để tạo thành một thành phần hoàn chỉnh của giao diện, ví dụ như header trang.
    4. Templates: Kết hợp các Organisms với nhau để tạo thành các trang.
    5. Pages: Là các mẫu cụ thể, kiểm tra cách các Templates hoạt động với nội dung thực tế
