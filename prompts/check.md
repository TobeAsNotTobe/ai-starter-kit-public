# Prompt: kiểm tra môi trường

Dán khối dưới đây cho trợ lý AI. Prompt này chỉ đọc, không sửa gì.

```text
Kiểm tra môi trường làm việc với AI trên máy này. Không sửa file nào, không tạo file
(kể cả cache khi chạy test, nếu tránh được); chỉ báo cáo.

1. Hướng dẫn cá nhân: file cấp người dùng có tồn tại không, có khối
   "starter-kit:begin" ... "starter-kit:end" không, còn chỗ trống "<...>" chưa điền không.
   Nếu tôi đã tự lưu nội dung (vì tool không cho AI ghi) thì kiểm tra như bình thường.
2. Với mỗi repo tôi chỉ ra (hoặc repo hiện tại):
   - Có AGENTS.md không? Lệnh build và test trong đó còn chạy được không, chạy từ thư mục
     nào? Chỉ chạy lệnh nhanh; hỏi tôi trước khi chạy lệnh tốn hơn vài phút.
     Test có kiểm tra thật không, hay chỉ là lệnh giả (ví dụ chỉ in "ok")?
   - Tool có thực sự đọc AGENTS.md không (tự đọc, hoặc qua file trỏ)? Nếu bạn không tự mở
     được phiên mới, đưa tôi câu lệnh hoặc câu hỏi để tôi tự kiểm ở một phiên mới.
   - File trỏ và file riêng của tool có bị commit không? Dùng "git -C <repo> ls-files"
     và "git -C <repo> status --short". Có nằm trong .gitignore không?
   - AGENTS.md có thay đổi chưa commit trên file dùng chung của nhóm không? Nếu có, nhắc tôi.
3. Có khóa, mật khẩu hay token nằm trong file hướng dẫn hay file cấu hình nào không?
   Chỉ báo đường dẫn, không in giá trị ra.
4. Kết nối công cụ đang bật có khớp với những gì được phép không?
5. Tool có phiên bản mới làm thay đổi cách đọc hướng dẫn không? Nếu nghi ngờ, chạy lại
   prompts/discover.md.

Kết quả: một bảng mục | đạt / không đạt / chưa xác minh | ghi chú | đề xuất sửa.
```
