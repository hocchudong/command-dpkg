command-dpkg
============
## Giới thiệu về dpkg
  DPKG là chương trình chính quản lí gói trong Debian. Nó sử dụng để  install, build, remove, và manage các gói. Aptitude là front-end chính cho dpkg.
  
  Dưới đây một số lệnh dpkg thường được sử dụng.

#### 1. Cài đặt gói
  Để cài đặt một gói ".deb", sử dụng lệnh với tùy chọn "-i". Ví dụ để cài đặt một gói ".deb" như "mysql-server-wsrep-5.5.28-23.7-amd64.deb" sử dụng lệnh sau đây.
  
    dpkg -i mysql-server-wsrep-5.5.28-23.7-amd64.deb
	
  ![img](http://i.imgur.com/Dn1KRGz.png "img")
  
#### 2. Hiển thị các gói đã cài đặt
  Để xem danh sách các gói đã được cài đặt, sử dụng tùy chọn "-l" vói câu lệnh.
  
    dpkg -l
	
  ![img](http://i.imgur.com/aFZ0TGx.png "img")
  
  Để xem một gói phần mềm cụ thể đã được cài đặt hay chưa sử dụng tùy chọn "-l" và tên gói, ví dụ kiểm tra xem gói "mysql-server-wsrep", Thực hiện lệnh:
  
    dpkl -l mysql-server-wsrep
	
  ![img](http://i.imgur.com/9qop5ZM.png "img")
  
#### 3. Remove gói
  Để Remove gói ".deb" ta phải xác định tên gói là "mysql-server-wsrep" không phải tên gốc "mysql-server-wsrep-5.5.28-23.7-amd64.deb". Sử dụng tùy chọn "-r" để remove/uninstall gói.

    dpkg -r mysql-server-wsrep
	
  ![img](http://i.imgur.com/VD7ost5.png "img")
  
 Có thể sử dụng "-p" thay cho "-r" thì nó sẽ loại bỏ các gói cùng với các file cấu hình, với "-r" dpkg sẽ chỉ bỏ các fois mà không xóa phần file cấu hình.
 
    dpkg -p mysql-server-wsrep 
	
#### 4. Xem nội dung của một gói
  Để xem nội dụng của một gói phần mềm, dùng tùy chọn "-c" để show. Câu lệnh này sẽ hiển thị nội dung của một gói ".deb" theo dạng danh sách.

    dpkg -c mysql-server-wsrep-5.5.28-23.7-amd64.deb
	
  ![img](http://i.imgur.com/k7pjSNs.png "img")
  
#### 5. Kiểm tra một gói đã được cài đặt hay chưa
  Sử dụng tùy chọn "-s" và tên gói để xem gói ".deb" đã được cài đặt chưa.
  
    dpkg -s mysql-server-wsrep
	
  ![img](http://i.imgur.com/LgxLtMW.png "img")
 
#### 6. Kiểm tra vị trí của gói đã được cài đặt
  Hiển thị vị trí các file trong hệ thống của gói đã cài đặt theo tên của gói. Dùng lệnh với tùy chọn "-L"
  
    dpkg -L mysql-server-wsrep
	
  ![img](http://i.imgur.com/recW5sZ.png "img")
  
#### 7. Cài đặt tất các các gói trong một thư mục
  Cài đặt tất cả các gói phù hợp với định dạng "*.deb" được tìm thấy trong một thư mục hoặc các thư mục con. Sử dụng tùy chọn "-R" và "--install".

    dpkg -R --install testdeb/
	
  Hoặc cũng có thể làm theo cách khác. Lưu hết các gói dạng ".deb" vào một thư mục, cd vào thư mục và chạy lệnh.
  
    dpkg -i *.deb
	
#### 8. Giải nén các gói mà không cấu hình
  Sử dụng "-unpack" để giải nén gói nhưng không cài đặt hay cấu hình gói.

    dpkg --unpack mysql-server-wsrep-5.5.28-23.7-amd64.deb
	
  ![img](http://i.imgur.com/krGYMGQ.png "img")
	
#### 9. Cấu hình lại một gói đã giải nén
  Dùng tùy chọn "-configure" để cấu hình lại một gói đã được giải nén
  
    dpkg --configure mysql-server-wsrep
	
#### 10. Thay thế thông tin của gói
  Dùng tùy chọn "--update-avail" thay thế các thông tin cũ với các thông tin có sãn trong tập tin gói.
  
    dpkg –-update-avail mysql-server-wsrep-5.5.28-23.7-amd64.deb
	
#### 11. Xóa bỏ thông tin có sẵn của gói
  Dùng "-clear-avaial" sẽ xóa những thông tin hiện tại sẵn có của các gói
  
    dpkg –-clear-avail
	
#### 12. Hiển thị thông tin phiên bản dpkg
  "--version" sẽ hiển thị thông tin phiên bản của dpkg
  
    dpkg --version
	
  ![img](http://i.imgur.com/DKYrHFR.png "img")
  
#### 13. Nhận các trợ giúp về dpkg
  "--help" sẽ hiển thị danh sách các tùy chọn của lệnh dpkg
  
    dpkg –-help
	
  ![img](http://i.imgur.com/dtXasco.png "img")
  
#### 14. Hiển thị Licence dpkg

    
#### 15. Forget Uninstalled and Unavailable Packages
