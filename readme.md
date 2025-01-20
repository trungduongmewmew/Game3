
Crackme là một chương trình máy tính nhỏ được thiết kế để kiểm tra kỹ năng dịch ngược (reverse engineering) của lập trình viên. Chúng được tạo ra như một cách hợp pháp để thực hành việc bẻ khóa phần mềm mà không vi phạm quyền sở hữu trí tuệ. 


Trong các cuộc thi Capture The Flag (CTF), crackme thường được sử dụng như một dạng thử thách trong lĩnh vực reverse engineering. Người tham gia cần phân tích mã nguồn của chương trình để tìm ra cách hoạt động, từ đó xác định "flag" – thường là một chuỗi ký tự ẩn trong chương trình. Các crackme này thường tích hợp các cơ chế bảo vệ và thuật toán tương tự như trong phần mềm thương mại, đôi khi còn phức tạp hơn với các kỹ thuật đóng gói hoặc bảo vệ tiên tiến, nhằm làm cho việc phân tích và chỉnh sửa trở nên khó khăn hơn. 


Ngoài ra, còn có một biến thể gọi là keygenme, yêu cầu người dịch ngược không chỉ xác định thuật toán bảo vệ được sử dụng trong ứng dụng mà còn phải tạo ra một chương trình tạo khóa (key generator) nhỏ bằng ngôn ngữ lập trình mà họ chọn. Các keygenme thường sử dụng các kỹ thuật chống gỡ lỗi và chống dịch ngược để gây khó khăn cho quá trình phân tích.

Hôm nay chúng ta sẽ làm một bài nhỏ về crackme 

Giải nén tập tin Game3.zip ta thu được 02 file : crackme.exe và msvcr100d.dll
Chạy chương trình crackme.exe bằng cmd ta thu được kết quả sau : 
    ![atl](images/Nu,1.png)
Kết quả trên cho ta thấy , chương trình sẽ chạy dưới dạng " game3.exe password " nghĩa là cần chạy chương trình tên là game3.exe trên cmd và cung cấp đầu vào là một chuỗi password. Vì vậy , nhiệm vụ của chúng ta là tìm ra password này. 
   