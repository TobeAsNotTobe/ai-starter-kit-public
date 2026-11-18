# ai-starter-kit

Một bộ prompt và mẫu nhỏ để **chính AI bạn đang dùng** dựng môi trường làm việc cho bạn: hướng dẫn cá nhân, hướng dẫn cho từng repo, và một cách làm việc theo bước giữa người và AI.

- **Dùng được với các trợ lý lập trình AI** đọc được file và chạy được lệnh. Kit không chứa chi tiết riêng của tool nào: AI tự tìm hiểu chính nó (`prompts/discover.md`).
- **Làm bằng tay, có kiểm soát.** AI đề xuất, bạn duyệt, rồi AI mới ghi. Kit không chứa script tự động hóa.
- **Không chứa thông tin của tổ chức nào.** Những gì riêng của nơi bạn làm việc thì nằm ở nơi đó.

## Nội dung

| File | Dùng khi |
|---|---|
| [`QUICKSTART.md`](QUICKSTART.md) | Bắt đầu ở đây: kiểm tra với nơi làm việc, đặt kit ở đâu, chạy thế nào tùy khả năng của trợ lý AI |
| [`PRINCIPLES.md`](PRINCIPLES.md) | Đọc một lần để hiểu kit dựng cái gì và vì sao |
| [`WORKFLOW.md`](WORKFLOW.md) | Quy trình làm việc theo checkpoint giữa người và AI, kể cả quy trình cho một phiên AI tự làm checkpoint tiếp theo và cách làm khi AI chỉ chat được |
| [`prompts/bootstrap.md`](prompts/bootstrap.md) | Lần đầu dựng môi trường trên một máy, hoặc khi muốn dựng lại |
| [`prompts/discover.md`](prompts/discover.md) | AI tự tìm hiểu cách tool của nó đọc hướng dẫn và cấu hình (bootstrap tự gọi) |
| [`prompts/check.md`](prompts/check.md) | Kiểm tra lại môi trường: sau khi đổi tool, đổi máy, hoặc thấy AI làm sai hướng dẫn |
| [`templates/AGENTS.md`](templates/AGENTS.md) | Mẫu hướng dẫn cho một repo |
| [`templates/personal.md`](templates/personal.md) | Mẫu hướng dẫn cá nhân, áp dụng cho mọi repo |
| [`templates/plans/`](templates/plans/) | Mẫu `plans/INDEX.md`, một kế hoạch, và `plans/inbox/README.md` |

## Cách dùng

1. Đọc `QUICKSTART.md`: kiểm tra với nơi làm việc, chép kit vào một thư mục cố định trên máy.
2. Mở trợ lý AI, dán khối prompt trong `prompts/bootstrap.md` (thay `<KIT>` bằng đường dẫn tới kit).
3. Trả lời các câu hỏi của AI, duyệt danh sách file nó đề xuất, rồi để nó ghi.
4. Thỉnh thoảng chạy `prompts/check.md`.

Mọi thứ AI tạo ra trên máy hoặc trong repo của bạn đều được bọc giữa hai dòng đánh dấu `starter-kit:begin` và `starter-kit:end`. Chạy lại prompt chỉ thay phần nằm giữa hai dòng đó, không động tới phần còn lại.

## Bản quyền

Kit được phát hành theo [CC BY-ND 4.0](LICENSE). Bạn được dùng kit ở bất cứ đâu, kể cả trong công việc; được tự sửa để dùng riêng; phải ghi nguồn khi chia sẻ; **không được phân phối bản đã sửa**. Cấu hình mà bạn hoặc AI tạo ra từ kit trong môi trường của bạn thuộc về bạn, hoặc về tổ chức nơi bạn làm việc.
