## Set
- Là 1 tập string ko trùng nhau

## Lệnh
- Sadd: `Sadd colors red` có nghĩa là thêm phân tử key vào 1 tập set có tên là colors. Trả về 0 tức là thêm failed, trả về 1 tức là thành công rồi
- Smember: `Smember colors` có nghĩa là lấy toàn bộ phần tử của 1 tập set có tên là colors


```
SADD colors1 red blue orange
SADD colors2 blue green purple
SADD colors3 blue red  purple
```

- Sunion:
```
SUNION colors1 colors2 colors3
```
Trả ra sẽ là `red blue orange green purple`


- SINTERSECTION:
Chỉ lấy phần tử ở set nào cũng có
```
SUNION colors1 colors2 colors3
```
Trả ra sẽ là `blue`

- SDIFF:
Chỉ lấy phần tử không có

```
SDIFF colors1 colors2 colors3
```
Trả ra sẽ là `orange`

- SISMEMBER:
Kiểm tra xem tập set đấy có key ko
```
SISMEMBER colors1 red
```
Nếu có trả ra 1 còn ko có thì trả ra 0

- SCARD
In ra số phần tử trong 1 tập
```
SCARD colors1
```
Trả ra 3

- SREM
Xóa phần tử ở trong 1 tập set
```
SREM colors1 red
```
Xóa phần tử red trong color1

- SMEMBERS
Trả về toàn bộ phần tử của 1 tập set
```
SMEMBERS colors1
```

- SSCAN
Trả về 1 tập phần tử trong tập set
```
SSCAN colors1 0 COUNT 2
```
Bắt đầu từ phần tử số 2