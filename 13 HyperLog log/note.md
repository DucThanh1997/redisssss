## HyperLoglog
Khá giống với set nhưng nó giá trị mà nó điền vào và nó có fix sized 12kb thôi thay vì thằng set nếu tập giá trị lớn có thể lên đến 39MB và hơn nữa cho 1 key

## Lệnh
- PFADD: Đưa vào 1 string. Trả về 1 nếu nó mới còn trả về 0 nếu nó cũ `PFADD vegetables celery`
- PFCOUNT: Trả về xấp xỉ số lượng các phần tử unique mà bạn đã thêm vào