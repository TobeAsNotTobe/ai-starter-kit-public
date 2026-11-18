# Prompt: tự tìm hiểu tool

Dán khối dưới đây cho trợ lý AI. `prompts/bootstrap.md` tự gọi prompt này, nên thường không cần chạy riêng.

```text
Hãy tìm hiểu chính tool AI mà bạn đang chạy trong, trên máy này. Mỗi câu trả lời phải
có BẰNG CHỨNG: tài liệu chính thức (ghi đường dẫn; ưu tiên đúng phiên bản đang cài),
kết quả lệnh bạn đã chạy, hoặc file bạn đã thấy trên máy. Không trả lời theo trí nhớ.
Câu nào không có bằng chứng thì ghi "chưa xác minh" và nói vì sao (không có mạng, lệnh
bị chặn, không có tài liệu...). Không đoán.

1. Tên tool, phiên bản, hệ điều hành.
2. Hướng dẫn cấp người dùng: file nào, ở đâu, có tự đọc mỗi phiên không. Tool có cho
   ghi vào đó không, hay sẽ hỏi quyền / chặn?
3. Hướng dẫn cấp repo: tool đọc file nào? Có tự đọc AGENTS.md không, từ phiên bản nào,
   và trong điều kiện gì? Có đọc file ở thư mục cha hoặc thư mục con không?
4. Nối file: có cú pháp để một file hướng dẫn kéo theo file khác không (import, include)?
   Cách đơn giản nhất để tool đọc AGENTS.md là gì? Có file hướng dẫn cục bộ nào được đọc
   mà thường không commit không?
5. Kết nối công cụ (ví dụ MCP): cấu hình ở đâu, cấp người dùng hay cấp repo, định dạng gì.
6. Khóa và đăng nhập: tool lưu thông tin đăng nhập ở đâu; có dùng kho khóa của hệ điều
   hành không. Không đọc và không in giá trị bí mật.
7. Những file và thư mục mà tool tự tạo trong repo (để đưa vào .gitignore).
8. Cách kiểm tra: làm sao chứng minh rằng ở một phiên mới tool thực sự đã nạp một file
   hướng dẫn? Cách chuẩn dùng được với mọi tool: mở phiên mới trong repo, yêu cầu
   "không dùng công cụ nào, không đọc file; chỉ dựa vào ngữ cảnh lúc bắt đầu phiên, liệt kê
   các tiêu đề mục của hướng dẫn repo". Ghi thêm cách riêng của tool nếu có.

Trả lời bằng một bảng: câu hỏi | câu trả lời | bằng chứng. Không ghi file nào.
```
