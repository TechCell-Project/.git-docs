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

## 🚀 Step to works:

* Nếu **chưa** có repo, `clone` repo từ github
* Đã có repo, xác định điều cần làm (feature, fix, ...)
* **Không** sử dụng các branch `main`, `stable`, `development` để chỉnh sửa, hãy tạo branch mới và làm việc trên branch mới đó
* Kiểm thử
* Commit khi hoàn thành, và push lên github
* Tạo **Pull Request** và nhờ người khác review code, đánh giá, kiểm thử.
* Chỉ tạo **Pull Request** để merge vào branch `development` hoặc branch khác các branch `main`, `stable`!

## 🔥 Bắt đầu nhanh

**1. Lấy code từ github:**

- Clone git repository về máy bằng câu lệnh:
  ```bash
  git clone <link-to-repo>
  ```
- Có thể đặt lại tên bằng cách thêm tên phía sau:
  ```bash
  git clone <link-to-repo> <name>
  ```

**2. Làm việc với branch:**

- Kiểm tra branch hiện tại: 
```bash
git branch
```

  <p align="center"><img src="./images/git-branch.PNG" alt="description of image" width="380px"></p>

- Chuyển sang branch đã tồn tại: `git checkout <branch_name>`
- Chuyển sang branch chưa tồn tại, và tạo mới: `git checkout -b <new_branch_name>`
  <p align="center">
    <img src="./images/checkout-b.PNG" alt="description of image" width="420px">
  </p>
- Để xóa branch, cần phải checkout sang branch khác sau đó: `git branch -d <branch_name>`

**3. Commit:**

- Để thêm các file muốn commit vào staged area. Bạn cũng có thể sử dụng git add . để thêm tất cả các thay đổi trong repository.
```bash 
  git add <path-to-file>
  #or
  git add .
``` 
- Để kiểm tra trạng thái của staged area và các file trong working directory, sử dụng:
```bash
git status
```
- Để xem sự khác biệt giữa các file trong working directory và staged area, sử dụng:
```bash
git diff
```
- Khi đã staged các file, để commit các file (Lưu ý rằng commit message cần phải rõ ràng và mô tả đầy đủ các thay đổi trong commit), sử dụng: 
```bash
git commit -m "<commit_message>"
```
- Nếu cần chỉnh sửa lại commit, sử dụng:
```bash
git commit --amend
```
- Để xem lại lịch sử commit của repository, sử dụng:
```bash
git log
```

**4. Push:**

- Sau khi đã commit các thay đổi, bạn có thể đẩy chúng lên repository trên server bằng lệnh:
```bash
git push
```
- Lưu ý rằng trước khi push, bạn cần phải pull dữ liệu mới nhất từ server về bằng lệnh:
```bash
git pull
```
- Để đẩy các thay đổi lên branch hiện tại, sử dụng lệnh:
```bash
git push origin <branch_name>
```
- Nếu branch chưa được đẩy lên server trước đó, để đẩy branch và thiết lập upstream cho lần đẩy tiếp theo bạn có thể sử dụng lệnh:
```bash
git push --set-upstream origin <branch_name>
```

**5. Tạo pull request:**

- Sau khi push thành công, truy cập vào repo trên github:
<p align="center">
  <img src="./images/new-branch.PNG" alt="description of image" width="500px"></p>
- Branch mới đã được push lên thành công, bấm vào branch vừa push, và chọn `Open Pull Request`:
<p align="center">
  <img src="./images/open-pull-request.PNG" alt="description of image" width="500px"></p>
- Chuyển sang `development`, không được merge vào `main` trừ khi là hot fix:
<p align="center">
  <img src="./images/change-to-dev-branch.PNG" alt="description of image" width="500px"></p>
- Điền tiltle và comment để mô tả mục đích của branch muốn merger, sau đó chọn `Create Pull Request`:
<p align="center">
  <img src="./images/create-pull-request.PNG" alt="description of image" width="500px"></p>

**6. Theo dõi Pull Request:**

- Nhớ theo dõi Pull Request để thảo luận về code của bạn ... 🔥
