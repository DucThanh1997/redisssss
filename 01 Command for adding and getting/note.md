## Set
![image](https://user-images.githubusercontent.com/45547213/202900895-7f03093f-6eb4-4ca2-a028-69c265e622e7.png)

- Khi thêm option GET vào câu lệnh set như sau `SET message 'hello 2' GET` thì giá trị trả về sẽ là giá trị của `message` trước khi chạy lệnh SET
![image](https://user-images.githubusercontent.com/45547213/202900959-91409cd4-c1fe-4ade-9975-cd515bd0943d.png)

- Khi thêm option `XX` thì key sẽ chỉ được set nếu nó đã tồn tại 
- Ngược lại NX chỉ set nếu không tồn tại key trong database
- EX là setup time tính bằng second để key tự xóa
- PX là setup time tính bằng millisecond
- EXAT/PXAT là setup time tính theo date rõ ràng vào giờ này ngày này thì xóa kiểu như thế (theo timestamp hoặc theo date)
- SETEX và SETNX giống với SET cùng các option của nó
- MSET để set nhiều key một lúc ví dụ `MSET color red model toyota`. Tức là set color là red và model là toyota

## GET
- Del để xóa key


## design consideration
- What type of data are we storing
- Should we be concerned about the size of the data
- Do we need to expire about the data
- What will be the key naming for this data
- Any business logic concern

## Key naming
- Keys should be unique
- De hieu
- Should use `:` to seperate differents parts of key