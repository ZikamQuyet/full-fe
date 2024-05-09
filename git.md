#GIT

##Config

- xem config ở global
  git config --global --list
- Đầu tiên thì chúng ta cần config cho git biết chúng ta là ai khi mà đưa code lên
  git config --global user.name "Zika Nguyen"
  git config --global user.email zikanguyen@gmail.com
- Khởi tạo Repository trên máy tính
  git init
- Khu vực làm việc với Git
1. Khu vực làm việc: Chính là nơi chúng ta đang code, vẫn ở local
2. Khu vực staging: Sau khi dùng git add thì file sẽ được đưa lên khu vực này, vẫn ở trên local
3. Khu vực committed: Sau khi dùng git commit thì file từ staging sẽ được đưa lên đây, cũng vẫn ở trên local
4. Khu vực remote (gọi origin cũng được): Sau khi dùng git push sẽ file ở commited lên đây, bây giờ file của bạn đã đưa lên trên server

- Thêm file vào khu vực Staging với git add
  + thêm 1 file
    git add index.html
  + thêm tất cả các file thay đổi
    git add .
- Khôi phục những file ở khu vực Staging về khu vực code với git reset(ngược vs git add)
  + thêm 1 file
    git reset index.html
  + thêm tất cả các file thay đổi
    git reset .

- Clone Repository ở remote về
 git clone git@github.com:test/123.git

- Tạo branch mới
  + Câu lệnh này sẽ tạo một nhánh mới dựa trên nhánh hiện tại
    git branch TenNhanhMoi
  + câu lệnh dưới sẽ tạo một nhánh mới dựa trên nhánh hiện tại và chuyển sang nhánh mới luôn.
    git checkout -b TenNhanhMoi
    git switch -c TenNhanhMoi
- check list branch
  git branch
  + remote branch
    git branch -r
  + local và remote branch
    git branch -a
- đổi tên branch
  git branch -m TenMoi
- Chuyển branch
  git checkout tenNhanh or git switch TenNhanh
- Push một branch
  git push -u origin localBranch
  `git push -u origin HEAD`(k cần tên branch)
- Xóa branch
  git branch -D localBranchName
  xóa trên remote
  git push origin --delete remoteBranchName
- push code mà không cần origin
  git push -u origin feature
-