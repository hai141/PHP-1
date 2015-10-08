##GET & POST
##Phương thức get và post trong php
 đó là phương thức truyền dữ liệu từ Client  lên Server.<br>
+ Có 2 cách gửi dữ liệu từ Client lên Server đó là dùng phương thức GET hoặc phương thức POST, cả 2 cách này bản chất lập trình viên mới biết chứ người dùng họ không quan tâm đến nó là cái gì, trừ khi là hacker :D. Để không mất thời gian nữa ta sẽ đi vào tìm hiểu từng cách, so sánh chúng với nhau và bàn luận xem khi nào ta dùng POST, khi nào ta dùng GET.<br>
## Phương Thức GET Trong PHP
Phương thức GET là phương thức gửi dữ liệu thông qua đường dẫn URL nằm trên thanh địa chỉ của Browser. Server sẽ nhận đường dẫn đó và phân tích trả về kết quả cho bạn. Server sẽ phân tích tất cả những thông tin đằng sau dấu hỏi (?) chính là phần dữ liệu mà Client gửi lên.<br>
Ví dụ:  Với URL freetuts.net?pass=12345 thì Server sẽ nhận được giá trị pass = 12345 <br>
ất cả các dữ liệu mà Client gửi lên bằng phương thức GET đều được lưu trong một biến toàn cục mà PHP tự tạo ra đó là biến $_GET, biến này là kiểu mảng kết hợp lưu trữ danh sách dữ liệu từ client gửi lên theo quy luật key => value <br>
## Phương Thức POST Trong PHP
POST sẽ gửi dữ liệu qua một cái form HTML và các giá trị sẽ được định nghĩa trong các input gồm các kiểu (textbox, radio, checkbox, password, textarea)và được nhận dang thông qua tên (name) của các input đó.<br>
Server Nhận Dữ Liệu
Tất cả các dữ liệu gửi bằng phương thức POST đều được lưu trong một biến toàn cục $_POST do PHP tự tạo ra, vì thế để lấy dữ liệu gửi lên bạn chỉ cần mổ xẻ thằng này là được. Cũng như lưu ý với các bạn là trước khi lấy phải dùng hàm isset($bien) để kiểm tra có hay không nhé.<br>
## Phân biết post và Get
* Phương thức POST bảo mật hơn GET vì dữ liệu được gửi ngầm bằng mắt thường không thể nhìn thấy được.<br>
  ![post va get](http://3.bp.blogspot.com/-4lp7Dx7VuVQ/VbGdOEx_PCI/AAAAAAAABis/-5mtrQiK6jA/s1600/s.jpg);
* Phương thức GET luôn luôn nhanh hơn POST vì dữ liệu gửi đi được Browser giữ lại trong cache, khi thực thi với POST thì Server luôn thực thi lệnh rồi trả về cho Client, còn với GET thì Browser sẽ kiểm tra trong cache có chưa, nếu có thì trả về ngay chứ không cần gửi lên Server.
* Khi dữ liệu bạn muốn SEO thì phải sử dụng phương thức GET.
* Khi dữ liệu bạn không cần bảo mật thì dùng phương thức GET, ngược lại dữ liệu bảo mật thì dùng phương thức POST.
* Ví dụ khi đăng nhập, Comment, đăng tin dùng phương thức POST. Còn khi lấy tin ra thì dùng phương thức GET…
