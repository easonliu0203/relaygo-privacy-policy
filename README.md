# RELAY GO 隱私權政策頁面

本目錄包含 RELAY GO 客戶端和司機端的隱私權政策 HTML 頁面，用於 App Store 審核合規。

## 📁 文件結構

```
privacy-policy/
├── index.html          # 重定向頁面（選擇客戶端或司機端）
├── customer.html       # 客戶端隱私權政策
├── driver.html         # 司機端隱私權政策
└── README.md          # 本文件
```

## 🚀 部署到 GitHub Pages

### 步驟 1: 提交文件到 GitHub

```powershell
# 在 mobile 目錄下執行
git add privacy-policy/
git commit -m "Add privacy policy HTML pages for App Store compliance"
git push origin main
```

### 步驟 2: 啟用 GitHub Pages

1. 前往 GitHub 儲存庫：https://github.com/easonliu0203/relaygo-backend
2. 點擊 **Settings** (設定)
3. 在左側選單中點擊 **Pages**
4. 在 **Source** 下拉選單中選擇 **Deploy from a branch**
5. 在 **Branch** 下拉選單中選擇 **main**
6. 在路徑選擇器中選擇 **/mobile/privacy-policy** 或 **/(root)** (如果選擇 root，則 URL 會包含 /mobile/privacy-policy/)
7. 點擊 **Save**

### 步驟 3: 等待部署完成

- GitHub Pages 通常需要 1-2 分鐘完成部署
- 部署完成後，您會在 Pages 設定頁面看到一個綠色的成功訊息
- 訪問 URL 確認頁面可以正常顯示

### 步驟 4: 獲取 URL

部署完成後，您的隱私權政策頁面將可以通過以下 URL 訪問：

**如果選擇 /mobile/privacy-policy 作為根目錄**:
- 首頁: `https://easonliu0203.github.io/relaygo-backend/`
- 客戶端: `https://easonliu0203.github.io/relaygo-backend/customer.html`
- 司機端: `https://easonliu0203.github.io/relaygo-backend/driver.html`

**如果選擇 /(root) 作為根目錄**:
- 首頁: `https://easonliu0203.github.io/relaygo-backend/mobile/privacy-policy/`
- 客戶端: `https://easonliu0203.github.io/relaygo-backend/mobile/privacy-policy/customer.html`
- 司機端: `https://easonliu0203.github.io/relaygo-backend/mobile/privacy-policy/driver.html`

**建議**: 使用第一種方式（選擇 /mobile/privacy-policy 作為根目錄），URL 會更簡潔。

## 📝 更新 App Store Connect

部署完成後，請在 App Store Connect 中更新隱私權政策 URL：

### 客戶端 APP (com.relaygo.customer)
1. 登入 [App Store Connect](https://appstoreconnect.apple.com/)
2. 選擇 **Relay GO** APP
3. 進入 **APP 資訊**
4. 找到 **隱私權政策 URL**
5. 更新為: `https://easonliu0203.github.io/relaygo-backend/customer.html`
6. 點擊 **儲存**

### 司機端 APP (com.relaygo.driver)
1. 登入 [App Store Connect](https://appstoreconnect.apple.com/)
2. 選擇 **Relay GO Driver** APP
3. 進入 **APP 資訊**
4. 找到 **隱私權政策 URL**
5. 更新為: `https://easonliu0203.github.io/relaygo-backend/driver.html`
6. 點擊 **儲存**

## ✅ 驗證部署

在更新 App Store Connect 之前，請確認：

1. ✅ 訪問 URL 可以正常顯示頁面
2. ✅ 頁面不需要 JavaScript 即可顯示內容（雖然我們使用了 JavaScript 來切換語言，但內容本身是靜態的）
3. ✅ 頁面在手機和桌面瀏覽器上都能正常顯示
4. ✅ 中英文切換功能正常運作
5. ✅ 所有連結都可以正常點擊

## 🔧 本地測試

如果您想在本地測試這些頁面，可以使用以下方法：

### 方法 1: 直接在瀏覽器中打開
```powershell
# 在 Windows 中
start customer.html
start driver.html
```

### 方法 2: 使用本地伺服器
```powershell
# 使用 Python 3
python -m http.server 8000

# 然後在瀏覽器中訪問
# http://localhost:8000/customer.html
# http://localhost:8000/driver.html
```

## 📱 特點

- ✅ **純 HTML + CSS**：不依賴外部框架或庫
- ✅ **響應式設計**：支援手機和桌面瀏覽器
- ✅ **中英文雙語**：使用 JavaScript 切換語言
- ✅ **無需 JavaScript 即可顯示內容**：內容是靜態的，JavaScript 只用於語言切換
- ✅ **清晰的排版**：易於閱讀和理解
- ✅ **符合 Apple 5.1.1 要求**：包含所有必要的隱私權政策內容

## 🔄 更新隱私權政策

如果需要更新隱私權政策內容：

1. 編輯 `customer.html` 或 `driver.html`
2. 更新中文和英文內容
3. 更新生效日期
4. 提交並推送到 GitHub
5. GitHub Pages 會自動重新部署（通常在 1-2 分鐘內完成）

## 📞 聯絡資訊

如有任何問題，請聯繫：
- Email: kyle5916263@gmail.com

