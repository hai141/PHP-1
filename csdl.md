##Kết nối vào cơ sở dữ liệu 
<b>. Để có thể làm việc trên CSDL, việc đầu tiên là phải kết nối (connect) vào CSDL </b> <br>
Để theo dõi chi tiết việc kết nối và thao tác trên CSDL, mình sẽ học lần lượt các cách để :<br>

<p>•	Kết nối vào CSDL (lấy chìa khóa mở cửa vào nhà)<br>
•	Chọn CSDL cần làm việc (vào nhà và chọn nơi làm việc)<br>
•	Ngắt kết nối với CSDL sau khi đã làm việc xong (khóa cửa lại, ra khỏi nhà)<br>
<b>1.	Kết nối(connection) </b><br>
để connect vào CSDL chúng ta dùng một hàm PHP: mysql_connect<br>
 mysql_connect("localhost","root","");   || mysql_connect("localhost","tên đang nhập vào csdl", "mật khẩu");<br>
hàm này cần có 3 thông số: địa chỉ máy chủ, username, pass<br>
<b>2.	Chọn CSDL làm việc</b><br>
Sau khi đã đăng nhập vào CSDL rồi, bạn cần phải lựa chọn tên CSDL mà bạn cần làm việc (nếu bạn có nhiều CSDL). Đối với các host miễn phí (như FREE.FR chẳng hạn) thì nó chỉ cho mình một CSDL thôi, vậy cũng quá đủ rồi! Và tên của CSDL này thường là trùng với username đăng nhập vào MySQL của bạn (do server tạo tự động).
Hàm PHP để lựa chọn CSDL: mysql_select_db (chữ db là viết tắt của DataBase)<br>
Code ví dụ:<br>
<?php <br>
mysql_connect("localhost","root",""); // đăng nhập vào CSDL trên máy tính<br>
mysql_select_db("taikhoan"); //Chọn CSDL tên là taikhoan<br>
?><br>
<b>3.	Ngắt kết nối </b><br>
Hàm để ngắt kết nối (đóng CSDL lại) : mysql_close();<br>
Phần 2: Lấy dữ liệu<br>
 Từ trên server<br>
2 ví dụ như ở trên server đã có cơ sở dữ liệu  làm sao để lấy ra và in ra màn hình.<br>
Sau đây là cách lấy:<br>
 bây giờ mình sẽ yêu cầu MySQL làm vài thứ bằng ngôn ngữ SQL. Viết một yêu cầu gọi là thực hiện một query . Mình sẽ nhờ MySQL in ra nội dung của cái bảng taikhoan mà hồi nãy mình có đề nghị bạn tải về đấy !
Để viết một query chúng ta sử dụng hàm PHP : mysql_query<br>
vd : 
<?php <br>
$traloi=mysql_query("SELECT * FROM taikhoan") ;<br>
?><br>
<b>3 In (hiển thị) kết quả của một query</b><br>
 $traloi của mình chứa một thứ gì đó không thể bung ra được, nghĩa là không giống như một biến bình thường chứa số hay chứa text<br> mà mình có thể dùng lệnh echo để in ra, mà nó chứa một thứ rất hỗn độn vô trật tự.
 nếu mà in ra lúc này dữ liệu sẽ bị in lung tung, hỗn độn.<br>
 sử dụng mảng trong php để in ra có trật tự<br>
$traloi là một biến chứa câu trả lời của MySQL, là một mớ hỗn độn vô trật tự có kiểu dữ liệu là resource (hiếm gặp từ này). <br>Nhờ vào hàm mysql_fetch_array mà mình tạo được mảng $dulieu ! Mảng này chứa 1 dòng trong bảng dữ liệu của mình, khi mình dùng hàm mysql_fetch_array một lần nữa thì mảng $dulieu sẽ chứa hàng thứ 2 trong bảng dữ liệu
</p>
