# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 專案概述

這是一個名為 "scratchchicken-tutorial" 的 Jekyll 靜態網站專案，提供 Scratch 電子雞創客課程的線上教學內容。專案針對國小四、五年級學生設計，共10週課程，每週75分鐘。

## 技術架構

### 核心技術
- **靜態網站生成器**: Jekyll
- **主題**: Minima (可切換其他 GitHub Pages 支援主題)
- **部署平台**: GitHub Pages
- **樣式**: SCSS/CSS 自訂樣式
- **語言**: 繁體中文 (zh-TW)

### 檔案結構
```
scratchchicken-tutorial/
├── _config.yml                  # Jekyll 主要配置檔
├── _data/course_structure.yml   # 課程結構資料
├── assets/css/style.scss        # 自訂樣式檔
├── index.md                     # 首頁
├── how-to-learn.md             # 學習指南
├── week1-10/                   # 各週課程內容
│   ├── index.md                # 週次主頁
│   ├── resources/              # 課程資源
│   ├── scratch_examples/       # Scratch 範例
│   └── worksheets/             # 學習單與評量
└── resources/                  # 全域資源檔案
```

## 開發指令

### Jekyll 本機開發
```bash
# 安裝相依套件
bundle install

# 啟動本機開發伺服器
bundle exec jekyll serve

# 建置靜態檔案
bundle exec jekyll build
```

### GitHub Pages 部署
專案已配置為自動部署到 GitHub Pages，推送到 main 分支即會自動建置。

## 內容管理

### 新增週次課程
1. 複製 `coming-soon-template.md` 到 `weekX/index.md`
2. 更新 `_data/course_structure.yml` 中的課程狀態
3. 更新 `index.md` 中對應的課程卡片狀態
4. 在 `_config.yml` 的 `header_pages` 新增導航連結

### 課程狀態管理
- `available`: 已開放學習
- `coming_soon`: 建置中

### 樣式自訂
主要樣式定義在 `assets/css/style.scss`，包含：
- 課程卡片系統 (`.week-card`, `.course-overview`)
- 按鈕樣式 (`.btn-primary`, `.learn-btn`)
- 響應式設計
- 色彩主題 (Scratch 綠色系)

## 網站配置重點

### _config.yml 關鍵設定
- `baseurl`: GitHub Pages 子目錄路徑
- `course_structure`: 10週課程資訊
- `custom`: 課程基本資訊與聯絡方式
- `header_pages`: 主選單頁面

### 內容編輯注意事項
- 所有 Markdown 檔案需包含 Front Matter
- 使用 Jekyll 變數語法 `{{ site.custom.* }}`
- 圖片資源放置於適當的 resources 目錄
- Scratch 檔案 (.sb3) 直接提供下載連結