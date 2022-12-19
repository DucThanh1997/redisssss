## Sorted set
- Là con lai giữa hash và set
- Chứa 1 tập key ko trùng nhau và value là 1 con số (int cũng được mà float cũng được), các key được sắp xếp theo thứ tự từ lớn đến bé
![image](https://user-images.githubusercontent.com/45547213/204095288-084d70b1-4629-47ee-bc89-fdd21db5841a.png)

## Lệnh sorted set
- ZADD: Để thêm key và value vào
```
ZADD products 45 monitor
```
Thêm key là monitor vào tập sorted set với value là 45

- ZREM: Để xóa key
```
ZREM products monitor
```
Để xóa key monitor khỏi tập products

- ZCARD: Để lấy toàn bộ key
```
ZCARD products
```
Để lấy toàn bộ products

- ZCOUNT: Để lấy toàn bộ key trong 1 khoảng
```
ZCOUNT products 0 60
```
Để lấy số lượng key của tập products có value trong khoảng từ 0 đến 60

- ZPOPMIN: Xóa key có value bé nhất
```
ZPOPMIN products
```

- ZPOPMAX: Xóa key có value lớn nhất
```
ZPOPMIN products
```

- ZINCRBY: Thêm 1 số lượng cho value trong 1 key
```
ZINCRBY products 15 keyboard
```
Nếu dùng số âm nó sẽ DECREASE
```
ZINCRBY products -25 keyboard
```

### ZRANGE
- `ZRANGE products 1 2 WITHSCORES`: Lấy phần tử từ số 1 đến số 2 trả cùng value
- `ZRANGE products 0 50 BYSCORES WITHSCORES`: Lấy phần tử có value từ 0 đến 50
- `ZRANGE products 1 2 REV`: Lấy phần tử từ 1 đến 2 ở chiều ngược lại (từ lớn đến bé, default của nó là từ bé đến lớn)
- `ZRANGE products LIMIT 1 5`: Bỏ qua một phần tử và lấy 5 phần tử ở phía sau  