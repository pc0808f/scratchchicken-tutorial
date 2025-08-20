# GitHub Pages 設置指南
## 🌐 將 Scratch 電子雞教學資料部署為教學網站

這份指南將帶您一步步完成 GitHub Pages 的設置，讓您的教學資料變成一個學生可以自學的線上網站。

---

## 📋 前置準備

### 🔧 需要準備的工具
1. **GitHub 帳號** - 如果還沒有，請到 https://github.com 註冊
2. **Git 工具** - 用於版本控制和檔案上傳
3. **文字編輯器** - 建議使用 VS Code 或其他 Markdown 編輯器

### 💻 安裝 Git（如果還沒有的話）
#### Windows 系統：
1. 前往 https://git-scm.com/download/windows
2. 下載並安裝 Git
3. 安裝過程中保持預設設定即可

#### 驗證安裝：
打開命令提示字元（cmd），輸入：
```bash
git --version
```
如果顯示版本號，代表安裝成功。

---

## 🚀 Step 1: 建立 GitHub Repository

### 1.1 登入 GitHub
1. 前往 https://github.com 並登入您的帳號
2. 點擊右上角的「+」號，選擇「New repository」

### 1.2 設定 Repository
**Repository 設定：**
- **Repository name**: `scratchchicken-tutorial`
- **Description**: `Scratch 電子雞創客課程教學網站`
- **Public** ✅ （必須是公開的才能使用免費的 GitHub Pages）
- **Add a README file** ✅
- **Add .gitignore**: 選擇 `None`
- **Choose a license**: 可選擇 `MIT License`

### 1.3 建立 Repository
點擊「Create repository」完成建立

---

## 📁 Step 2: 複製 Repository 到本地

### 2.1 複製 Repository URL
在新建立的 Repository 頁面，點擊綠色的「Code」按鈕，複製 HTTPS URL

### 2.2 Clone 到本地
打開命令提示字元，切換到您想存放專案的目錄：
```bash
cd C:\git
git clone https://github.com/您的用戶名/scratchchicken-tutorial.git
cd scratchchicken-tutorial
```

---

## 📝 Step 3: 準備網站檔案

### 3.1 複製教學資料
將目前的教學資料複製到新的 Repository 資料夾中：
```bash
# 從原本的 scratchchicken 資料夾複製檔案
xcopy C:\git\scratchchicken\week1 C:\git\scratchchicken-tutorial\week1 /E /I
xcopy C:\git\scratchchicken\*.md C:\git\scratchchicken-tutorial\
```

### 3.2 檢查檔案結構
確認資料夾結構如下：
```
scratchchicken-tutorial/
├── week1/
│   ├── scratch_examples/
│   ├── slides/
│   ├── worksheets/
│   ├── resources/
│   └── README.md
├── index.md                    # 網站首頁（即將建立）
├── _config.yml                 # GitHub Pages 設定（即將建立）
└── README.md
```

---

## ⚙️ Step 4: 設定 GitHub Pages

### 4.1 建立 _config.yml 檔案
在專案根目錄建立 `_config.yml` 設定檔

### 4.2 建立網站首頁
建立 `index.md` 作為網站首頁

### 4.3 上傳檔案到 GitHub
```bash
git add .
git commit -m "Initial commit: Add Scratch 電子雞教學網站"
git push origin main
```

---

## 🌐 Step 5: 啟用 GitHub Pages

### 5.1 前往 Repository 設定
1. 在 GitHub 上進入您的 Repository
2. 點擊「Settings」標籤頁
3. 在左側選單找到「Pages」

### 5.2 設定 GitHub Pages
**Source 設定：**
- **Source**: Deploy from a branch
- **Branch**: main
- **Folder**: / (root)

### 5.3 保存設定
點擊「Save」按鈕完成設定

---

## 📋 Step 6: 測試網站

### 6.1 等待部署完成
GitHub Pages 需要幾分鐘時間來建置網站，您可以在 Repository 的「Actions」標籤頁查看部署狀態

### 6.2 訪問網站
部署完成後，您的網站將可以透過以下網址訪問：
```
https://您的GitHub用戶名.github.io/scratchchicken-tutorial
```

---

## 🔄 Step 7: 更新網站內容

### 7.1 本地修改
當您需要更新網站內容時：
1. 在本地修改檔案
2. 測試修改是否正確

### 7.2 推送更新
```bash
git add .
git commit -m "Update: 描述您的修改"
git push origin main
```

### 7.3 自動部署
GitHub Pages 會自動檢測到變更並重新部署網站（通常需要1-5分鐘）

---

## 🎨 Step 8: 自訂網站外觀（可選）

### 8.1 選擇主題
GitHub Pages 支援 Jekyll 主題，您可以在 `_config.yml` 中設定：

### 8.2 自訂樣式
如果需要更多自訂，可以建立 `assets/css/style.scss` 檔案

---

## 🛠️ 常見問題解決

### ❓ 問題1：網站無法訪問
**可能原因：**
- Repository 不是公開的
- GitHub Pages 還在建置中
- 分支設定錯誤

**解決方法：**
1. 確認 Repository 是 Public
2. 等待 5-10 分鐘
3. 檢查 Pages 設定中的分支是否為 main

### ❓ 問題2：網站內容沒有更新
**可能原因：**
- 檔案沒有正確推送到 GitHub
- GitHub Pages 快取

**解決方法：**
```bash
git status  # 檢查檔案狀態
git push origin main  # 確認推送
```

### ❓ 問題3：Markdown 格式顯示異常
**可能原因：**
- Jekyll 處理 Markdown 的方式與本地不同
- 檔案編碼問題

**解決方法：**
- 檢查檔案編碼是否為 UTF-8
- 確認 Markdown 語法正確
- 查看 GitHub 的建置日誌

---

## 📞 取得更多幫助

### 🔗 官方資源
- **GitHub Pages 官方文件**: https://docs.github.com/en/pages
- **Jekyll 官方文件**: https://jekyllrb.com/docs/
- **Markdown 語法指南**: https://guides.github.com/features/mastering-markdown/

### 🆘 常見支援管道
- **GitHub Community**: https://github.community/
- **Stack Overflow**: 搜尋 "github pages" 相關問題
- **YouTube 教學影片**: 搜尋 "GitHub Pages tutorial"

---

## ✅ 完成檢核表

完成以下步驟後，您的教學網站就會成功上線：

**基本設定：**
- [ ] 建立 GitHub 帳號
- [ ] 安裝 Git 工具
- [ ] 建立 Repository
- [ ] 複製檔案到本地

**網站建置：**
- [ ] 建立 _config.yml
- [ ] 建立 index.md
- [ ] 上傳檔案到 GitHub
- [ ] 啟用 GitHub Pages

**測試驗證：**
- [ ] 網站可以正常訪問
- [ ] 所有頁面連結正常
- [ ] 圖片和資源正常載入
- [ ] 手機版顯示正常

**後續維護：**
- [ ] 了解如何更新內容
- [ ] 設定定期備份
- [ ] 規劃內容更新流程

---

**🎉 恭喜！您的 Scratch 電子雞教學網站即將上線！**

接下來我將為您建立完整的網站內容，讓學生可以透過這個網站進行自主學習。