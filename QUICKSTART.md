# Bắt đầu nhanh

Dùng file này khi áp dụng kit trên máy làm việc, nhất là máy do nơi làm việc cấp.

## 1. Trước khi dùng: kiểm tra với nơi làm việc

- [ ] Nơi làm việc cho phép dùng tài liệu bên ngoài này. Kit theo license CC BY-ND 4.0 (`LICENSE`): được dùng, kể cả trong công việc; không được phân phối bản đã sửa.
- [ ] Trợ lý AI bạn định dùng là trợ lý được nơi làm việc cho phép.
- [ ] Bạn biết dữ liệu nào được đưa cho AI và dữ liệu nào không (code, tài liệu, dữ liệu khách hàng, secret).
- [ ] Bạn được tạo file hướng dẫn cá nhân cho AI trên máy này, và được thêm `AGENTS.md`, `plans/` vào các repo bạn làm.
- [ ] Nếu nơi làm việc đã có hướng dẫn hay chính sách AI: biết nó nằm ở đâu, để bootstrap trỏ tới.

Chưa chắc mục nào thì hỏi người phụ trách trước. Kit không thay thế chính sách của nơi làm việc.

## 2. Đặt kit ở đâu

Chép kit vào **một thư mục cố định** trên máy và giữ nguyên chỗ đó. Hướng dẫn cá nhân và `AGENTS.md` sẽ trỏ tới `WORKFLOW.md` bằng đường dẫn này.

| Trợ lý AI của bạn | Đặt kit ở |
|---|---|
| Đọc được file bất kỳ trên máy | Một thư mục riêng, ví dụ `~/ai-starter-kit/` (Windows: `%USERPROFILE%\ai-starter-kit\`) |
| Chỉ đọc được file trong thư mục đang mở (workspace) | Bên trong workspace, ví dụ `<workspace>/.ai-starter-kit/`. Nếu workspace là một repo git: thêm dòng `.ai-starter-kit/` vào `.git/info/exclude` để kit không bị commit |

Trong mọi hướng dẫn, `<KIT>` là đường dẫn tới thư mục này.

## 3. Chọn cách chạy theo khả năng của trợ lý AI

**A. Trợ lý đọc được file và chạy được lệnh** (trợ lý dòng lệnh, hoặc trợ lý trong IDE có quyền chạy lệnh):

1. Đặt kit như mục 2.
2. Mở trợ lý trong thư mục làm việc, dán khối prompt trong `prompts/bootstrap.md` (thay `<KIT>` bằng đường dẫn thật).
3. Trả lời câu hỏi, duyệt danh sách file, để trợ lý ghi.
4. Mở một phiên mới và chạy `prompts/check.md`.

**B. Trợ lý chỉ chat, nhưng đọc được file trong workspace:**

1. Đặt kit bên trong workspace (mục 2).
2. Dán khối prompt trong `prompts/bootstrap.md`, kèm câu: "Bạn không chạy được lệnh: hãy soạn lệnh để tôi chạy, tôi sẽ dán kết quả lại."
3. File nào trợ lý không tự ghi được, nó sẽ in nội dung; bạn tự lưu đúng đường dẫn nó chỉ.
4. Khi làm theo checkpoint: xem `WORKFLOW.md`, mục 10.

**C. Trợ lý không đọc được file, không vào được internet:**

1. Dán toàn bộ `KIT.md` (bản gộp của kit, nếu có trong bản phát hành) hoặc lần lượt nội dung `PRINCIPLES.md`, `WORKFLOW.md`, `prompts/discover.md`, `prompts/check.md` và các file trong `templates/` vào chat.
2. Dán khối prompt trong `prompts/bootstrap.md`, kèm câu như ở B.
3. Tự lưu các file trợ lý soạn ra; tự chạy các lệnh nó đề xuất và dán kết quả lại.

## 4. Sau khi dựng xong

- Mở một phiên mới trong một repo, hỏi: "Không dùng công cụ nào, không đọc file; chỉ dựa vào ngữ cảnh lúc bắt đầu phiên, liệt kê các tiêu đề mục của hướng dẫn repo." Trợ lý liệt kê đúng các mục của `AGENTS.md` là đạt.
- Việc lớn: lập kế hoạch trong `plans/` theo `WORKFLOW.md`, rồi giao từng checkpoint bằng câu "làm checkpoint tiếp theo".
