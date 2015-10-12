# He-thong-tap-tin-trong-linux
Hệ thống tập tin trong Linux


#1. Cấu trúc hệ thống tập tin

- Mỗi hệ điều hành có cách tổ chức lưu trữ dữ liệu riêng, ở mức vật lý, đĩa được định dagnj từ các thành phần sector, track, cylinder. Ở mức logic, mỗi hệ thống sử dụng cấu trúc riêng, có thể dùng chỉ mục hay phân cấp để xác định được dữ liệu từ logic tới mức vật lý. Cách tổ chức nhuwvaayj gọi là hệ thống tập tin (file system).
- Chẳng hạn như Windows sử dụng hệ thống tập tin FAT16, FAT32, NTFS.
- Hệ thống tập tin là một phần cơ bản của hệ điều hành Linux
- Một hệ thống tập tin là thiết bị mà nó đã được định dạng để lưu trữ tập tin và thư mục.
- Hệ thống tập tin Linux bao gồm: đĩa mềm, CD_ROM, những partition của đĩa cứng. Những hệ thống tập tin thường được tạo trong quá trình cài đặt hệ điều hành nhưng bạn cũng có thể thay đổi cấu trúc hệ thống tập tin khi thêm thiết bị hay chỉnh sửa những partition đã tồn tại
- Linux hỗ trợ rất nhiều loại hệ thống tập tin như: ext2, ext3, ext4, proc..... Hệ thống tập tin cơ bản của Linux là ext2, ext3, ext4. Proc là hệ thống ttapaj tin ảo (/proc) nghĩa là không dành dung lượng đĩa phân phối cho nó.
- Các thành phần của hệ thống tập tin:
<ul>
<li>Superblock: là một cấu trúc được tạo ra tại vị trí bắt đầu hệ thống tập tin. Nó lưu trữ thông tin về hệ thống tập tin như: thông tin về block-size, free block. thời gian mount cuối cùng của tập tin.</li>
<li>Inode: Lưu những thông tin về những tập tin và thư mục được tạo ra trong hệ thống tập tin. Nhưng nó không lưu tên tập tin và thư mục. Mỗi tập tin tạo ra sẽ được phân bổ một inode lưu thoogn tin sau: Loại tập tin và quyền hạn truy cập tập tin, người sở hữu tập tin, kích thước của tập tin và số hard link đến tập tin, ngày và thời gian chỉnh sửa tập tn lần cuối cùng, vị trí lưu nội dung tập tin trong hệ thống tập tin.</li>
<li>Storageblock: là vùng lưu dữ liệu thực sự của tập tin và thư mục. Nó chia thành những Data block. Dữ liệu lưu trữ vào địa chỉ trong các data block. Mỗi block thường chứa 1024 byte. Ngày khi tập tin chỉ có 1 ký tự thì cũng phải cấp phát một block để lưu nó. Không có ký tự kết thúc tập tin.Data block của tập tin thông thường lưu inode của tập tin và nội dung tập tin, Data block của thư mục lưu danh sách những entry bao gồm inode number, tên của tập tin và những thư mục con.</li>

</ul>

#2. Cấu trúc cây thư mục

#3. Mount và Unmount một hệ thống tập tin

#4. Liên kết tập tin

#5. Thao tác trên hệ thống tập tin và thiết bị

