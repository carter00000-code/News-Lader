# 新聞雷達 PWA — 部署說明

## 檔案說明
```
news-radar/
├── index.html      主程式（全部邏輯在此）
├── manifest.json   PWA 設定檔
├── sw.js           Service Worker（離線支援）
├── icon-192.svg    App 圖示
└── README.md       本說明
```

## 部署到 GitHub Pages（免費，5分鐘完成）

1. 前往 https://github.com 註冊／登入
2. 點「New repository」→ 取名（例如 `news-radar`）→ Public → Create
3. 點「uploading an existing file」→ 把 4 個檔案全部拖進去 → Commit
4. 進入 Settings → Pages → Branch 選 main → Save
5. 等約 1 分鐘，網址會出現：`https://你的帳號.github.io/news-radar`

## iPhone 加入主畫面（變成 App）

1. 用 Safari 開啟上述網址（**必須用 Safari**，Chrome 不支援）
2. 點底部分享按鈕（方形加箭頭的圖示）
3. 選「加入主畫面」
4. 點「新增」
5. 完成！桌面會出現「新聞雷達」圖示，開啟後全螢幕運作

## 未來升級選項

### 串接真實 RSS（需要後端）
台灣各媒體 RSS 因跨域限制，需透過後端 proxy 轉發。
建議使用 Cloudflare Workers（免費方案）建立 RSS proxy。

### 接入 AI 摘要（Anthropic API）
取得 API key 後，在 index.html 加入：
```javascript
const API_KEY = '你的-api-key';
// 呼叫 Claude 生成摘要
```

## 支援媒體（計畫串接）
- 自由時報
- 聯合新聞網
- ETtoday
- TVBS
- 三立新聞
- 中時新聞網
- 公視新聞
- 風傳媒
