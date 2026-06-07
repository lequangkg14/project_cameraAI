# 🇻🇳 Nhận Diện Tiền Việt Nam

Web app nhận diện tiền mặt VNĐ (10K, 20K, 50K, 100K) bằng AI Edge Impulse + Web Speech API.

## Tính năng
- 📷 Mở camera và quét tiền theo thời gian thực
- 🤖 Nhận diện bằng AI WASM (Edge Impulse)
- 🔊 Đọc tên tờ tiền bằng giọng nói tiếng Việt
- 📊 Lưu lịch sử và tính tổng
- 📦 Chạy hoàn toàn offline trên trình duyệt

## Cấu trúc
```
browser/
├── index.html                    ← Giao diện chính
├── edge-impulse-standalone.js    ← Runtime Edge Impulse
├── edge-impulse-standalone.wasm  ← Model AI
└── run-impulse.js                ← Classifier API
```

## Deploy lên GitHub Pages

1. Tạo repo mới trên GitHub
2. Push toàn bộ code lên nhánh `main`
3. Vào **Settings → Pages → Source**: chọn `GitHub Actions`
4. Workflow sẽ tự động chạy và deploy

URL sẽ là: `https://<username>.github.io/<repo-name>/`

## Chạy local

```bash
cd browser
python3 -m http.server 8082
# Mở http://localhost:8082
```

> ⚠️ **Lưu ý CORS**: File `.wasm` cần được serve qua HTTP server, không thể mở file:// trực tiếp.
