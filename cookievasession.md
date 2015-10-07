
##Giới thiệu Cookies và Session trong php
##Mục đích của sesion:
lưu trữ thông tin người dùng tạm thời trên server,khi người dùng thoát ra thì tài khoản, mật khẩu… sẽ bị mất.
Mục đích của cookie:
   


Biết được thông tin người sư dụng để có những phản hồi từ máy chủ cho biết: vd lần cuối đổi mk, thời gian đăng nhập web.

Bất kỳ một trang web nào cũng có các phiên làm việc riêng, việc này giúp website tương tác với từng user từ đó thu thập các thông tin riêng biệt và cần thiết. Để làm dc việc này ta dùng cookie và session. Bây giờ chúng ta sẽ tìm hiểu cách sử dụng của hai loại biến này.<br>
- cookies<br>
	Lưu thông tin người dùng:<br>
	Lưu trong máy client(máy khách), trong vùng do<br> brownser quản lý.<br>
	Không dùng cookies để lưu thông tin quan trọng vì nó không đảm bảo<br>
-	Tạo cookie<br>
Setcookie(“tên cookie”, giá trị,[thời điểm quá hạn]);
Nếu không có thời gian chỉ định thì người dùng thoát ra brownser sẽ bị mất.<br>
	Sử dụng $_cookie(“tên”); để brownser xóa cookie<br>
Session:<br>
	Đối tượng chứa thông tin người dùng trên server:
	Mỗi người dùng có 1 session riêng.<br>
	Cấu trúc session của mỗi người giống nhau chỉ khac nhau giá trị các biến<br>
	$_session là dãy toàn cục trong php dùng để chứa các biến session do đó dữ liệu trong session có thể được truy xuất từ mọi trang trong php.<br>
*) khai báo và sử dụng:<br>
	$_session[“tên biến”]<br>
Trên tất cả các trang phải có hàm này để dùng đk session:
Vd: $_session[“dangnhap”]=1<br>
// hàm isset để kiểm tra tồn tại của biến.<br>
•  session_destroy(): Cho phép hủy bỏ toàn bộ giá trị của session<br>
•  session_unset(): Cho phép hủy bỏ session- <br>
##Kết luận: <br>
Vậy là đã tìm hiểu sơ lược về cookie và sesion cơ bản về thì hai loại biến này hoàn toàn giống nhau chỉ là cookie thì là biến ở clien hoạt động ở trình duyệt, session thì ở server. Biến này dùng để quản lý các phiên làm việc của một mảng nào đó chẳng hạn của 1 user. Khi bạn khai báo biến session hay cookie trong thời gian sống của nó thì ở bất kỳ trang nào trong site bạn cũng đều sử dụng được biến này. <br>


 

