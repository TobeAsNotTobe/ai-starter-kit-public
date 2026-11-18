# Nguyên tắc

Kit dựa trên hai nguyên tắc dưới đây. Các prompt chỉ là cách thực hiện chúng.

## 1. Người và AI làm việc theo checkpoint

Việc nhỏ làm thẳng. Việc lớn làm theo kế hoạch gồm nhiều checkpoint, chi tiết trong [`WORKFLOW.md`](WORKFLOW.md). Ý chính:

1. **Kế hoạch nằm trong repo** (`plans/<mã>.md`), mỗi checkpoint có mục tiêu, phạm vi, lệnh "xong khi", checkpoint cần trước, và độ khó (S/M/L).
2. **Người duyệt kế hoạch trước khi làm**; trạng thái kế hoạch (`ai-draft`, `review`, `coding`...) được ghi bằng commit.
3. **Mỗi checkpoint một phiên AI.** Phiên đó nhận checkpoint bằng git (hai phiên không nhận trùng), chỉ sửa trong phạm vi, commit một lần khi xong, và tự merge vào nhánh ticket nếu qua các bước kiểm tra.
4. **AI không tự sửa kế hoạch**: việc phát hiện ngoài phạm vi ghi vào inbox; người lập kế hoạch quyết từng mục.
5. **Trạng thái suy ra từ git**, không nằm trong chat. Bất kỳ phiên nào, trên bất kỳ máy nào, chỉ cần đọc repo là làm tiếp được.
6. **Người review cả ticket một lần**, ở PR vào nhánh đích.

Câu lệnh để AI tự làm việc tiếp theo: "làm checkpoint tiếp theo" (`WORKFLOW.md`, mục 9).

## 2. An toàn

- Không ghi khóa API, mật khẩu hay token vào bất kỳ file nào. Hãy dùng kho khóa của hệ điều hành, hoặc kho mà nơi làm việc chỉ định.
- Không đưa cho AI dữ liệu mà nơi làm việc không cho phép.
- Chỉ bật những công cụ hay kết nối mà nơi làm việc cho phép; ưu tiên chế độ chỉ đọc.
- Trước khi ghi đè file có sẵn, AI phải sao lưu hoặc cho bạn xem trước phần thay đổi.
