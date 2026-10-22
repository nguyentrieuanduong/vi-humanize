# Nguồn

Skill này chưng cất từ các dự án dưới đây. Các dự án GitHub đều dùng giấy phép MIT; trang Wikipedia dùng CC BY-SA 4.0 và chỉ được lấy ý. Một số ví dụ trong [patterns.md](patterns.md) và [keep-signals.md](keep-signals.md) được chuyển thể từ các nguồn này, có sửa lại để bản "sau" không thêm dữ kiện. Thông báo bản quyền đầy đủ của từng nguồn nằm trong `THIRD-PARTY-NOTICES.md` ở gốc kho mã.

| Dự án | Lấy gì |
|---|---|
| [blader/humanizer](https://github.com/blader/humanizer) (MIT) | Khung giải thích vì sao văn máy nghe như vậy; nhóm làm màu, nhịp theo công thức, phóng đại, trình bày, rác khung chat, sai người đọc; nguyên tắc mẫu văn thắng quy tắc; trả kết quả theo kiểu việc |
| [andyluu98/vn-humanize](https://github.com/andyluu98/vn-humanize) (MIT) | Danh mục dấu hiệu tiếng Việt và nhóm V; danh sách dấu hiệu người viết thật cần giữ và những thứ không phải dấu hiệu AI; bảng giọng theo thể loại; nguyên tắc không nâng mức trang trọng, không bịa giọng "tôi" |
| [cuongducle/viet-humanize](https://github.com/cuongducle/viet-humanize) (MIT) | Đọc ngữ cảnh trước; không có từ cấm; giữ mức chắc chắn ("có thể giảm" không thành "giảm"); không chọn chế độ; chỉ trả sản phẩm, không mặc định kèm bảng phân tích |
| [fioenix/vietnamizer](https://github.com/fioenix/vietnamizer) (MIT) | Các mẫu ngữ pháp và văn dịch (bổ ngữ kết quả, cặp liên từ, thiếu "là", loại từ, "của", "các/những", bị động "bởi", danh hóa), mục "không sửa khi" cho từng mẫu, quy tắc gạch dài và gạch ngang tiếng Việt, đặc điểm riêng cần giữ |
| [AnhTuan2111/vina-me](https://github.com/AnhTuan2111/vina-me) (MIT) | Bảy điều khi viết mới; phép thử "người ngồi cạnh"; ba mức giọng; danh sách sửa quá tay |
| [longhang2004/vietnamese-humanizer](https://github.com/longhang2004/vietnamese-humanizer) (MIT) | Cân nhắc xưng hô và mức trang trọng, để nguyên văn đã ổn; phân biệt văn dịch với bị động và Hán Việt hợp lệ; giữ mức nghĩa vụ, nguồn của nhận định, phần chưa rõ nghĩa và ngữ cảnh thật sự đã được cung cấp |
| [kkhanh-kas/humanizer-VietAcademic](https://github.com/kkhanh-kas/humanizer-VietAcademic) (MIT) | Danh sách quy ước học thuật không được sửa nhầm (câu dài, Hán Việt thuật ngữ, trích dẫn, dấu phẩy thập phân). Không chép ví dụ trước/sau vì một số ví dụ thêm dữ kiện không có trong bản gốc |
| [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) (MIT) | Ý tưởng: giới hạn số lượt sửa; danh sách thứ không được chèn vào vì "dấu hiệu người" giả sẽ thành khuôn mới |
| [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) | Nguồn gốc của phần lớn danh mục; lưu ý dấu hiệu chỉ là gợi ý, không phải bằng chứng |

## Những chỗ skill này chủ động khác nguồn

- Không có cổng cứng: không bắt buộc hỏi trước khi viết, không từ chối thể loại, không bắt chạy script, không vòng lặp "sửa tới khi đạt". Thay bằng hướng dẫn: dùng phương án an toàn rồi nêu giả định, sửa tối thiểu ở thể loại có quy ước chặt, rà một lượt.
- Không mặc định trả bản nháp kèm danh sách dấu hiệu như blader/humanizer; chỉ trả sản phẩm và ghi chú khi cần.
- Không cấm mọi dấu gạch như vina-me; xét chức năng, mật độ, mẫu giọng và quy ước nơi đăng thay vì chỉ xét ký tự.
- Không nhắc khai báo dùng AI ở cuối bài nộp như vn-humanize; việc đó thuộc về người dùng và nơi nộp.

## Mức độ kiểm chứng

Các quy tắc ở đây là tổng hợp từ hướng dẫn và ví dụ của các dự án trên, cộng suy luận về khác biệt giữa cấu trúc tiếng Anh và tiếng Việt. Chưa có đánh giá so sánh trên bộ ngữ liệu độc lập. Cách kiểm hợp lý: so skill với một lời nhắc thường trên các mẫu tiếng Việt chưa thấy (tin nhắn công việc, bài giải thích, báo cáo, bản dịch, bài cá nhân, văn vốn đã tốt), nhờ người đọc bản ngữ chấm mù theo giữ nghĩa, dễ đọc, giữ giọng, xưng hô đúng và số chỗ sửa thừa.

## Phiên bản đã đối chiếu

Giấy phép và chủ sở hữu bản quyền được đối chiếu ngày 2026-10-22 ở các commit sau. Đây là mốc kiểm giấy phép, không khẳng định nội dung skill lấy từ đúng commit đó.

| Dự án | Commit | Ngày commit |
|---|---|---|
| blader/humanizer | `8c307f3` | 2026-10-16 |
| andyluu98/vn-humanize | `5aa44de` | 2026-10-07 |
| cuongducle/viet-humanize | `f87e899` | 2026-10-06 |
| fioenix/vietnamizer | `feed64d` | 2026-10-19 |
| AnhTuan2111/vina-me | `dbeb502` | 2026-10-13 |
| longhang2004/vietnamese-humanizer | `576c80f` | 2026-09-18 |
| kkhanh-kas/humanizer-VietAcademic | `96a083e` | 2026-09-11 |
| conorbronsdon/avoid-ai-writing | `209815c` | 2026-10-20 |
