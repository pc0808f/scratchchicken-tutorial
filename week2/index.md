---
layout: default
title: 第二週：讓電子雞動起來！
nav_order: 4
has_children: true
---

# 🎬 第二週：讓電子雞動起來！
{: .fs-9 }

是時候讓你的電子雞活起來了！這一週我們將學習動畫製作，讓電子雞會眨眼、搖尾巴，並且能夠對你的互動做出可愛的回應。
{: .fs-6 .fw-300 }

[開始學習](#學習內容){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [下載學習單](./worksheets/第二週學習單.md){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## 🎯 本週學習目標

完成本週學習後，你將能夠：

- ✅ **掌握事件觸發**：學會使用「當...時」積木
- ✅ **製作基本動畫**：讓角色移動、旋轉、改變大小
- ✅ **切換造型**：讓電子雞展現不同表情和姿態
- ✅ **處理使用者互動**：回應滑鼠點擊和鍵盤按鍵
- ✅ **運用音效**：為動畫添加生動的聲音效果

## 📚 學習內容

### 1️⃣ 事件積木的魔法
{: .text-green-300}

事件積木是讓電子雞「活起來」的關鍵！它們就像電子雞的「感應器」，能夠察覺到各種變化：

#### 🔸 常用的事件積木

<div class="event-blocks-gallery">
<img src="./resources/當綠旗被點擊.jpg" alt="當綠旗被點擊積木" class="event-block">
<p class="block-description">程式開始執行</p>

<img src="./resources/當角色被點擊.jpg" alt="當角色被點擊積木" class="event-block">
<p class="block-description">滑鼠點擊角色時</p>

<img src="./resources/當按鍵被點擊.jpg" alt="當按鍵被點擊積木" class="event-block">
<p class="block-description">鍵盤按鍵觸發</p>

<img src="./resources/當收到訊息.jpg" alt="當收到訊息積木" class="event-block">
<p class="block-description">收到廣播訊息時</p>
</div>

#### 💡 實作練習：電子雞的第一個反應

**步驟1：製作點擊反應**
1. 選擇你的電子雞角色
2. 拖拉「當這個角色被點擊」積木
3. 在下方接上「說 [你好！] 持續 2 秒」
4. 點擊你的電子雞，看看會發生什麼！

### 2️⃣ 動作動畫基礎
{: .text-green-300}

讓電子雞動起來有許多方法，我們先從基本動作開始：

#### 🔸 移動類動畫

<div class="animation-blocks">
<img src="./resources/移動類積木.jpg" alt="移動類動畫積木" class="block-example">
</div>

#### 🔸 視覺變化動畫

<div class="animation-blocks">
<img src="./resources/視覺變化動畫.jpg" alt="視覺變化動畫積木" class="block-example">
</div>

#### 💡 實作練習：讓電子雞跳舞

**目標**：製作一個簡單的跳舞動畫

**程式積木組合**：

<div class="example-code">
<img src="./resources/製作一個簡單的跳舞動畫.jpg" alt="跳舞動畫程式積木組合" class="code-example">
</div>

### 3️⃣ 造型切換動畫
{: .text-green-300}

造型切換是製作生動動畫的重要技巧！

#### 🔸 準備造型

我們使用 Scratch 內建的小雞角色，它有三種不同的造型：

<div class="costume-gallery">
<div class="costume-item">
<img src="./resources/平常小雞.jpg" alt="平常小雞造型" class="costume-image">
<p><strong>1. 平常小雞</strong>：預設的可愛樣子</p>
</div>

<div class="costume-item">
<img src="./resources/開嘴小雞.jpg" alt="開嘴小雞造型" class="costume-image">
<p><strong>2. 開嘴小雞</strong>：張嘴準備說話或吃東西</p>
</div>

<div class="costume-item">
<img src="./resources/低頭小雞.jpg" alt="低頭小雞造型" class="costume-image">
<p><strong>3. 低頭小雞</strong>：害羞或思考的樣子</p>
</div>
</div>

#### 🔸 造型切換積木

<div class="costume-blocks">
<img src="./resources/造型切換積木.jpg" alt="造型切換積木" class="block-example">
</div>

#### 💡 實作練習：電子雞開闔嘴動畫

**目標**：讓小雞定期開闔嘴巴，就像在說話或呼吸

**步驟**：
1. 選擇 Scratch 內建的小雞角色
2. 使用造型切換製作開闔嘴動畫
3. 建立以下程式：

<div class="practice-code">
<img src="./resources/實作練習：電子雞開闔嘴.jpg" alt="開闔嘴動畫程式積木" class="code-example">
</div>

**動畫效果說明**：
- 小雞會從平常樣子開始
- 每隔 2 秒張嘴 0.5 秒
- 形成自然的呼吸或說話效果

### 4️⃣ 互動式動畫設計
{: .text-green-300}

讓電子雞能夠回應玩家的各種操作：

#### 🔸 滑鼠互動

```scratch
當這個角色被點擊     # 點擊角色
如果 <碰到滑鼠指標?> 那麼  # 滑鼠碰觸檢測
  說 [你摸我了！] 持續 1 秒
```

#### 🔸 鍵盤互動

```scratch
當按下 [空白] 鍵     # 空白鍵觸發
如果 <按下 [上] 鍵?> 那麼  # 方向鍵檢測
  y 改變 (10)        # 向上移動
```

#### 💡 實作練習：電子雞情緒反應

**目標**：按不同按鍵觸發不同情緒

```scratch
當按下 [h] 鍵        # H = Happy 開心
換成 [開心] 造型
說 [我很開心！] 持續 2 秒
播放音效 [meow]

當按下 [s] 鍵        # S = Sad 難過
換成 [難過] 造型
說 [嗚嗚...] 持續 2 秒
播放音效 [cat]
```

#### 🎨 情緒造型範例

以下是不同情緒的電子雞造型參考：

<div class="demo-gallery">
<img src="./resources/開心電子雞.png" alt="開心的電子雞" class="demo-image">
<img src="./resources/難過電子雞.png" alt="有點難過的電子雞" class="demo-image">
<img src="./resources/極度難過電子雞.png" alt="極度難過的電子雞" class="demo-image">
</div>

**造型設計要點**：
- 😊 **開心**：瞇瞇眼、上揚嘴角、充滿活力
- 😐 **有點難過**：眼角下垂、嘴巴平直
- 😭 **極度難過**：眼淚直流、嘴角明顯下垂、需要安慰

### 5️⃣ 音效與動畫的結合
{: .text-green-300}

聲音能讓動畫更加生動有趣！

#### 🔸 音效積木

```scratch
播放音效 [meow]        # 播放音效（不等待）
播放音效 [meow] 直到播完  # 播放音效（等待結束）
將音量改變 (10)        # 調整音量
停止所有音效           # 停止音效
```

#### 💡 綜合實作：電子雞完整互動

結合所有學過的技巧，製作一個完整的互動動畫：

```scratch
當 🏁 被點擊
重複執行
  等待 (2) 秒
  換成 [眨眼] 造型
  等待 (0.1) 秒
  換成 [預設] 造型

當這個角色被點擊
播放音效 [meow]
換成 [開心] 造型
說 [謝謝你和我玩！] 持續 2 秒
重複 (3) 次
  將大小改變 (10)
  等待 (0.1) 秒
  將大小改變 (-10)
  等待 (0.1) 秒
換成 [預設] 造型
```

## 🎮 本週小挑戰

### 🥉 銅牌挑戰：基礎動畫師
製作一個包含以下功能的電子雞：
- 能夠眨眼（自動重複）
- 點擊時會說話
- 按空白鍵會跳一下

### 🥈 銀牌挑戰：互動設計師
在銅牌基礎上，增加：
- 3種不同的情緒造型
- 對應的鍵盤觸發（h=開心、s=難過、a=生氣）
- 每種情緒都有相應的音效和動作

### 🥇 金牌挑戰：動畫大師
創作一個完整的電子雞互動系統：
- 至少5種不同動畫
- 滑鼠跟隨功能
- 組合動畫（如：開心時會跳舞）
- 背景音樂配合

## 📖 學習資源

### 📋 本週檔案下載
- [🎨 電子雞造型範例](./resources/電子雞造型包.sb3)
- [📝 第二週學習單](./worksheets/第二週學習單.md)
- [🎵 音效素材包](./resources/音效包/)
- [💡 範例程式專案](./scratch_examples/)

### 🎯 重點提醒卡
- **事件積木**是動畫的觸發器
- **等待積木**控制動畫速度
- **造型切換**創造視覺變化
- **音效配合**增加真實感
- **重複積木**製作連續動作

### 🔗 延伸學習
- [Scratch 官方動畫教學](https://scratch.mit.edu/ideas)
- [動畫製作技巧影片](../resources/videos/)
- [下週預告：變數與餵食系統](../week3/)

## 🏆 學習檢核表

在進入下一週前，請確認你已經：

- [ ] 理解事件積木的運作原理
- [ ] 能夠製作基本的移動動畫
- [ ] 學會切換造型製作動畫
- [ ] 能夠處理滑鼠和鍵盤互動
- [ ] 成功結合音效與動畫
- [ ] 完成本週的小挑戰
- [ ] 建立個人的動畫作品

---

## 🎊 完成第二週了嗎？

恭喜你讓電子雞動起來了！現在你的電子雞不再只是靜態的圖片，而是一個會互動、有感情的數位寵物！

下一週我們將學習**變數系統**，為電子雞加入**餵食功能**，讓牠真正需要你的照顧！

[📖 返回課程總覽](../){: .btn .btn-outline } [▶️ 前往第三週](../week3/){: .btn .btn-primary }