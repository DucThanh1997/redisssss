## List
- Nó là double-linked list

## Lệnh
- Lpush: Thêm 1 phần tử vào bên trái `LPUSH temps 25` trả về số lượng của list
- Rpush: Thêm 1 phần tử vào bên phải `RPUSH temps 35` trả về số lượng của list
- LLEN: Trả về số lượng của phần tử `LLEN temps` trả về 2
- LINDEX: Trả về giá trị của cái index đó `LLEN temps 0` trả về 25
- LRANGE: Trả về giá trị từ số đầu tiên đến số cuối cùng `LRANGE temps 1 3` 
- LPOS: Trả về index của giá trị mà mình tìm `LPOS temps 25` trả về 0
    + `LPOS temps 25 RANK 2`: Trả về index thứ 2 có giá trị là 25
    + `LPOS temps 25 RANK 2`: Trả về array index của 2 giá trị 25
    + `LPOS temps 25 MAXLENS 10`: Chỉ tìm index ở 10 phần tử đầu tiên
- LPOP: Xóa giá trị bên trái
- RPOP: Xóa giá trị bên phải
- LSET: `LSET temps 2 32` đặt giá trị 32 cho index 2
- LREM: `LREM temps 2 25` xóa 2 giá trị là 25 trong list
- LINSERT `LINSERT temps BEFORE 4 25` đặt giá trị là 25 trước phần tử thứ 4 nếu là after thì là sau phần tử thứ 4   