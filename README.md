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