# Authentication bypass via flawed state machine

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_1.png "Lab9")

-	Mục tiêu: Truy cập vào giao diện admin và xóa tài khoản carlos

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_2.png "Lab9")

-	Ta sẽ Bruteforce xem trang web này có những path nào

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_3.png "Lab9")

=>	Phát hiện đường dẫn đến trang admin

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_4.png "Lab9")

=>	Không vào được vì không phải user của DontWannaCry

-	Vào email client, ta phát hiện ra trang Exploit này sẽ nhận toàn bộ email từ @exploit-0a9f000f04aebfe482b82567017e0054.exploit-server.net và tên miền phụ của nó. Tức là nó vẫn có thể nhận được: @dontwannacry.com.exploit-0a9f000f04aebfe482b82567017e0054.exploit-server.net

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_5.png "Lab9")

-	Tuy nhiên, Server vẫn có thể check xem sau @ có phải của dontwannacry.com thật không nên ta cần phải tìm cách để Server chỉ kiểm tra đến được chữ “m” của @dontwannacry.com.exploit-0a9f000f04aebfe482b82567017e0054.exploit-server.net

-	Đăng ký tài khoản mới với tài khoản email cực dài

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_6.png "Lab9")

-	Sau khi xác nhận thành công và đăng nhập, ta thấy rằng email đã bị rút gọn lại xuống 250 ký tự

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_7.png "Lab9")

=>	Ta có thể dựa vào điều này để thực hiện khai thác và rút gọn xuống chữ “m” trong email @dontwannacry.com.exploit-0a9f000f04aebfe482b82567017e0054.exploit-server.net

-	Đăng ký tài khoản mới. 

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_8.png "Lab9")

=>	Sau khi đăng nhập lại trang thì đã xuất hiện “Admin panel”

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_9.png "Lab9")

## Hoàn thành bài lab

![Lab9](/Nguyễn%20Xuân%20Hiếu/PortSwigger/Business%20Logic/Images/lab9_10.png "Lab9")
