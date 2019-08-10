# 01
## Định nghĩa
- Là 1 NoSQL
- Lưu dạng key-value
- Lưu trên bộ nhớ tạm thời(Ram)
- open source 
- Remote dictionary Server (Redis)

## Công dụng
- Làm database
- Làm caching
- Làm message broker

## Các kiểu dữ liệu lưu
- Primative
  + String
- Containers (of string)
  + Hashes
  + Lists
  + Sets
  + Sorted Sets

Max của mấy cái Container này là 512 Mb

## Các lệnh thường dùng
`keys *`: In ra hết key có trong server

`set key_name value`: tạo key và set giá trị cho nó

`get key_name`: lấy key

`del key_name`: xóa key

**Lưu ý**: Nếu bạn đã set giá trị cho 1 key rồi sau đó bạn set thêm lần nữa thì giá trị mới sẽ ghi đè lên giá trị cũ okke?

`flush all`: để xóa hết key 

`clear`: để làm trống màn hình

`setex key_value time_to_live value`:set thời gian cho cái value trong key đấy sống

`ttl`: check xem còn sống được bao lâu

`setnx key_value value`: nếu chưa có nó sẽ tạo ra key rồi set còn nếu có rồi nó sẽ chỉ trả về 0 thôi và không ghi đè

`strlen key_name`: check độ dài của key

`mset key_name1 value1 key_name2 value2 ....`: set nhiều key 1 lúc

`psetex key_value time_to_live value`:set thời gian cho cái value trong key đấy sống theo milisecond 

`decr key_name`: giảm 1 đơn vị của value

`incr key_name`: tăng 1 đơn vị của value

`incryby key_name number`: tăng đơn vị của value theo number

`decryby key_name number`: giảm đơn vị của value theo number

4 lệnh trên dùng cho value số thôi nhé

`append key_name value`: thêm chữ vào key string






























