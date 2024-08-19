# Excessive trust in client-side controls

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_1.png "Lab1")

- Mục tiêu: Mua sản phẩm "Lightweight l33t leather jacket"

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_2.png "Lab1")

- Đăng nhập tài khoản người dùng đề bài cung cấp

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_3.png "Lab1")

- Thử truy cập sản phẩm thì ta thấy rằng giá của sản phẩm là 1337$ -> Không thể mua.

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_4.png "Lab1")

- Tuy nhiên, ta vẫn có thể thêm vào giỏ hàng

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_5.png "Lab1")

- Bắt gói tin bằng BurpSuite thì ta thấy khi thêm sản phẩm vào giỏ hàng sẽ đưa một vài trường dữ liệu dễ tổn thương

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_6.png "Lab1")

- Ta có thể thử sửa đổi trường price về 1 và gửi lại server bằng Repeater

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_7.png "Lab1")

=> Sản phẩm đã có giá 0.01$ và ta đã có thể mua nó

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_8.png "Lab1")

![Lab1](/Nguyễn Xuân Hiếu/PortSwigger/Business Logic/Images/lab1_9.png "Lab1")
