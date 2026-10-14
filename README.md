# Website tư vấn tuyển sinh cao học

Bản đầu tiên, giao diện tiếng Việt, tương thích máy tính và điện thoại. Chưa có thương hiệu hoặc dữ liệu tuyển sinh chính thức của một cơ sở đào tạo.

## Chạy ngay trên máy

Mở `index.html` bằng Chrome hoặc Edge. Không cần Node.js, cài thư viện hay khóa API. Tất cả CSS, JavaScript và dữ liệu mẫu đã có trong file này.

## Chức năng

- Điều hướng đến thông tin tuyển sinh, lộ trình, hồ sơ và hỏi đáp.
- Tìm kiếm câu hỏi thường gặp, có tìm tiếng Việt không dấu.
- Danh sách nhắc việc lưu trên trình duyệt, có thể bỏ đánh dấu.
- Cửa sổ chatbot: gửi câu hỏi, chọn gợi ý, đóng/mở, nhấn Escape để đóng.
- Chatbot hiện dùng khớp từ khóa với nội dung mẫu, **chưa phải AI**. Không xác nhận đủ điều kiện hay tạo thông tin tuyển sinh.
- Không gửi hội thoại hoặc thông tin đăng ký đến máy chủ. Không nhận hồ sơ tuyển sinh.

## Đưa mã lên GitHub

1. Tạo repository tên `tuyen-sinh-cao-hoc`. Nếu chỉ lưu mã và chưa muốn công khai, chọn Private.
2. Chọn Add file → Upload files, tải `index.html`, `README.md` và `.nojekyll` lên thư mục gốc; commit.
3. Chưa bật Pages nếu chưa quyết định công bố website.

## Khi bạn quyết định công bố bằng GitHub Pages

GitHub Pages thông thường tạo website công khai, kể cả khi mã nguồn nằm trong repository riêng tư. Repository riêng tư không đồng nghĩa với website riêng tư. Các khả năng Pages cho repository riêng tư và kiểm soát truy cập phụ thuộc gói tài khoản.

1. Vào Settings → Pages.
2. Source: Deploy from a branch.
3. Branch: main, thư mục: /(root); Save.
4. Chờ GitHub hoàn tất triển khai và dùng URL GitHub trả về, thường có dạng https://TEN_TAI_KHOAN.github.io/tuyen-sinh-cao-hoc/.

Tài liệu: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Chưa cấu hình tên miền `abc.com`; không có file CNAME. Tên miền đó chỉ là ví dụ trong yêu cầu.

## Cập nhật nội dung

Sửa tên đơn vị, các mục đang “Chờ cập nhật” và thông tin liên hệ trong `index.html`. Mảng `KNOWLEDGE` ở đầu đoạn script chứa câu hỏi, các từ khóa không dấu và câu trả lời. FAQ và chatbot cùng dùng mảng này. Khi đưa thông báo thật vào, bổ sung năm/đợt, nguồn và ngày cập nhật trong câu trả lời; tránh trộn thông tin giữa các đợt.

## Nâng cấp thành chatbot AI

GitHub Pages chỉ phục vụ phần giao diện tĩnh. Cần một API phía máy chủ riêng để tìm tài liệu và gọi Gemini hoặc nhà cung cấp AI khác. Không dán khóa API vào index.html, không đưa khóa lên repository. Phần này chưa được triển khai trong bản đầu tiên.

## Kiểm tra thủ công

- Mở file, kiểm tra menu trên điện thoại, liên kết các mục.
- Gõ “ngoai ngu” trong ô tìm FAQ.
- Đánh dấu các việc, tải lại trang, kiểm tra tiến độ nếu trình duyệt cho phép lưu.
- Hỏi “Học phí bao nhiêu?”, “Khi nào hết hạn nộp hồ sơ?”; câu trả lời phải nói chưa có dữ liệu chính thức.
- Gõ chuỗi `<img src=x onerror=alert(1)>`: phải hiển thị như văn bản, không thực thi.

Bản này sẵn sàng tải lên GitHub, nhưng chưa được đưa lên tài khoản hoặc xuất bản.
