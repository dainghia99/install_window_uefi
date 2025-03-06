# Phân vùng ổ cứng cài Windows chuẩn UEFI

## Các câu lệnh
Thực hiện tuần tự

Vào chế độ `Menu Boot` nhấn tổ hợp phím `shift + F10` để mở CMD

Gõ lệnh
``` bash
diskpart
```

Liệt kê danh sách ổ đĩa
``` bash
list disk
```

Gõ lệnh
``` bash
sel disk "so_hien_thi"
```

Làm sạch ổ đĩa
``` bash
clean
```
Chuyển sang định dạng GPT
``` bash
conv gpt
```
Tạo phân vùng EFI kích thước 512MB
``` bash
cre part efi size=512
```
Format phân vùng thành Fast32
``` bash
format fs=fat32 quick
```
Gán cho phân vùng là ổ Z
``` bash
assign letter z
```
Thực hiện các lệnh bên dưới theo thứ tự
``` bash
cre part pri
```

``` bash
format fs=ntfs quick label=Windows
```

``` bash
assign letter C
```

``` bash
exit
```

# Thoát CMD và tiến hành cài window









