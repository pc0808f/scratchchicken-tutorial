---
name: a4-coursebook
description: Use when creating or converting Jekyll course pages into printable A4 textbook lessons, especially week pages, Scratch teaching materials, ebook-style layouts, step-by-step image instructions, or classroom worksheets.
---

# A4 課本頁面

將課程週次頁面製作成「可在瀏覽器閱讀，也能直接列印成 A4」的電子課本。優先服務國小 Scratch 課程，保留清楚的教學節奏，不把 Landing Page 的視覺元件直接塞進教材頁。

## 觸發時機

使用者提到以下任一需求時使用本 Skill：

- A4 課本、電子課本、教材列印、直接列印
- 週次課程頁、Scratch 教學頁、學習單
- ebook、單頁／雙頁閱讀、紙本教材風格
- 需要把操作截圖依流程排版

## 核心原則

1. 每一頁只教一個小任務，先確認學生能完成，再安排延伸挑戰。
2. 以實際有效教學時間排課；若課堂約 45 分鐘，頁面不可假設 90 分鐘都能教新概念。
3. 螢幕預覽使用置中的白色 A4 紙張、灰色閱讀背景和頁間距。
4. 列印時隱藏網站導覽列、頁尾、工具列和裝飾，保留純教材內容。
5. 圖片需要看細節時，一頁最多放兩張，且上下排列；圖片簡單且清楚時才使用 2×2 或三欄縮圖。
6. 先放「完成目標」大圖，再放分步驟操作圖，讓學生知道正在完成什麼。
7. 不把尚未教過的功能提前混入本週；例如背景製作週不放砲位、老鼠移動或碰撞程式。

## 建議頁面結構

每個週次頁依需要從以下頁面中選擇，不必全部使用：

1. 封面：週次、主題、課程名稱、簡短任務描述。
2. 學習目標：本週完成成果、關鍵概念、課堂取捨。
3. 操作介面：一張完整 Scratch 畫面，下面用編號說明區域。
4. 完成目標：一張完整成品大圖，標出起點、過程和終點。
5. 操作步驟：依時間順序放截圖與短說明。
6. 完成檢查：學生可以勾選的 checklist。
7. 下週預告：只說明下一個核心任務，不提前教完整內容。

## 圖片排版規則

### 大圖

適合以下內容：

- Scratch 完整介面
- 完成的舞台或背景
- 需要辨識細節的積木
- 需要看清楚工具列的操作截圖

建議使用：

```html
<div class="large-resource">
  <img src="{{ '/weekX/resources/image.jpg' | relative_url }}" alt="清楚描述圖片內容">
  <span>圖片下方放一句操作重點</span>
</div>
```

### 兩張大圖

兩張圖必須上下排列，不要左右並排造成窄圖或大面積空白：

```html
<div class="large-process">
  <div><img src="..." alt="步驟一"><span>01 步驟說明</span></div>
  <div><img src="..." alt="步驟二"><span>02 步驟說明</span></div>
</div>
```

### 小圖流程

只有在截圖內容簡單、縮小後仍能辨識時，才使用多張小圖：

```html
<div class="route-steps">
  <div><img src="..." alt="步驟一"><span>01 說明</span></div>
  <div><img src="..." alt="步驟二"><span>02 說明</span></div>
</div>
```

## Scratch 教學規則

- 背景固定元素：草地、道路、老鼠洞、飼料桶等可放在背景。
- 可互動元素：砲位、老鼠、母雞、按鈕等應做成角色。
- 固定砲位適合用獨立角色，使用「空砲位」與「守衛母雞」兩個造型。
- 每週先完成一個可測試成果，再加入外觀或進階邏輯。
- 「僅適用於這個角色」是 Scratch 的正式文字；可在教材中補充說明這是角色專屬變數，適合分身各自保存血量。
- 不用清單和角度運算時，路徑可先用簡化的繪圖和固定路線教學。

## A4 列印 CSS

頁面應包含下列概念：

```css
@page { size: A4; margin: 0; }

@media print {
  .site-header, .site-footer, .ebook-toolbar { display: none !important; }
  .page-content, .page-content > .wrapper { padding: 0 !important; }
  .book-page {
    width: 210mm;
    height: 297mm;
    min-height: 297mm;
    margin: 0;
    box-shadow: none;
    break-after: page;
    overflow: hidden;
  }
}
```

列印版要使用 `print-color-adjust: exact` 保留封面或重點區塊的底色；不要讓網站導覽或預覽工具列出現在紙本教材上。

## 建立或改寫流程

1. 先讀取週次實際教學內容與圖片檔案的修改時間。
2. 依檔案時間和檔名建立操作順序，不要自行猜測圖片流程。
3. 分類圖片：介面、完成目標、步驟、延伸、成果。
4. 先寫本週 45 分鐘核心成果，再決定要放幾頁。
5. 以 A4 白頁建立頁面，不先製作複雜互動元件。
6. 將圖片放入對應步驟，圖片下方加一句可執行的說明。
7. 將超出本週範圍的圖片移到下一週或標為延伸挑戰。
8. 啟動本機 Jekyll 預覽，確認桌面、手機和列印版。

## 驗證清單

- 頁面使用正確的 `weekX/index.md` 路徑。
- 所有圖片路徑使用 Jekyll 的 `relative_url`。
- 每張圖片有描述性的 `alt` 文字。
- 圖片不會在手機上超出頁面寬度。
- 列印預覽為 A4，頁面沒有被奇怪地切成兩半。
- 每頁大圖足夠清楚，沒有為了塞圖而縮得太小。
- 課程內容沒有重複上一週或提前教下一週的核心功能。
- 執行 `git diff --check`。
- 使用本機 Jekyll 預覽確認頁面回應 `200 OK`。
