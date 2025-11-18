# LocalPlay - Video & HTML Viewer with Advanced Subtitle Support

<img width="1892" height="953" alt="image" src="https://github.com/user-attachments/assets/62d8ff0b-5298-49e0-ab51-f00b1a122935" />

## 📋 Mô tả / Description

**LocalPlay** là một ứng dụng web đơn giản để phát video và xem tài liệu HTML trực tiếp từ thư mục cục bộ của bạn, với hỗ trợ phụ đề tiếng Việt và nhiều ngôn ngữ khác.

**LocalPlay** is a simple web application to play videos and view HTML documents directly from your local folder, with support for Vietnamese and multi-language subtitles.

## ✨ Tính năng / Features

### 🎬 Video Player
- ✅ Hỗ trợ nhiều định dạng video: MP4, MKV, AVI, WebM, MOV
- ✅ Phát video trực tiếp từ thư mục cục bộ
- ✅ Tự động chuyển video tiếp theo khi kết thúc
- ✅ Lưu danh sách phát trong localStorage

### 📝 Subtitle Support
- ✅ Hỗ trợ định dạng: SRT, VTT
- ✅ Tự động nhận diện phụ đề cùng tên với video
- ✅ Điều chỉnh độ trễ phụ đề (delay)
- ✅ Tùy chỉnh:
  - Cỡ chữ (12-60px)
  - Màu chữ
  - Độ đậm viền chữ (text shadow)
- ✅ Hiển thị phụ đề trong chế độ toàn màn hình

### 🌐 HTML Viewer
- ✅ Xem tài liệu HTML trực tiếp
- ✅ Phân biệt file HTML với badge đặc biệt
- ✅ Render HTML trong iframe an toàn

### 💾 Data Persistence
- ✅ Lưu danh sách video/HTML đã load
- ✅ Ghi nhớ thư mục đã chọn lần trước
- ✅ Cảnh báo khi cần load lại thư mục

## 🚀 Cách sử dụng / How to Use

### Bước 1: Mở ứng dụng
1. Tải file `index.html` về máy
2. Mở file bằng trình duyệt web (Chrome, Firefox, Edge, Safari)

### Bước 2: Chọn thư mục
1. Click nút **"📁 Chọn thư mục / Select Folder"**
2. Chọn thư mục chứa video và phụ đề của bạn
3. Ứng dụng sẽ tự động quét và hiển thị danh sách

### Bước 3: Phát video
1. Click vào video bạn muốn xem trong danh sách bên trái
2. Video sẽ tự động phát
3. Nếu có phụ đề, chúng sẽ tự động load

### Bước 4: Tùy chỉnh phụ đề (nếu có)
- **Chọn phụ đề**: Dropdown menu phía dưới
- **Độ trễ**: Điều chỉnh nếu phụ đề không khớp với video
- **Cỡ chữ**: Thay đổi kích thước hiển thị
- **Màu chữ**: Chọn màu yêu thích
- **Viền chữ**: Chọn độ đậm viền để dễ đọc hơn

## 📁 Cấu trúc thư mục đề xuất / Recommended Folder Structure

```
My Videos/
├── Movie1.mp4
├── Movie1.srt
├── Movie1.vi.srt
├── Movie2.mkv
├── Movie2.en.srt
├── Document.html
└── Guide.html
```

### Quy tắc đặt tên phụ đề / Subtitle Naming Rules

Phụ đề phải có cùng tên với video (không bao gồm phần mở rộng):

✅ **Đúng / Correct:**
- `Movie.mp4` + `Movie.srt` ✓
- `Movie.mp4` + `Movie.vi.srt` ✓
- `Movie.mp4` + `Movie.en.srt` ✓

❌ **Sai / Wrong:**
- `Movie.mp4` + `Subtitle.srt` ✗
- `Movie.mp4` + `Different.srt` ✗

## 🎨 Giao diện / Interface

### Sidebar (Bên trái / Left)
- Danh sách video và HTML files
- Hiển thị số lượng phụ đề có sẵn
- Badge đặc biệt cho HTML files
- Thông tin thư mục đã chọn lần trước

### Main Content (Giữa / Center)
- Video player với controls
- HTML viewer
- Hiển thị phụ đề overlay

### Control Panel (Dưới / Bottom)
- Chọn phụ đề
- Điều chỉnh delay
- Tùy chỉnh style phụ đề

## 🔧 Yêu cầu kỹ thuật / Technical Requirements

- **Trình duyệt / Browser:** 
  - Chrome 90+ (recommended)
  - Firefox 88+
  - Edge 90+
  - Safari 14+
  
- **Tính năng cần thiết / Required Features:**
  - File System Access API support
  - localStorage support
  - ES6+ JavaScript support

## ⚠️ Lưu ý quan trọng / Important Notes

1. **Bảo mật / Security:**
   - Ứng dụng chạy hoàn toàn trên trình duyệt (client-side)
   - Không upload dữ liệu lên server
   - File chỉ được đọc, không bị sửa đổi

2. **Tương thích / Compatibility:**
   - Một số trình duyệt có thể yêu cầu chọn lại thư mục sau khi refresh
   - localStorage có giới hạn dung lượng (~5-10MB)

3. **Performance:**
   - Video lớn (>2GB) có thể load chậm
   - Khuyến nghị sử dụng video đã được encode tối ưu

4. **Reload sau khi đóng / Reload After Closing:**
   - Khi mở lại ứng dụng, cần chọn lại thư mục để load video
   - Danh sách video sẽ được giữ lại nhưng file cần được load lại

## 🐛 Xử lý sự cố / Troubleshooting

### Video không phát
- ✅ Kiểm tra định dạng video có được hỗ trợ
- ✅ Thử chọn lại thư mục
- ✅ Kiểm tra console (F12) để xem lỗi

### Phụ đề không hiển thị
- ✅ Đảm bảo tên file phụ đề khớp với video
- ✅ Kiểm tra định dạng (SRT hoặc VTT)
- ✅ Chọn phụ đề từ dropdown menu

### Phụ đề không khớp với video
- ✅ Sử dụng "Độ trễ / Delay" để điều chỉnh
- ✅ Số dương: phụ đề xuất hiện sớm hơn
- ✅ Số âm: phụ đề xuất hiện muộn hơn

### HTML không hiển thị đúng
- ✅ Kiểm tra file HTML có hợp lệ
- ✅ Một số script có thể bị chặn do bảo mật

## 📝 Changelog

### Version 1.0.0 (Current)
- ✨ Initial release
- ✨ Video player with subtitle support
- ✨ HTML viewer
- ✨ localStorage persistence
- ✨ Bilingual interface (Vietnamese/English)
- ✨ Customizable subtitle styling

## 📄 License

MIT License - Free to use and modify

## 👨‍💻 Support

Nếu gặp vấn đề hoặc có góp ý, vui lòng:
- Kiểm tra phần Troubleshooting ở trên
- Kiểm tra console (F12) để xem lỗi chi tiết

If you encounter issues or have suggestions:
- Check the Troubleshooting section above
- Check console (F12) for detailed errors

---

**Made with ❤️ for local media enthusiasts**
