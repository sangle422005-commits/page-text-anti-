# Nhà Mình – Ví gia đình 💸

Một app dùng chung cho cả gia đình (tối đa 3 người), có **Quỹ chung** mà mọi người cùng thấy theo thời gian thực.

## Cấu trúc
- `index.html` – toàn bộ app (giao diện + logic)
- `firebase.js` – cấu hình Firebase (**bắt buộc dán `apiKey`**)
- `firestore.rules` – luật bảo mật Firestore
- `firebase.json`, `.firebaserc` – cấu hình Firebase CLI
- `favicon.svg` – icon

## Bật đồng bộ chung (bắt buộc để cả nhà cùng thấy dữ liệu)
1. Firebase Console → Project settings → copy `apiKey` dán vào `firebase.js`.
2. Authentication → bật **Email/Password** (và Google nếu muốn).
3. Authentication → Settings → Authorized domains → thêm domain Render (`xxx.onrender.com`).
4. Firestore Database → Rules → dán nội dung `firestore.rules` → Publish.

## Cách dùng
- Người 1: đăng ký → **Tạo gia đình mới** → vào Cài đặt copy **Mã gia đình**.
- Người 2, 3: đăng ký → **Tham gia gia đình** → nhập mã. Từ đó cùng thấy chung giao dịch, quỹ chung, ngân sách, mục tiêu.

## Deploy lên Render
Static Site → Build command: để trống → Publish directory: `.`
