# Khóa Học Tiếng Trung Giao Tiếp Thực Chiến - Anh Phungciteen

Trang web Landing Page giới thiệu khóa học tiếng Trung cùng anh Phungciteen, được thiết kế chuẩn xác 100% theo nội dung và hình ảnh gốc, tối ưu hóa giao diện di động & máy tính, tốc độ tải siêu nhanh và sẵn sàng đưa lên Vercel.

---

## 1. Cách điền link Video YouTube

Bạn có 2 cách cực kỳ tiện lợi để điền link video:

### Cách 1: Chỉnh sửa trực tiếp trong file `videos.js` (Khuyên dùng)
Mở file `videos.js` trong thư mục này, bạn sẽ thấy danh sách các vị trí video:
```javascript
const VIDEO_CONFIG = {
  // 1. Video ở đầu trang (dưới tiêu đề "Bỏ hết SÁCH VỞ...")
  hero: "https://www.youtube.com/shorts/...", 

  // 2. Video phần "Học viên sau 7 buổi"
  hocVien7Buoi: "https://www.youtube.com/shorts/...",

  // 3. Video phần "Học thử"
  hocThu: "https://www.youtube.com/watch?v=...",

  // 4. Video phần "Công cụ học giao tiếp độc quyền"
  congCuGiaoTiep: "https://www.youtube.com/shorts/...",

  // 5. Video feedback 1
  feedback1: "https://www.youtube.com/shorts/...",

  // 6. Video feedback 2
  feedback2: "https://www.youtube.com/shorts/...",

  // 7. Video feedback 3
  feedback3: "https://www.youtube.com/shorts/...",

  // 8. 4 ô ảnh feedback cảm nhận học viên (nếu có link ảnh):
  feedbackImages: [
    "",
    "",
    "",
    ""
  ]
};
```
> **Lưu ý:** Hệ thống tự động nhận diện mọi định dạng link:
> - Link YouTube Shorts: `https://www.youtube.com/shorts/xxxxxxxxx`
> - Link YouTube thông thường: `https://www.youtube.com/watch?v=xxxxxxxxx`
> - Link rút gọn: `https://youtu.be/xxxxxxxxx`
> - Hoặc chỉ cần dán mã ID 11 ký tự: `xxxxxxxxx`

### Cách 2: Điền trực tiếp trên giao diện Web
Khi bạn mở trang web lên, ở góc dưới bên phải màn hình có nút màu đỏ **"Điền link YouTube"**.
- Bấm vào nút này, một cửa sổ sẽ hiện ra để bạn dán link các video vào.
- Bấm **"Áp dụng xem ngay"** để kiểm tra ngay lập tức mà không cần chỉnh sửa code.
- Bấm **"Copy mã videos.js"** để sao chép cấu hình vừa nhập và lưu lại vào file `videos.js`.

---

## 2. Cách xem thử trên máy tính (Local Preview)

- **Cách 1**: Đơn giản chỉ cần nhấp đúp (Double Click) trực tiếp vào file `index.html` để mở trong trình duyệt Chrome, Edge, Cốc Cốc,...
- **Cách 2**: Chạy lệnh xem thử qua Node.js (nếu muốn chạy qua localhost):
  ```bash
  npx serve .
  ```
  Sau đó mở `http://localhost:3000`.

---

## 3. Hướng dẫn đưa lên Vercel (Miễn phí 100%)

Dự án đã được cấu hình sẵn file `vercel.json`, tương thích hoàn hảo với Vercel.

### Cách A: Đưa lên qua Vercel CLI (Nhanh nhất - khoảng 1 phút)
1. Mở PowerShell hoặc Terminal tại thư mục `D:\phung - tam`:
   ```bash
   npx vercel
   ```
2. Nếu chưa đăng nhập, Vercel sẽ gửi link đăng nhập qua trình duyệt (đăng nhập bằng tài khoản Vercel / GitHub / Google của bạn).
3. Làm theo hướng dẫn trên màn hình:
   - `Set up and deploy?` -> bấm `y`
   - `Which scope?` -> chọn tài khoản của bạn (bấm Enter)
   - `Link to existing project?` -> bấm `N`
   - `What's your project's name?` -> đặt tên (ví dụ: `tieng-trung-phungciteen`, bấm Enter)
   - `In which directory is your code located?` -> bấm Enter
4. Chờ 10-15 giây, bạn sẽ nhận được đường link web chính thức chạy trên Vercel dạng: `https://tieng-trung-phungciteen.vercel.app`!
5. Để deploy bản chính thức (Production), bạn gõ:
   ```bash
   npx vercel --prod
   ```

### Cách B: Đưa lên qua GitHub & Vercel Dashboard
1. Tạo một repository mới trên GitHub (ví dụ: `tieng-trung-phungciteen`).
2. Tải toàn bộ các file trong thư mục này lên repository đó.
3. Vào trang [vercel.com](https://vercel.com), bấm **"Add New..."** -> **"Project"**.
4. Chọn repository GitHub vừa tạo và bấm **"Deploy"**.
5. Vercel sẽ tự động build và cấp domain miễn phí trong vài giây!

---

## 4. Danh sách các file trong dự án

- `index.html`: Toàn bộ mã nguồn giao diện web (HTML5, Tailwind CSS, JavaScript xử lý nhúng video).
- `videos.js`: Nơi bạn điền link video YouTube và thông tin liên hệ.
- `vercel.json`: Tệp cấu hình tối ưu hiệu năng và đường dẫn cho Vercel.
- `package.json`: Tệp cấu hình dự án chuẩn.
