# 🖼️ PNG 圖片透明背景使用指南

## ❌ 問題描述

雖然 PNG 圖片本身是透明背景，但在網頁和 Scratch 中可能出現白灰方塊背景的問題。

## 🌐 網頁顯示解決方案

### ✅ 已修正的 CSS 設定

在 `assets/css/style.scss` 中已加入以下設定：

```css
/* 圖片透明背景處理 */
.demo-image,
img[src$=".png"] {
  background: transparent !important;
  background-color: transparent !important;
  image-rendering: -webkit-optimize-contrast;
  image-rendering: crisp-edges;
}

/* 示範圖片庫樣式 */
.demo-gallery {
  display: flex;
  gap: 1rem;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin: 2rem 0;
  padding: 1rem;
  /* 模擬透明背景的棋盤格效果 */
  background: linear-gradient(45deg,
    rgba(255,255,255,0.9) 25%,
    transparent 25%,
    transparent 75%,
    rgba(255,255,255,0.9) 75%),
    linear-gradient(45deg,
    rgba(255,255,255,0.9) 25%,
    transparent 25%,
    transparent 75%,
    rgba(255,255,255,0.9) 75%);
  background-size: 20px 20px;
  background-position: 0 0, 10px 10px;
  border-radius: 8px;
}
```

### 🎯 使用方法

1. **圖片庫展示**：使用 `demo-gallery` 類別
   ```html
   <div class="demo-gallery">
     <img src="./resources/電子雞.png" alt="電子雞" class="demo-image">
   </div>
   ```

2. **單一狀態圖片**：使用 `chicken-state-image` 類別
   ```html
   <img src="./resources/飢餓狀態.png" alt="飢餓電子雞" class="chicken-state-image">
   ```

## 🎮 Scratch 使用建議

### ✅ 正確匯入步驟

1. **開啟 Scratch 3.0**
   - 使用最新版本的 Scratch 3.0（線上版或桌面版）

2. **匯入角色**
   ```
   1. 點擊「選擇一個角色」按鈕
   2. 選擇「上傳角色」
   3. 選擇你的 PNG 檔案
   4. 等待上傳完成
   ```

3. **檢查透明效果**
   - 匯入後，角色應該沒有背景色塊
   - 如果仍有背景，可能是 Scratch 版本問題

### 🔧 故障排除

#### 問題：Scratch 中仍顯示背景色塊

**解決方案 1：使用繪圖編輯器**
```
1. 在 Scratch 中點擊角色
2. 點擊「造型」標籤
3. 點擊造型下方的「編輯」按鈕
4. 使用「填充」工具選擇透明色
5. 點擊任何白色/灰色背景區域
```

**解決方案 2：重新處理圖片**
```
1. 下載 GIMP（免費圖片編輯軟體）
2. 開啟 PNG 檔案
3. 右鍵選擇「Colors」→「Color to Alpha」
4. 選擇白色作為透明色
5. 匯出為 PNG 格式
```

**解決方案 3：使用線上工具**
```
1. 訪問 remove.bg 或類似網站
2. 上傳你的 PNG 檔案
3. 自動移除背景
4. 下載處理後的檔案
```

### 📱 不同平台注意事項

#### 💻 桌面版 Scratch
- 通常處理透明背景較好
- 建議使用最新版本

#### 🌐 線上版 Scratch
- 可能對某些 PNG 處理有限制
- 如有問題，嘗試桌面版

#### 📲 平板/手機版
- 功能可能受限
- 建議在電腦上完成角色設計

## 🎨 最佳實踐

### ✅ 圖片準備建議

1. **檔案格式**：使用 PNG-24 格式（支援透明度）
2. **解析度**：建議 300x300 像素左右
3. **檔案大小**：控制在 500KB 以下
4. **色彩**：避免使用純白色邊框

### 🎯 設計技巧

1. **清晰邊框**：給角色加上深色邊框線，增加辨識度
2. **適當尺寸**：不要過大或過小，適合 Scratch 舞台
3. **色彩對比**：確保在不同背景下都清楚可見
4. **一致風格**：同一專案中的角色風格保持一致

## 🔍 測試檢查清單

### ✅ 網頁測試
- [ ] 圖片在不同瀏覽器中正常顯示
- [ ] 沒有白色/灰色背景色塊
- [ ] CSS 樣式正確載入
- [ ] 響應式設計正常

### ✅ Scratch 測試
- [ ] 角色匯入成功
- [ ] 透明背景正確顯示
- [ ] 角色大小適中
- [ ] 動畫效果自然

## 📞 問題回報

如果仍有透明背景問題，請提供：
1. 使用的瀏覽器版本
2. Scratch 版本（線上/桌面）
3. 具體的錯誤截圖
4. 問題出現的步驟

**聯絡方式**：LINE 私訊老師

---

*💡 記住：好的圖片資源是成功課程的基礎！透明背景讓你的電子雞更加專業和吸引人！*