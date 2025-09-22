# Scratch 積木圖示索引

這個檔案提供了所有 Scratch 積木和介面元素的圖片引用，方便各週課程使用。

## 🎮 基本控制元素

### 綠旗（程式開始）
- **檔案路徑**: `../resources/綠旗.jpg`
- **使用範例**: `![綠旗](../resources/綠旗.jpg)`
- **說明**: 用於表示「當綠旗被點擊」事件積木

## 📝 使用指南

### 在各週課程中引用圖片

**方法1: 直接引用**
```markdown
![綠旗](../resources/綠旗.jpg)
```

**方法2: 帶樣式的引用**
```markdown
<img src="../resources/綠旗.jpg" alt="綠旗" class="icon-small">
```

### 路徑說明
- 從週次目錄 (如 week1/, week2/) 引用: `../resources/檔名`
- 從週次子目錄 (如 week1/resources/) 引用: `../../resources/檔名`

## 🎨 建議的CSS樣式

```css
.icon-small {
  width: 24px;
  height: 24px;
  display: inline-block;
  vertical-align: middle;
}

.icon-medium {
  width: 48px;
  height: 48px;
  display: inline-block;
  vertical-align: middle;
}
```