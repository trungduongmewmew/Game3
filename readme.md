Crackme là một chương trình máy tính nhỏ được thiết kế để kiểm tra kỹ năng dịch ngược (reverse engineering) của lập trình viên. Chúng được tạo ra như một cách hợp pháp để thực hành việc bẻ khóa phần mềm mà không vi phạm quyền sở hữu trí tuệ.  

Trong các cuộc thi Capture The Flag (CTF), crackme thường được sử dụng như một dạng thử thách trong lĩnh vực reverse engineering. Người tham gia cần phân tích mã nguồn của chương trình để tìm ra cách hoạt động, từ đó xác định "flag" – thường là một chuỗi ký tự ẩn trong chương trình. Các crackme này thường tích hợp các cơ chế bảo vệ và thuật toán tương tự như trong phần mềm thương mại, đôi khi còn phức tạp hơn với các kỹ thuật đóng gói hoặc bảo vệ tiên tiến, nhằm làm cho việc phân tích và chỉnh sửa trở nên khó khăn hơn. 

Ngoài ra, còn có một biến thể gọi là keygenme, yêu cầu người dịch ngược không chỉ xác định thuật toán bảo vệ được sử dụng trong ứng dụng mà còn phải tạo ra một chương trình tạo khóa (key generator) nhỏ bằng ngôn ngữ lập trình mà họ chọn. Các keygenme thường sử dụng các kỹ thuật chống gỡ lỗi và chống dịch ngược để gây khó khăn cho quá trình phân tích.  


Hôm nay chúng ta sẽ làm một bài nhỏ về crackme  

Giải nén tập tin Game3.zip ta thu được 02 file : *crackme.exe* và *msvcr100d.dll*  

Chạy chương trình crackme.exe bằng cmd ta thu được kết quả sau :  
      ![atl](images/Num1.png)  
 Kết quả trên cho ta thấy , chương trình sẽ chạy dưới dạng " game3.exe password " nghĩa là cần chạy chương trình tên là game3.exe trên cmd và cung cấp đầu vào là một chuỗi password.  
 
 
Tôi đã thử cung cấp vào chuỗi password là "duongdt" kết quả trả về là Fail! . Vì vậy nhiệm vụ của chúng ta là phân tích mã nguồn và tìm ra chuỗi password này.  

Có nhiều chương trình hổ trợ để phân tích mã nguồn, trong bài này chúng ta sẽ sử dụng công cụ [IDAFree](https://hex-rays.com/ida-free)  

Giao diện khi load file crackme.exe vào ida:  

      ![atl](images/Num2.png)   
Khi chạy chương trình trên cmd , chúng ta thấy xuất hiện từ khoá *usage* vì vậy chúng ta sẽ search từ khoá này trên IDA. Mã hợp ngữ của chương trình xuất hiện, cùng phân tích mã hợp ngữ này  
    ![atl](images/Num3.png)   

Như chúng ta thấy , chương trình này có phân nhánh nên có thể là thực hiện các câu lệnh điều kiện. Nhìn vào mã nguồn , dễ dàng thấy rằng câu điều kiện kiểm tra đầu vào game3.exe với chuỗi *dromedary* thì chương trình sẽ in ra câu *Congratulations!  You solved the crackm* .   Vì yêu cầu chương trình đầu vào là game3.exe nên ta sẽ đổi tên tệp crackme.exe và chạy chương trình   
 ![atl](images/Num4.png) 