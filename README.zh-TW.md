<div align="center">

# LINE Bot with Gemini AI

[English](README.md) | [繁體中文](README.zh-TW.md)

這是一個結合 LINE Messaging API 和 Google Gemini AI 的聊天機器人專案。

</div>

---

### 功能特點

- 整合 LINE Messaging API
- 使用 Google Gemini AI 進行對話生成
- 支援即時訊息回覆
- 使用環境變數管理敏感資訊

### 安裝需求

- Python 3.8 或更高版本
- pip（Python 套件管理器）

### 必要套件

```plaintext
flask==3.0.2
line-bot-sdk==3.5.1
pyngrok==7.1.5
google-generativeai==0.3.2
python-dotenv==1.0.1
```

### 安裝步驟

1. 克隆專案：

```bash
git clone [您的專案URL]
cd [專案資料夾名稱]
```

2. 安裝相依套件：

```bash
pip install -r requirements.txt
```

3. 設定環境變數：
   建立 `.env` 檔案並填入以下資訊：

```plaintext
LINE_CHANNEL_ACCESS_TOKEN=您的LINE Channel Access Token
LINE_CHANNEL_SECRET=您的LINE Channel Secret
GEMINI_API_KEY=您的Gemini API金鑰
```

### 使用方法

1. 執行應用程式：

```bash
python main.py
```

2. 使用 ngrok 建立通道（選用）：

```bash
ngrok http 5000
```

3. 在 LINE Developers Console 設定 Webhook URL：
   - 設定為 `https://您的網域/callback`

### 專案結構

```plaintext
.
├── README.md
├── README.zh-TW.md
├── main.py                 # 主程式檔案
├── requirements.txt        # 相依套件清單
├── .env                    # 環境變數設定檔
└── .gitignore             # Git 忽略檔案清單
```

### 設定說明

#### LINE Bot 設定
1. 前往 [LINE Developers Console](https://developers.line.biz/console/)
2. 建立新的 Provider 和 Channel
3. 取得 Channel Access Token 和 Channel Secret
4. 開啟 Webhook 功能並設定 URL

#### Gemini AI 設定
1. 前往 [Google AI Studio](https://makersuite.google.com/app/apikey)
2. 建立新的 API 金鑰
3. 將金鑰加入 `.env` 檔案

### 注意事項

- 請確保 `.env` 檔案已被加入 `.gitignore`
- 請勿將敏感資訊直接寫入程式碼中
- 使用前請確認已取得所需的 API 金鑰和權限
- 建議在本機測試時使用 ngrok 進行測試

### 常見問題

1. **無法連接到 LINE Bot？**
   - 確認 Webhook URL 設定是否正確
   - 檢查 Channel Access Token 和 Channel Secret 是否正確
   - 確認 Webhook 功能是否已開啟

2. **Gemini AI 無法回應？**
   - 確認 API 金鑰是否正確
   - 檢查網路連線狀態
   - 確認 API 使用額度是否足夠

3. **程式無法啟動？**
   - 確認所有相依套件是否已正確安裝
   - 檢查 Python 版本是否符合要求
   - 確認環境變數是否正確設定

### 開發建議

- 建議使用虛擬環境進行開發
- 定期更新相依套件
- 保持程式碼簡潔且註解完整
- 遵循 Python 程式碼風格指南

### 貢獻指南

歡迎提交 Pull Request 或建立 Issue 來改善專案。在提交之前，請確保：

1. 程式碼符合現有的程式碼風格
2. 新功能有適當的測試
3. 文件已更新
4. Commit 訊息清晰明確

### 授權資訊

MIT

### 聯絡方式

📮 如有任何問題或建議:

🐛 建立 Issue
🔀 提交 Pull Request  
📧 發送電子郵件至 [sun055676@gmail.com]