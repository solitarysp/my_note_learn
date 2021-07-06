# What is Blocking ?
- Blocking là việc chặn để đợi công việc đang thực hiện hoàn trước khi chuyển sang công việc tiếp theo.
- ![img.png](image/Blocking_NonBlocking_IO_synchronized_Asynchronized_img1.png)
- Các công việc đang bị chờ đợi sẽ có thể bị Failure khi chờ đợi quá lâu ( Ví dụ: Người xếp hàng chờ mua vé quá lâu. Sẽ bỏ đi về vì quá lâu).
# What is NON Blocking ?
- Với Non-blocking các công việc khi bắt đầu thực hiện sẽ không chặn việc thực hiện công việc mới. Các công việc mới có thể được thực hiện ngay lập tức.
  ![img_1.png](image/Blocking_NonBlocking_IO_synchronized_Asynchronized_img2.png)
- Thông thường, sau khi công việc hoàn thành sẽ gửi notification để tiếp tục xử lý logic nếu có sau khi công việc đó hoàn thành.
# I/O (Input / Output)
- I/O là việc giao tiếp giữa các hệ thống xử lý thông tin.
- Trong đó Input là 1 tín hiệu hoặc dữ liệu mà hệ thống nhận được. Output là các tín hiệu hoặc dữ liệu mà hệ thống đó gửi đi.
### Ví dụ giữa con người, bàn phím, máy tính và màn hình :
- Con người thực hiện hành động click chuột (Với context của chuột thì đây là input của chuột, Với context của con người là outpt của con người)
- Chuột nhận Input từ con người sau đó tiến hành gửi tiến hiệu đến máy tính (Với context của chuột thì là Output của chuột , với context của máy tính thì là input của máy tính )
- Máy tính nhận Input từ chuột, thực hiện gửi tín hiệu vị trí của chuột đến màn hình (Với context của máy tính thì là output của máy tính, với context của màn hình thì là input của màn hình)
- Màn hình nhận thông tin từ máy tính , thực hiện hiển thị vị trí chuột trên màn hình (Với context của màn hình thì là output của màn hình, với context của con người sẽ là input của con người)
# Blocking I/O
- Blocking i/O là việc chặn các công việc I/O được thực hiện hoàn thành trước khi thực hiện các công việc khác.
### Ví dụ
- Một công việc của chúng ta có 3 việc nhỏ. (Tính 1+1, lưu vào data base, tính 1+1 = 2)
- Tại công việc nhỏ thứ 2, chúng ta IO đến database. Nếu tại thời điểm này bị blocking thì được gọi là Blocknig I/O

