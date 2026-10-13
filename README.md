# 🎤 Where Were You Yesterday? – Phòng lồng tiếng Anh và Trung

Trang web giúp học sinh 4–10 tuổi luyện nói và hát bài *Where Were You Yesterday?* của Little Fox bằng **tiếng Anh** và **tiếng Trung** (你昨天在哪里？).

## Các file

Tất cả file nằm chung một chỗ, không cần thư mục con:

```
index.html              # Trang chủ: chọn tiếng Anh hoặc tiếng Trung
README.md
where-en.html           # Phòng tiếng Anh
where-en.mp4            # Video tiếng Anh (chỉ còn nhạc nền)
where-en-goc.mp3        # Âm thanh gốc tiếng Anh (có giọng hát)
where-en-poster.jpg     # Ảnh bìa
where-zh.html           # Phòng tiếng Trung
where-zh.mp4            # Video tiếng Trung (chỉ còn nhạc nền)
where-zh-goc.mp3        # Âm thanh gốc tiếng Trung (có giọng hát)
where-zh-poster.jpg     # Ảnh bìa
```

## Mỗi phòng có 3 tab

- **🎬 Nghe mẫu**: video bài hát có giọng hát gốc, kèm lời bài hát và nghĩa tiếng Việt (tiếng Trung có thêm phiên âm pinyin). Bấm một câu để nghe từ câu đó. Nút **CC** bật/tắt phụ đề karaoke.
- **🗣 Luyện tập**: mỗi câu một thẻ. Bấm **🔊** để nghe riêng câu đó (chữ tô màu theo lời hát), **🐢** để nghe chậm, **🎤** để thu giọng mình và **▶** để nghe lại. Câu lặp lại trong bài chỉ hiện một lần (có ghi "hát 2 lần").
- **🎤 Thử tài**: video chỉ còn nhạc nền, có phụ đề **karaoke** (chữ chuyển đỏ đúng lúc hát) và camera tròn với **🎭 mặt nạ vui** (Mèo, Cún, Thỏ, Gấu, Cáo, Gấu trúc). Có thể bật **🎵 Hát theo giọng mẫu (nhỏ)**: giọng mẫu chỉ phát ra loa, không bị ghi vào video. Ghi xong có 3 nút: **▶ Xem lại**, **⬇ Tải video về**, **🔁 Thử lại**.

## Đưa lên GitHub Pages

1. Tạo repository mới trên GitHub, ví dụ `where-were-you`.
2. Bấm **Add file → Upload files**, chọn cả 10 file ở trên (giữ phím Ctrl để chọn nhiều file), rồi bấm **Commit changes**.
3. Vào **Settings → Pages**. Ở mục *Source*, chọn **Deploy from a branch**, chọn nhánh `main` và thư mục `/ (root)`, rồi bấm **Save**.
4. Sau khoảng 1–2 phút, trang sẽ có địa chỉ `https://<tên-tài-khoản>.github.io/where-were-you/`.

> ⚠️ Micro và camera chỉ hoạt động khi trang chạy qua **https** (GitHub Pages có sẵn). Mặt nạ vui cần có mạng Internet khi dùng lần đầu.

## Hướng dẫn cho học sinh

1. Mở trang bằng **Chrome, Edge** (máy tính hoặc Android) hoặc **Safari** (iPad, iPhone), rồi chọn tiếng Anh hoặc tiếng Trung.
2. **🎬 Nghe mẫu**: nghe cả bài vài lần.
3. **🗣 Luyện tập**: nghe từng câu, thu giọng mình và nghe lại cho thuộc.
4. **🎤 Thử tài**: bấm **Cho phép** khi trình duyệt hỏi quyền dùng camera và micro, rồi đeo tai nghe và chọn mặt nạ nếu thích. Bấm **Bắt đầu thử tài** và hát theo phụ đề cho đến hết bài.
5. Bấm **▶ Xem lại video**. Nếu ưng thì bấm **⬇ Tải video về** để nộp bài cho cô.

## Khi gặp lỗi

| Hiện tượng | Cách xử lý |
|---|---|
| Khung báo *"Không tải được where-en.mp4"* (hoặc file khác) | File chưa được tải lên GitHub, hoặc tên file bị sai. Tên phải đúng từng chữ và phân biệt chữ hoa/thường: `where-en (1).mp4` là **sai**. |
| Link GitHub báo lỗi 404 | GitHub Pages chưa bật hoặc chưa chạy xong. Kiểm tra **Settings → Pages** và đợi 1–2 phút. |
| Bấm nút mà không nghe thấy gì | Kiểm tra âm lượng, tắt chế độ im lặng trên iPhone/iPad, rồi bấm lại. |
| Chọn mặt nạ nhưng không thấy gì | Kiểm tra mạng Internet, ngồi thẳng mặt vào camera và đủ ánh sáng, rồi chọn lại mặt nạ. |
| Không thu được âm / không mở được camera | Bấm biểu tượng ổ khoá trên thanh địa chỉ, chọn **Micro** và **Máy ảnh → Cho phép**, rồi tải lại trang. |

## Ghi chú kỹ thuật

- Nhạc nền được tách khỏi giọng hát bằng AI (mô hình UVR MDX-Net), nên vài chỗ có thể còn lẫn rất nhỏ tiếng hát.
- Thời điểm của từng từ (phụ đề karaoke) được lấy bằng nhận dạng giọng nói (SenseVoice) trên phần giọng hát đã tách. Muốn chỉnh, sửa các số `ws` (giây bắt đầu) và `we` (giây kết thúc) của từng từ trong file `where-en.html` / `where-zh.html`.
- Mặt nạ vui dùng MediaPipe Face Detector của Google. Hình con vật do trang tự vẽ bằng code.
- Mọi thứ chạy ngay trên trình duyệt: hình và tiếng thu được không gửi đi đâu.

## Lưu ý bản quyền

Bài hát *Where Were You Yesterday?* (tiếng Anh, tiếng Trung) thuộc bản quyền © Little Fox Co., Ltd., chỉ dùng cho mục đích học tập trong lớp. Nếu để repository ở chế độ **công khai**, thầy cô nên cân nhắc về bản quyền.
