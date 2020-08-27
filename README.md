Đây là các bước cơ bản thao tác với git

1. git init:
    Khi bắt đầu project thì cần sử dụng lệnh init để sử dụng git. nó sẽ tao ra file .git
    sử dụng lệnh ls .git để kiểm tra file.

2. git status:
    Kiểm tra trạng thái các file đã được committed chưa

3. git add <fileName>:
    Thêm 1 file vào committed

    Có thẻ sử dụng git "add ." để thêm tất cả

4. git commit:
    Đóng gói tất cả files đã được add vào committed và dán cho nó một mô tả
    Vd: git commit -m 'First commit'
    khi sử dụng lần đầu sẽ chưa sử dụng git commit được , nó yêu cầu phải config:
        *** Please tell me who you are.

        Run

        git config --global user.email "you@example.com"
        git config --global user.name "Your Name"

        to set your account's default identity.
        Omit --global to set the identity only in this repository.

        fatal: unable to auto-detect email address (got 'duyla@DESKTOP-LEH69C6.(none)')
5. git config:
    git config --global user .email duynd.nde17023@vtc.edu.vn
    git config --global user .name "Duy Elbi"

    Sau khi config thì sử dụng git commit để commit lại . khi này console hiển thị:
        [master (root-commit) 33d0be5] First commit
        3 files changed, 32 insertions(+)
        create mode 100644 README.md
        create mode 100644 haha.html
        create mode 100644 index.html

6. git log:
    Xem lại lịch sử các commit
        commit 33d0be56c141d8e305d6d6fbab0808f0e71f2cdb (HEAD -> master)
        Author: Duy Elbi <duynd.nde17023@vtc.edu.vn>
        Date:   Thu Aug 27 19:13:58 2020 +0700

        First commit


        nhấn Q để thoát ra
7. git show <commitId>:
    Hiển thị chi tiết 1 commit theo ví dụ:
    git show 33d0be56c141d8e305d6d6fbab0808f0e71f2cd

8. git diff:
    Xem thay đổi của các file có modified

    Sau đó có thể sử dụng git add . và git commit để commit thay đổi

9. Các thuật ngữ Working dir, Staging area, Respository:
    a. Working dir:
        Thư mục đang làm việc
    b. Staging area:
        Khi đã commit rồi mà thay đổi chỉnh sửa các file thì sẽ được add vào Staging area //chính là modified
    c. Respository:
        Lưu các thay đổi của các commit

        muốn xem sử dụng git log

        mẹo: sử dụng gitk để mởi giao diên người dùng

10. check out -- <fileName>
    Xóa bỏ các thay đổi chưa được commit của file

11. git restore --staged <fileName>:
    Unstage file đac được add vào Staging area

12. Branching:
    Kỹ thuật tạo nhánh mới trong git
    a. git branch:
        Xem nhánh hiện tại
    b. git checkout -b <branchName>:
        tạo một branch mới và chuyển sang branch đó
    c. git checkout <branchName>:
        chuyển sang branch khác đã được tạo
13. Merging:
    Kỹ thuật ghép nhánh
    a. git merge <branchName>:
        Ghép các commit của branch khác vào branch hiện tại.
    b. git branch -D <branchName>:
        Sau khi đã merge thì có thể xóa branch đó đi

14. .gitignore:
    từ chối commit những file không cần thiết
    vd: node_modules // chiếm rất nhiều bộ nhớ, làm nặng dự án
    tạo file .gitignore

15. chalk:
    giúp terminal có nhiều màu sắc hơn
    npm install chalk --save

16. github:
    b1: Vào trang github tạo mới project
    b3: copy link project
    b2: git remote add origin https://github.com/duyelbi/testGit.git
        git remote -v //kiểm tra
    b3: git push
        nếu không thành công thì sử dụng "git push -u origin master" sau đó đăng nhập vào github