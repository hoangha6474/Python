#### Nguyên tắc:
- Luôn có một kho lữu trữ trung tâm
- Có thể lấy dữ liệu về và thực hiện được các công việc chỉnh sửa, cập nhật dữ liệu lên kho trung tâm
- công cụ giải quyết các xung đột
## Các câu lệnh cơ bản
- Lệnh kiểm tra version:
```git
git --version
```
- Cd : change direction 
```git
cd .. # quay lại direction trước
```

```git
	dir # hiểm thị hết thư mục
```

![[image 1.png]]

![[Pasted image 20260623090313.png]]

- Cách tạo repository mới

![[Pasted image 20260623221002.png]]

![[Pasted image 20260623221442.png]]

![[Pasted image 20260623221958.png]]

![[Pasted image 20260623222759.png]]

![[Pasted image 20260624150647.png]]


Cấu hình `gitignore` chỉ đinh tệp/ thư mục không nên theo dõi bởi git ( bỏ qua )

![[Pasted image 20260625191407.png]]

- Tương tác với Remote Repository
![[Pasted image 20260626101915.png]]

- Xử lý xung đột trog git:
 **Trình tự gây xung đột:** Cả hai lập trình viên cùng `pull` một phiên bản tệp `a.txt` về máy local. Cả hai cùng chỉnh sửa nội dung tệp này. Người thứ nhất `push` thành công lên Central Repo, nhưng khi người thứ hai cố gắng `push`, hệ thống sẽ báo lỗi vì phiên bản ở local của họ đã cũ hơn so với trên server
 ![[Pasted image 20260627212746.png]]
***
Syntax:
```git
git checkout <commit_hash>
```

![[Pasted image 20260627220945.png]]