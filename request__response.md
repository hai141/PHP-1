##Tìm Hiểu vể request và response
HTTP cho phép giao tiếp giữa rất nhiều loại server/client với nhau, chủ yếu thông qua TCP/IP, tuy nhiên bất kỳ giao thức đáng tin cậy nào khác cũng có thể được dùng. Cổng giao tiếp chuẩn là 80, tuy nhiên có thể dùng bất kỳ cổng khác.<br>
<b>Giao tiếp giữa client và server dựa vào một cặp request/response. </b>
	 <br>
* Client khởi tạo HTTP request và nhận HTTP response từ server gửi về.
*  client đưa ra các request, và server sẽ trả lời các request này.
<br>


<b> HTTP request bao gồm hai thành phần quan trọng là URL và Verb (phương thức) </b>, được gửi từ client. Ở phía ngược lại,
<br> server trả về HTTP response trong đó chứa Status code và Message body.
