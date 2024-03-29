# git.md

## 1.git là gì?
Git là một hệ thống quản lý phiên bản phân tán (DVCS - Distributed Version Control System) được phát triển bởi Linus Torvalds vào năm 2005. Được thiết kế để quản lý mã nguồn của dự án phần mềm, Git đã trở thành một trong những công cụ phổ biến nhất trong cộng đồng phát triển phần mềm.

## 2. Kiến trúc của Git bao gồm các thành phần chính sau đây:

### Repository (Kho lưu trữ):
Repository là nơi lưu trữ toàn bộ lịch sử thay đổi của dự án, bao gồm mã nguồn, các phiên bản và thông tin liên quan khác.
Có hai loại repository: Local Repository (Kho lưu trữ cục bộ) và Remote Repository (Kho lưu trữ từ xa).

### Working Directory (Thư mục làm việc):
Working Directory là thư mục trên máy tính của bạn nơi bạn làm việc và chỉnh sửa các tệp trong dự án.
Git theo dõi tất cả các thay đổi bạn thực hiện trong thư mục này.

### Index (Staging Area hoặc Cache):
Index là một vùng trung gian giữa Working Directory và Repository.
Trước khi commit, bạn cần thêm các thay đổi mong muốn từ Working Directory vào Index bằng lệnh git add.

### Commit (Ghi nhận):
Commit là hành động lưu trữ một bản sao của tất cả các thay đổi đã được thêm vào Index vào Repository.
Mỗi commit được gắn với một thông điệp mô tả nội dung thay đổi.

### Branch (Nhánh):
Branch là một phiên bản song song của Repository, cho phép phát triển đồng thời nhiều tính năng hoặc sửa lỗi mà không ảnh hưởng đến nhau.
Một repository có thể chứa nhiều nhánh khác nhau.

### Merge (Gộp nhánh):
Merge là quá trình kết hợp các thay đổi từ một nhánh vào nhánh khác.
Khi bạn hoàn thành một tính năng hoặc sửa lỗi trên một nhánh, bạn có thể gộp các thay đổi đó vào nhánh chính hoặc nhánh khác.

### Remote Repository (Kho lưu trữ từ xa):
Remote Repository là phiên bản của Repository được lưu trữ trên máy chủ từ xa như GitHub, GitLab, hoặc Bitbucket.
Bạn có thể push (đẩy) các thay đổi từ Local Repository lên Remote Repository và pull (kéo) các thay đổi từ Remote Repository về Local Repository.

### Clone (Sao chép):
Clone là hành động sao chép một Remote Repository vào Local Repository.
Khi bạn clone một repository, bạn tạo ra một bản sao hoàn chỉnh của toàn bộ lịch sử và mã nguồn của dự án.

Kiến trúc này giúp Git hoạt động một cách linh hoạt và hiệu quả, cho phép các nhóm phát triển làm việc một cách song song, quản lý và theo dõi các thay đổi trong dự án phần mềm một cách hiệu quả.


## 3. Thuật ngữ quan trọng trong Git và quản lý phiên bản phần mềm:
Commit: Hành động ghi nhận các thay đổi vào repository.

Repository: Nơi lưu trữ toàn bộ lịch sử thay đổi của dự án.

Branch: Phiên bản song song của repository, cho phép phát triển tính năng hoặc sửa lỗi mà không ảnh hưởng đến nhánh chính.

Merge: Quá trình kết hợp các thay đổi từ một nhánh vào nhánh khác.

Push: Hành động đẩy các thay đổi từ Local Repository lên Remote Repository.

Pull: Hành động kéo các thay đổi từ Remote Repository về Local Repository.

Clone: Hành động sao chép một Remote Repository vào Local Repository.

Fork: Tạo một bản sao của một repository public trên GitHub vào tài khoản của bạn.

Pull Request: Yêu cầu để gộp các thay đổi từ một nhánh vào nhánh khác trên GitHub.

Merge Conflict: Xung đột xảy ra khi hai nhánh có sự thay đổi mà không thể tự động gộp lại.

Checkout: Chuyển đổi giữa các nhánh hoặc khôi phục các thay đổi từ một commit cụ thể.

Stash: Tạm thời lưu trữ các thay đổi chưa commit để có thể làm việc trên một nhánh khác.

Tag: Đánh dấu một điểm cụ thể trong lịch sử của repository, thường được sử dụng để đánh dấu phiên bản phát hành.

Remote: Repository từ xa, thường là một dịch vụ như GitHub, GitLab, hoặc Bitbucket.

Working Directory: Thư mục trên máy tính của bạn nơi bạn thực hiện các thay đổi và làm việc trên dự án.

## 4. Các lệnh cơ bản trong Git:
git init: Khởi tạo một repository Git mới trong thư mục hiện tại.

git clone <URL>: Sao chép (clone) một repository từ URL đã cho vào thư mục hiện tại.

git add <file>: Thêm một file hoặc thay đổi vào Index (Staging Area) để chuẩn bị cho commit.

git commit -m "<message>": Ghi nhận (commit) các thay đổi đã được thêm vào Index với một thông điệp mô tả.

git status: Hiển thị trạng thái của các file trong thư mục làm việc và các file đã thêm vào Index.

git pull: Kéo (pull) các thay đổi từ Remote Repository về Local Repository và tự động thực hiện merge.

git push: Đẩy (push) các thay đổi từ Local Repository lên Remote Repository.

git branch: Liệt kê tất cả các nhánh trong repository và chỉ ra nhánh hiện tại.

git checkout <branch>: Chuyển đổi sang một nhánh khác.

git merge <branch>: Gộp (merge) các thay đổi từ một nhánh vào nhánh hiện tại.

git log: Hiển thị lịch sử các commit trong repository.

git diff: Hiển thị các thay đổi chưa staged (chưa thêm vào Index).

git remote add <name> <URL>: Thêm một Remote Repository với tên được chỉ định và URL đã cho.

git remote -v: Liệt kê tất cả các Remote Repository đã được cấu hình và URL tương ứng.

git fetch: Kéo về (fetch) tất cả các thay đổi từ Remote Repository mà không thực hiện merge.






