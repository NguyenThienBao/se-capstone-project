# Database Design

## 1 - Database Diagram

![database diagram](../img/db-diagram.jpg)

## 2 - Database Specification

### 2.1 - List of Tables.

| No     | Table Name     | Description                          |
| :----: | :------------: | :----------------------------------: |
| 1      | loaitaikhoan   | Thông tin phân quyền của tài khoản   |
| 2      | taikhoan       | Thông tin tài khoản                  |
| 3      | hangsanxuat    | Thông tin hãng sản xuất              |
| 4      | loaisanpham    | Thông tin danh mục sản phẩm          |
| 5      | sanpham        | Thông tin sản phẩm                   |
| 6      | tinhtrang      | Thông tin tình trạng của đơn đặt     |
| 7      | dondathang     | Thông tin chi tiết đơn đặt hàng      |

### 2.1 - Tables structure.

2.2.1 - Table: ***loaitaikhoan***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | maloaitaikhoan      | int            | PK          | mã loại tài khoản                    |
| 2      | tenloaitaikhoan     | varchar(45)    |             | tên của tài khoản                    |

2.2.2 - Table: ***taikhoan***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | mataikhoan          | int            | PK          | Mã tài khoản                         |
| 2      | tendangnhap         | varchar(20)    |             | Tên đăng nhập                        |
| 3      | matkhau             | varchar(20)    |             | Mật khẩu                             |
| 4      | tenhienthi          | varchar(64)    |             | Tên hiện thị                         |
| 5      | diachi              | varchar(256)   |             | Địa chỉ                              |
| 6      | dienthoai           | varchar(11)    |             | Số điện thoại                        |
| 7      | email               | varchar(30)    |             | email                                |
| 8      | bixoa               | bool           |             | Trạng thái bị xoá                    |
| 9      | maloaitaikhoan      | int            | FK          | Mã loại tài khoản                    |

2.2.3 - Table: ***hangsanxuat***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | mahangsanxuat       | int            | PK          | Mã hãng sản xuất                     |
| 2      | tenhangsanxuat      | varchar(45)    |             | Tên hãng sản xyất                    |
| 3      | logourl             | varchar(45)    |             | URL của  url                         |
| 4      | bixoa               | bool           |             | Trạng thái bị xoá                    |

2.2.4 - Table: ***loaisanpham***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | maloaisanpham       | int            | PK          | Mã loại sản phẩm                     |
| 2      | tenloaisanpham      | varchar(64)    |             | Tên loại sản phẩm                    |
| 3      | bixoa               | bool           |             | Trạng thái bị xoá                    |
2.2.5 - Table: ***sanpham***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | masanpham           | int            | PK          | Mã sản phẩm                          |
| 2      | tensanpham          | varchar(45)    |             | Tên sản phẩm                         |
| 3      | hinhurl             | varchar(45)    |             | URL của hình                         |
| 4      | giasanpham          | int            |             | Giá sản phẩm                         |
| 5      | ngaynhap            | datetime       |             | Ngày nhập                            |
| 6      | soluongton          | int            |             | Số lượng tồn kho                     |
| 7      | soluongban          | int            |             | Số lượng bán                         |
| 8      | soluongxem          | int            |             | Số lượng xem                         |
| 9      | mota                | text           |             | Mô tả                                |
| 10     | bixoa               | bool           |             | Trạng thái bị xoá                    |
| 11     | maloaisanpham       | int            | FK          | Mã loại sản phẩm                     |
| 12     | mahangsanxuat       | int            | FK          | Mã loại sản xuất                     |

2.2.6 - Table: ***tinhtrang***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | matinhtrang         | int            | PK          | Mã tình trạng                        |
| 2      | tentinhtrang        | varchar(45)    |             | Tên tình trạng                       |

2.2.7 - Table: ***dondathang***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | madondathang        | varchar(9)     | PK          | Mã đơn đặt hàng                      |
| 2      | ngaylap             | datetime       |             | Ngày lập                             |
| 3      | tongthanhtien       | int            |             | Tổng thành tiền                      |
| 4      | mataikhoan          | int            | FK          | Mã tài khoản                         |
| 5      | matinhtrang         | int            | FK          | Mã tình trạng                        |

2.2.8 - Table: ***chitietdondathang***

| No     | Field Name          | Data type      | Key (PK/FK) | Description                          |
| :----: | :------------:      | :------------: | :---------: | :----------------------------------: |
| 1      | machitietdondathang | varchar(11)    | PK          | Mã chi tiết đơn đặt hàng             |
| 2      | soluong             | int            |             | Số lượng                             |
| 3      | giaban              | int            |             | Giá bán                              |
| 4      | madondathang        | varchar(9)     | FK          | Mã đơn đặt hàng                      |
| 5      | masanpham           | int            | FK          | Mã sản phẩm                          |
