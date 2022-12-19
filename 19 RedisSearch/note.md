## Redis search
Dùng để search các hash theo các key và giá trị trong nó

![image](https://user-images.githubusercontent.com/45547213/205902831-069f5898-6ee0-4652-9369-2d7f01d69fd4.png)

```
HSET cars#c1 name 'new car' color blue year 1970
```

- Tạo index: `FT.CREATE idx:cars ON HASH PREFIX 1 cars# SCHEMA name TEXT year NUMERIC color TAG`
- Search: `FT.SEARCH idx:cars '@name:(fast car)'`

![image](https://user-images.githubusercontent.com/45547213/205904275-d9813311-a9e6-4ec2-8d27-64c143b27a16.png)

Khi chọn kiểu dữ liệu chúng ta cần lưu ý
![image](https://user-images.githubusercontent.com/45547213/205904418-d2182040-8ca3-4b84-b33d-6256b710dfa6.png)

Khi search
![image](https://user-images.githubusercontent.com/45547213/205904745-cb21a59d-41c1-4928-be3a-705fbab452ce.png)

- Khi search với kiểu tag
![image](https://user-images.githubusercontent.com/45547213/205904935-ba10b039-2ce5-423f-989c-e3d9b46d0216.png)

- Khi search với kiểu text
![image](https://user-images.githubusercontent.com/45547213/205905164-71407207-6165-4fed-bcf4-5626fdc65c59.png)

- Fuzzy search dùng cho text search khi người dùng gõ không đúng hẳn keyword mà nó vẫn ra được. Khi đó chúng ta dùng cú pháp như này
![image](https://user-images.githubusercontent.com/45547213/205906086-9277698b-4148-4b47-906b-d0ec48a2aae6.png)

Nếu chúng ta có 2 dấu %%car%% thì nó sẽ chấp nhận kết quả sai lệch là 2 ví dụ nó searh là garr thì vẫn sẽ tìm ra kết quả là car

- Prefix search
![image](https://user-images.githubusercontent.com/45547213/205906481-19b2f45b-135d-45d8-a1ed-fc8c85149cca.png)
