# Github documentations for project

Step to step to work with git 🔥:

## 🚀 Lưu ý:

- Không làm việc tại các branch main, stable, development. Hãy tạo branch mới, làm việc tại đó.
- Cách đặt tên cho branch mới:
  - Theo định dạng `<type>_<name>`.
  - Với type là:
    - Feature: Chức năng mới.
    - Fix: Sửa lỗi.
    - Refactor: Sửa lại định dạng, tổ chức lại code.
    - Test: Kiểm, thử ...
    - ...
  - Và `name` là mô tả ngắn gọn cho mục tiêu
  - (Ví dụ: `Feature_Auth_with_github` để thêm chức năng đăng nhập với github)

## 🔥 Bắt đầu nhanh

**1. Lấy code từ github:**

- Clone git repository về máy bằng câu lệnh:
  `git clone <link-to-repo>`
- Có thể đặt lại tên bằng cách thêm tên phía sau:
  `git clone <link-to-repo> <name>`

**2. Làm việc với branch:**

- Kiểm tra branch hiện tại: `git branch`

  <p align="center"><img src="./images/git-branch.PNG" alt="description of image" width="350px"></p>

- Chuyển sang branch đã tồn tại: `git checkout <branch_name>`
- Chuyển sang branch chưa tồn tại, và tạo mới: `git checkout -b <new_branch_name>`
<p align="center">
  <img src="./images/checkout-b.PNG" alt="description of image" width="350px"></p>
- Để xóa branch, cần phải checkout sang branch khác sau đó: `git branch -d <branch_name>`

**3. Commit:**

- Sử dụng `git add <path-to-file>` để thêm các file muốn commit vào staged area. Bạn cũng có thể sử dụng git add . để thêm tất cả các thay đổi trong repository.
- Sử dụng `git status` để kiểm tra trạng thái của staged area và các file trong working directory.
- Sử dụng `git diff` để xem sự khác biệt giữa các file trong working directory và staged area.
- Khi đã staged các file, sử dụng `git commit -m "<commit_message>"` để commit các file. Lưu ý rằng commit message cần phải rõ ràng và mô tả đầy đủ các thay đổi trong commit.
- Nếu cần chỉnh sửa lại commit, sử dụng `git commit --amend`.
- Để xem lại lịch sử commit của repository, sử dụng `git log`.

**4. Push:**

- Sau khi đã commit các thay đổi, bạn có thể đẩy chúng lên repository trên server bằng lệnh `git push`.
- Lưu ý rằng trước khi push, bạn cần phải pull dữ liệu mới nhất từ server về bằng lệnh `git pull`.
- Để đẩy các thay đổi lên branch hiện tại, sử dụng lệnh `git push origin <branch_name>`. Nếu branch chưa được đẩy lên server trước đó, bạn có thể sử dụng lệnh `git push --set-upstream origin <branch_name>` để đẩy branch và thiết lập upstream cho lần đẩy tiếp theo.

**5. Tạo pull request:**

- Sau khi push thành công, truy cập vào repo trên github:
<p align="center">
  <img src="./images/new-branch.PNG" alt="description of image" width="400px"></p>
- Branch mới đã được push lên thành công, bấm vào branch vừa push, và chọn `Open Pull Request`:
<p align="center">
  <img src="./images/open-pull-request.PNG" alt="description of image" width="400px"></p>
- Chuyển sang `development`, không được merge vào `main` trừ khi là hot fix:
<p align="center">
  <img src="./images/change-to-dev-branch.PNG" alt="description of image" width="400px"></p>
- Điền tiltle và comment để mô tả mục đích của branch muốn merger, sau đó chọn `Create Pull Request`:
<p align="center">
  <img src="./images/create-pull-request.PNG" alt="description of image" width="400px"></p>

**6. Theo dõi Pull Request:**

- Nhớ theo dõi Pull Request để thảo luận về code của bạn ... 🔥
