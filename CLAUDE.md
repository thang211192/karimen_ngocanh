# Karimen - Thi thử bằng lái xe ô tô Nhật Bản (仮免許学科試験)

## Mô tả dự án

Web app luyện thi bằng lái xe ô tô karimen (仮免許学科試験) tiếng Nhật, được làm riêng cho **Ngọc Anh** - bạn gái của chủ dự án.

## Thông tin đề thi thật

- **Dạng đề**: 50 câu hỏi ○× (đúng/sai - まるばつ)
- **Thời gian**: 30 phút
- **Điểm đạt**: 45/50 câu trở lên (90%)
- **Mỗi câu**: 1 điểm

## Yêu cầu nội dung

- Câu hỏi phải **bằng tiếng Nhật**, gần chính xác nhất so với đề thi thật
- Phần **dịch tiếng Việt** bên dưới mỗi câu hỏi
- Có **đáp án** (○ hoặc ×) và **giải thích** bằng cả tiếng Nhật lẫn tiếng Việt
- Khi chọn đáp án, **hiện ngay** kết quả đúng/sai và giải thích (không đợi nộp bài)
- Sau khi chọn **không được đổi đáp án**

## Yêu cầu giao diện & trải nghiệm

- Giao diện **song ngữ Nhật-Việt** xuyên suốt
- Thiết kế **giống đề thi thật Nhật Bản** nhất có thể
- Có **đồng hồ đếm ngược 30 phút**, hết giờ tự động nộp bài
- Có **bảng điều hướng câu hỏi** (nhấn số để nhảy đến câu bất kỳ)
- Câu hỏi **xáo trộn ngẫu nhiên** mỗi lần thi
- Sau khi nộp bài: hiện điểm, lọc xem câu đúng/sai/chưa trả lời
- Hỗ trợ **phím tắt**: `1`/`O` = ○, `2`/`X` = ×, mũi tên trái/phải chuyển câu

## Yêu cầu cá nhân hóa cho Ngọc Anh

- Trang web có **lời nhắn khích lệ** dành riêng cho Ngọc Anh
- Màn hình bắt đầu: lời chúc, động viên từ người yêu
- Khi trả lời đúng: **khen ngợi ngẫu nhiên** (ví dụ: "Giỏi lắm Ngọc Anh！")
- Khi trả lời sai: **động viên nhẹ nhàng** (ví dụ: "Không sao, đọc giải thích nha！")
- Màn hình kết quả: **lời nhắn tùy theo điểm số** (perfect, đỗ, gần đỗ, cần luyện thêm)
- Tone: ấm áp, yêu thương, tích cực

## Chủ đề câu hỏi cần bao phủ

Ngân hàng câu hỏi phải bao phủ đầy đủ các chủ đề trong đề thi thật:

1. **信号 (Tín hiệu)** - đèn xanh/đỏ/vàng, đèn nhấp nháy, đèn mũi tên, cảnh sát điều khiển
2. **標識 (Biển báo)** - cấm, chỉ dẫn, cảnh báo, phụ (車両進入禁止, 一方通行, 徐行, 一時停止...)
3. **速度 (Tốc độ)** - tốc độ luật định đường thường/cao tốc, tốc độ xe gắn máy
4. **車間距離・停止距離 (Khoảng cách)** - khoảng cách xe, khoảng cách phanh, khoảng cách phản ứng
5. **追い越し (Vượt xe)** - nguyên tắc vượt phải, ngoại lệ vượt trái, vượt kép, nơi cấm vượt
6. **駐停車 (Dừng đỗ xe)** - phân biệt dừng/đỗ, khoảng cách cấm (ngã tư 5m, trạm buýt 10m, hộp báo cháy 1m...)
7. **交差点 (Ngã tư)** - rẽ trái/phải, ưu tiên bên trái, đường ưu tiên, tắc ngã tư
8. **歩行者保護 (Bảo vệ người đi bộ)** - vạch sang đường, trẻ em, người khuyết tật, xe lăn
9. **緊急車両 (Xe khẩn cấp)** - cách nhường đường, trong/ngoài ngã tư
10. **高速道路 (Đường cao tốc)** - tốc độ tối thiểu 50km/h, cấm lùi/quay đầu, tam giác cảnh báo, làn tăng tốc
11. **安全運転 (Lái xe an toàn)** - hiện tượng fade, hydroplaning, standing wave, creep, phanh động cơ
12. **合図 (Tín hiệu xe)** - rẽ 30m trước, đổi làn 3 giây trước, tín hiệu tay
13. **免許 (Bằng lái)** - bằng tạm, bằng loại 2, thời hạn, nghĩa vụ mang theo
14. **積載・けん引 (Chở hàng & Kéo xe)** - giới hạn chiều cao 3.8m, chiều rộng, kéo xe bằng dây
15. **危険予測 (Dự đoán nguy hiểm)** - trẻ em, bóng lăn, xe buýt dừng, tắc đường ngược chiều
16. **装置・点検 (Thiết bị & Kiểm tra)** - dây an toàn, ghế trẻ em, kiểm tra xe, shaken

## Cấu trúc dự án

```
karimen/
├── index.html      # Trang web chính (HTML + CSS + JS tất cả trong 1 file)
└── CLAUDE.md       # File này - thông tin & yêu cầu dự án
```

## Ghi chú kỹ thuật

- Single-page app, không cần backend hay framework
- Tất cả HTML, CSS, JS nằm trong 1 file `index.html`
- Ngân hàng câu hỏi nằm trong mảng `allQuestions` ở phần `<script>`
- Responsive, hoạt động tốt trên cả điện thoại và máy tính
