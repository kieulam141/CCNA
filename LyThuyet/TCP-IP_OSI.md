# Phân biệt mô hình OSI và TCP/IP
## I.Mô hình OSI có 7 lớp:
### 1.Lớp ứng dụng(Application)
- Quy định giao diện giữa ứng dụng và mạng.
- Các giao thức trong thuộc về lớp này rất nhiều, phổ biến: FTP, HTTP, HTTPs, SMTP, Telnet ...

### 2.Lớp Trình bày (Presentation)
- Chịu trách nhiệm chính về phần mã hóa và định dạng dữ liệu.
- VD: để máy tính Linux có thể giao tiếp với máy tính Windows, lớp Trình bày phải định dạng dữ liệu sao cho phù hợp với các hệ điều hành.

### 3.Lớp Phiên (Session) 
- Chịu trách nhiệm cung cấp và giải phóng các phiên làm việc thông qua việc cấp port cho các phiên này.
- 1 máy tính có thể vừa duyệt web, vừa gửi mail, vừa truyền file cho máy tính khác.Các hoạt động diễn ra đồng thời.

### 4.Lớp vận chuyển (Transport) 
- Đảm bảo thông tin chính xác giữa các thiết bị.
-  Các máy tính phải sử dụng kiểu truyền như thế nào cho phù hợp với môi trường truyền (môi trường ít lỗi hay nhiều lỗi), phải bắt tay trước khi truyền hay không, ... đều do lớp Vận chuyển quy định.
- Dữ liệu từ lớp Session đưa xuống sẽ được chia thành các đơn vị dữ liệu lớp Vận Chuyển, gọi là segment, các segment được đánh số thứ tự để bên nhận có thể ghép dữ liệu lại 1 cách chính xác.

### 5.Lớp Mạng (Network)
- Định ra địa chỉ logic cho các thiết bị mạng và quy định các nguyên tắc sử dụng địa chỉ logic này.
- VD: các giao thức như IP, IPX, Apple Talk có những cơ chế định địa chỉ cho máy tính và mạng máy tính trên mạng.
- Các giao thức: RIP, OSPF, EIGRP, BGP: định tuyến.
- Đóng gói các segment -> các gói tin(packet)

### 6.Lớp liên kết dữ liệu(Data Link)
- Xác định địa chỉ vật lý của các thiết bị trên mạng. (Địa chị MAC)
- Đóng gói các packet thành frames.

### 7.Lớp vật lý
- Biển đôi 0,1 thành các tín hiệu điện.

=>>>>> Mô hình OSI chỉ là mô hình tham chiếu k được đưa vào sử dụng trong thực tế.

## 2.Mô hình TCP/IP
- Mô hình được sử dụng nhiều nhất, giản lược của mô hình OSI
- Chỉ có 4 lớp: Ứng dụng ( 3 lớp 5 + 6 + 7), Vận chuyển (= vận chuyển của OSI), Internet (= network), Truy cập mạng ( 1+2 ).
- 1 số giao thức : IP (Internet Protocol), ICMP (Internet Control Message Protocol), TCP, UDP, Telnet, FTP, WWW, SMTP, ...
- Mô hình này gọn nhẹ hơn và biến đổi phù hợp với thực tế.
- 2 giao thức quan trọng nhất: TCP, UDP
- TCP đảm bảo độ tin cậy ( bằng các cơ chế xác thực, bắt tay), nhưng chậm.
- UDP ko có cơ chế tin cậy, nhưng nhanh hơn.
