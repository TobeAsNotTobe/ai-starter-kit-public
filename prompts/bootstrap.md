# Prompt: dựng môi trường

Dán khối dưới đây cho trợ lý AI. Thay `<KIT>` bằng đường dẫn tới kit (thư mục trên máy, hoặc URL repo ở một tag cố định). Nếu AI không đọc được kit, dán kèm nội dung `PRINCIPLES.md`, `WORKFLOW.md`, `prompts/discover.md`, `prompts/check.md` và các file trong `templates/` (hoặc `KIT.md` nếu bản phát hành có). Nếu AI không tự chạy được lệnh, thêm câu: "Bạn không chạy được lệnh: hãy soạn lệnh để tôi chạy, tôi sẽ dán kết quả lại." Xem `QUICKSTART.md`.

```text
Bạn sẽ dựng môi trường làm việc với AI cho tôi theo bộ kit ở <KIT>.

BƯỚC 1. ĐỌC VÀ TÌM HIỂU
- Đọc <KIT>/PRINCIPLES.md.
- Làm ĐẦY ĐỦ <KIT>/prompts/discover.md: tra tài liệu chính thức hoặc chạy lệnh để có
  bằng chứng cho từng câu, không trả lời theo trí nhớ. Cho tôi xem bảng kết quả.
  Các bước sau dựa vào bảng này; câu nào "chưa xác minh" thì chọn cách an toàn hơn.

BƯỚC 2. HỎI (mỗi lượt tối đa 5 câu, chỉ hỏi những gì chưa biết)
- Tôi muốn bạn trả lời bằng ngôn ngữ nào? Comment trong code viết bằng ngôn ngữ nào?
- Nơi làm việc có hướng dẫn hay chính sách AI sẵn có không? Nếu có, ở đâu?
  (Chỉ trỏ tới, không chép nội dung.)
- Có giới hạn nào không: dữ liệu không được đưa cho AI, công cụ hay kết nối không được bật,
  không được cài phần mềm?
- Những repo nào cần dựng hướng dẫn (đường dẫn)?
- Thói quen làm việc nào bạn nên luôn tuân theo?

BƯỚC 3. ĐỀ XUẤT
Đọc từng repo thật (README, file build, cấu hình test, CI) và chạy thử lệnh test nhanh
trước khi đề xuất. Liệt kê mọi file sẽ tạo hoặc sửa:
đường dẫn | mục đích | cách ghi (tạo mới / thay khối có sẵn / THÊM KHỐI VÀO CUỐI file có sẵn).
Bao gồm:
- Hướng dẫn cá nhân, dựa trên <KIT>/templates/personal.md, ở file cấp người dùng của tool.
- Với mỗi repo chưa có AGENTS.md: tạo AGENTS.md dựa trên <KIT>/templates/AGENTS.md.
- Với mỗi repo ĐÃ có AGENTS.md: đây là file dùng chung của nhóm. Nêu rõ điều đó và đưa
  hai phương án để tôi chọn:
  (a) thêm khối vào cuối AGENTS.md (cần nhóm đồng ý trước khi commit);
  (b) không sửa AGENTS.md; đặt phần bổ sung vào một file cục bộ không commit mà tool đọc
      được (thường chính là file trỏ ở dưới).
- Với mỗi repo: file trỏ cục bộ nếu tool không tự đọc AGENTS.md; các dòng .gitignore cho
  file trỏ, file riêng của tool, và file sinh ra khi chạy test (cache của ngôn ngữ) nếu
  repo chưa ignore.
- Nếu tạo file hướng dẫn cục bộ: kiểm tra theo bảng ở bước 1 rằng tool VẪN đọc AGENTS.md
  khi có file đó (một số tool thôi tự đọc AGENTS.md khi có file khác); nếu cần, đặt dòng
  import AGENTS.md ở đầu file cục bộ.
- Phần bổ sung không lặp lại điều đã có trong AGENTS.md hay hướng dẫn của nơi làm việc;
  chỉ ghi điều còn thiếu. Mỗi điều chỉ viết một lần.
- Với mỗi repo chưa có `plans/`: hỏi tôi có muốn dùng quy trình checkpoint không (<KIT>/WORKFLOW.md). Nếu có, tạo `plans/INDEX.md` và `plans/inbox/README.md` từ <KIT>/templates/plans/.
- Trong hướng dẫn cá nhân, thay `<KIT>` bằng đường dẫn thật tới kit trên máy này.
- Cấu hình kết nối công cụ, chỉ khi tôi đã xác nhận là được phép.
- Câu hỏi cần tôi trả lời trước khi ghi (ví dụ chọn (a) hay (b)).
Dừng lại, chờ tôi duyệt.

BƯỚC 4. GHI (chỉ sau khi tôi duyệt)
- Mọi nội dung bạn thêm phải nằm giữa hai dòng đánh dấu "starter-kit:begin" và
  "starter-kit:end", viết dưới dạng comment hợp với loại file. Nếu hai dòng đó đã có thì
  chỉ thay phần nằm giữa. Không sửa gì bên ngoài. Khối mới trong file có sẵn thì thêm vào cuối.
- Không ghi khóa, mật khẩu hay token vào bất kỳ đâu. Nếu cần, hướng dẫn tôi tự lưu vào
  kho khóa của hệ điều hành.
- Nếu không ghi được một file (tool chặn, thiếu quyền): không tìm cách lách. In ra
  đường dẫn và toàn bộ nội dung đã duyệt để tôi tự lưu, rồi làm tiếp các file khác.
- Không commit.
- Chạy lại toàn bộ bước 4 lần nữa phải cho ra kết quả y hệt.

BƯỚC 5. KIỂM TRA VÀ BÁO CÁO
- Làm theo <KIT>/prompts/check.md.
- Báo cáo: việc đã làm; việc bỏ qua (kèm lý do); việc tôi cần tự làm (kèm nội dung cần
  lưu nếu có); cách tôi tự xác minh ở một phiên mới.
- Liệt kê những chỗ kit chưa hợp với môi trường này, viết dưới dạng chung,
  KHÔNG nêu tên tổ chức, hệ thống hay dữ liệu nội bộ.
```
