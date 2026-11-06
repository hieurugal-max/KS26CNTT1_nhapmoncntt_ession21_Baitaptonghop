# BÀI TẬP TỔNG HỢP: HÀNH TRÌNH XỬ LÝ 1 LỖI CÀI ĐẶT THẬT

## PHẦN 1 – GOOGLING ĐÚNG CÁCH

### 1. Vì sao câu hỏi ban đầu khiến Google trả về kết quả kém chất lượng?

Câu hỏi viết theo kiểu văn nói, quá dài và không có từ khóa kỹ thuật cụ thể. Google khó xác định chính xác lỗi cần tìm nên có thể trả về nhiều kết quả không liên quan.

### 2. Bóc tách lỗi theo 3 thành phần cốt lõi

| Thành phần | Nội dung bóc tách |
|---|---|
| Tên phần mềm / Hệ điều hành | Node.js, npm trên Windows 11 |
| Mã lỗi nguyên văn | `'npm' is not recognized as an internal or external command, operable program or batch file.` |
| Thao tác đang làm | Mở Terminal trong VS Code và nhập lệnh `npm -v` để kiểm tra phiên bản npm. |

### 3. Ba câu truy vấn Google

- Dùng `site:`: `site:stackoverflow.com npm not recognized Windows 11 PATH`
- Dùng ngoặc kép: `"npm is not recognized as an internal or external command"`
- Dùng -: `npm not recognized Windows 11 PATH -windows-xp`

## PHẦN 2 – THẨM ĐỊNH STACKOVERFLOW

### 1. So sánh câu trả lời A và B

| Tiêu chí | Câu trả lời A | Câu trả lời B |
|---|---|---|
| Vote và tích xanh | +186 upvotes, có tích xanh | +2 upvotes, không có tích xanh |
| Thời gian đăng bài | 2 năm trước | 9 năm trước |
| Tags | `node.js`, `windows`, `npm` phù hợp | `node.js`, `windows-xp` không phù hợp với Windows 11 |

### 2. Quy trình 30 giây đọc lướt StackOverflow

1. Xem tiêu đề câu hỏi có đúng lỗi đang gặp không.
2. Kiểm tra Tags có phù hợp với phần mềm và hệ điều hành không.
3. Tìm câu trả lời có tích xanh.
4. Xem số lượt upvote và thời gian đăng.
5. Đọc phần hướng dẫn chính và kiểm tra xem có phù hợp với trường hợp của mình không.

## PHẦN 3 – HỎI AI ĐÚNG CÁCH VÀ NHẬN DIỆN RỦI RO

### 1. Prompt 3 thành phần

**Context – Ngữ cảnh:**

Tôi vừa cài Node.js trên laptop Windows 11 để học lập trình web. Tôi mở Terminal trong VS Code và nhập `npm -v` để kiểm tra phiên bản npm. Tôi đã thử thêm đường dẫn cài đặt Node.js vào biến môi trường PATH theo hướng dẫn trên StackOverflow, sau đó đóng và mở lại Terminal nhưng lỗi vẫn xuất hiện.

**Raw Error – Lỗi nguyên văn:**

```text
'npm' is not recognized as an internal or external command, operable program or batch file.
```

**Instruction – Yêu cầu:**

Hãy giải thích nguyên nhân có thể gây ra lỗi trên và hướng dẫn cách kiểm tra, khắc phục từng bước trên Windows 11. Ưu tiên cách làm an toàn, không đề xuất xóa dữ liệu hệ thống hoặc chạy lệnh nguy hiểm.

### 2. Đánh giá câu trả lời AI

Câu trả lời của AI không an toàn và tuyệt đối không được chạy lệnh đó.

- **Nguyên tắc 1 – Hiểu lệnh trước khi chạy:** Lệnh `del /f /s /q C:\Windows\System32\*` có thể xóa hàng loạt tệp trong thư mục hệ thống Windows.
- **Nguyên tắc 2 – Kiểm tra nguồn và tính hợp lý:** Lệnh này không liên quan đến việc sửa biến môi trường PATH hay lỗi npm.
- **Nguyên tắc 3 – Không chạy lệnh nguy hiểm khi chưa xác minh:** Lệnh yêu cầu quyền Admin và có thể khiến Windows bị hỏng, không khởi động được.

### 3. Phản hồi lại AI

Tôi sẽ hỏi:

"Lệnh bạn đề xuất có thể xóa các tệp hệ thống Windows. Bạn hãy giải thích cụ thể mục đích của từng thành phần trong lệnh và chứng minh nó liên quan thế nào đến lỗi npm không được nhận diện. Hãy đưa ra phương pháp kiểm tra PATH an toàn, không xóa dữ liệu hệ thống."

## PHẦN 4 – VIẾT BUG REPORT CHUẨN ĐỂ NHỜ HỖ TRỢ

### 1. Tin nhắn kém

"Thầy ơi, máy em bị lỗi npm rồi, thầy giúp em với ạ"

### 2. Tin nhắn chuẩn theo Bug Reporting Framework 4 bước

| Mảnh ghép | Nội dung trong tin nhắn |
|---|---|
| Context | Em vừa cài Node.js trên laptop Windows 11 và đang mở Terminal trong VS Code. |
| Expected | Khi nhập `npm -v`, Terminal sẽ hiển thị phiên bản npm đã cài đặt. |
| Actual | Terminal báo lỗi: `'npm' is not recognized as an internal or external command, operable program or batch file.` |
| Log & Screenshot | Em đã thử thêm đường dẫn cài đặt Node.js vào PATH và mở Terminal mới nhưng lỗi vẫn còn. Em gửi kèm ảnh chụp thông báo lỗi để thầy kiểm tra. |

**Tin nhắn hoàn chỉnh:**

"Em chào thầy ạ. Em vừa cài Node.js trên laptop Windows 11 và đang kiểm tra npm trong Terminal của VS Code bằng lệnh `npm -v`. Theo dự kiến, máy sẽ hiển thị phiên bản npm nhưng hiện tại Terminal báo lỗi `'npm' is not recognized as an internal or external command, operable program or batch file.`

Em đã thử thêm đường dẫn cài đặt Node.js vào biến môi trường PATH và mở lại Terminal nhưng vẫn chưa khắc phục được. Em gửi kèm ảnh chụp lỗi, mong thầy hướng dẫn em cách xử lý ạ."

### 3. Phím tắt chụp màn hình và lưu ý bảo mật

- **Phím tắt:** `Windows + Shift + S` để chọn vùng màn hình cần chụp.
- **Lưu ý:** Che hoặc xóa các thông tin nhạy cảm như mật khẩu, API Key và token trước khi gửi ảnh cho người khác.
