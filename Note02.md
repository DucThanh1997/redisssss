# Các kiểu dữ liệu
## hash
### Định nghĩa
![image](https://user-images.githubusercontent.com/45547213/62828977-666cf180-bc1d-11e9-9a76-8513c0837b40.png)

giống như là dict ấy nó sẽ là như này
{"student1": {"age": 22, "name": "Thanh", "class": "12a1"}}

### 1 vài lệnh
- `hmset key_name value hash_name1 hash_value1 hash_name2 hash_value2 hash_name3 hash_value3`: set hash key

Ví dụ:
`hmset stu1 age 22 name Thanh class 12a1`

- `hget key_name field_name`: in ra giá trị của field trong hash

- `hgetall key_name field_name`: in ra hết

- `hexist key_name field_name`: kiểm tra xem có field đấy không

- `hdel key_name field_name`: xóa trường trong field 

- `hsetnx key_name field_name`: set field_name cho nó nếu nó chưa tồn tại nếu tồn tại rồi thì không thành công

- `hkeys key_name`: trả về hết field_name

- `hincryby key_name field_name` number: tăng field theo number

- `hvals key_name`: trả về hết value của field

- `hlen key_name`: trả về số lượng field_name

- `hmget key_name field_name`: trả về value của field_name theo key

## List
### Định nghĩa
![image](https://user-images.githubusercontent.com/45547213/62829177-0af13280-bc22-11e9-9867-cefffe09d92e.png)
Giống list bình thường nhé 

### 1 số lệnh

- `lpush key_name value`: đẩy từ bên trái vào key với 1 value

- `lrange key_name start stop`: xem các giá trị theo range từ start đến stop của key

- `lpop key_name`: xóa 1 phần tử từ bến trái

**rpush cũng như này**

- `llen key_name`: in ra số phần tử của list

- `lindex key_name index`: in ra value theo index

- `lset key_name index value`: set index bằng value 

- `lrange key_name 0 -1`: in ra hết

- `lpushx key_name value`: chỉ đẩy từ trái vào 1 value nếu key tồn tại

- `linsert key_name before/after value_exsit new_value`: đẩy vào 1 new_value trước hoặc sau 1 key đã tồn tại

## Set
### Định nghĩa
![image](https://user-images.githubusercontent.com/45547213/62829373-468dfb80-bc26-11e9-8ddd-de2b74648d93.png)
đặc điểm giống set bình thường 

### 1 vài lệnh

- `sadd set_name value`: add value vào set name

- `smember set_name`: trả về hết value

- `scard`: trả về số lượng value có trong key

- `sdiff set_name1 set_name2`: trả về các phần tử của set1 mà không có trong set2

- `sdiffstore set_name3 set_name1 set_name2`: lưu các phần tử của set1 mà không có trong set2 vào set3

- `sunion set_name1 set_name2`: gộp set1 và set2 lại vào thành set1 chỉ lấy unique thôi nhé

- `sunion set_name4 set_name1 set_name2`: gộp set1 và set2 lại vào thành set4 chỉ lấy unique thôi 

- `srem set_name value`: xóa 1 member có giá trị = value trong set_name

- `spop set_name 2`: xóa random 2 giá trị của set

- `sinter set_name1 set_name2`: lấy những phần tử giống nhau

- `sinterstore set_name3 set_name1 set_name2`: lấy những phần tử giống nhau rồi lưu vào set_name3

- `smove set_name1 set_name2 value`: lấy value chuyển từ 1 sang 2

## Sorted Set
### Định nghĩa
![image](https://user-images.githubusercontent.com/45547213/62829482-a8e7fb80-bc28-11e9-8220-21db8fb79b74.png)
đi cùng với value sẽ có score để sort cho cno
### 1 số lệnh
- `zadd set_name score value`: thêm vào

- `zrange set_name 0 -1: in ra hết

- `zcard set_name`: in ra số lượng

- `zcount set_name min_score max_score`: đếm xem trong khoảng score này có bao nhiêu phần tử 

- `zrem set_name member`: xóa phần tử theo value not score

- `zrank set_name member`: xem thứ tự của phần tử bắt đầu từ 0 

- `zrevrank set_name member`: xem thứ tự của phần tử theo hướng ngược lại 

- `zscore set_name member`: xem score nếu member không tồn tại nó sẽ random ra score

**Lưu ý**: Có thể có nhiều member có cùng score thì cái nào được định nghĩa score trước thì sẽ đứng đầu

- `zrangebyscore set_name start stop`: in ra member trong khoảng score nhất định






















