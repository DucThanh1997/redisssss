# Hash
- Dùng để lưu json

Lệnh set
```
hset company name 'nautilus' year 2
```

Lệnh get 1 value của 1 key của hash
```
hget company name
```

Lệnh get toàn bộ key của hash
```
hgetall company name
```

Lệnh kiểm tra xem key có tồn tại không. Trả về 1 nếu tồn tại, trả về 0 nếu không tồn tại
```
hexist company name
```

Lệnh xóa key
```
del company
```

