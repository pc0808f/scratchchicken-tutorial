---
layout: default
title: 第四週：吃飽也要開心玩：互動遊戲（一）
nav_order: 6
has_children: true
---

# 🎮 第四週：吃飽也要開心玩：互動遊戲（一）
{: .fs-9 }

電子雞會吃也會餓了，現在是時候教牠玩遊戲！這一週我們將學習條件判斷，讓電子雞能夠智慧地回應你的互動，並建立快樂度系統讓牠真正「開心」起來！
{: .fs-6 .fw-300 }

[開始學習](#學習內容){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [下載學習單](./worksheets/第四週學習單.md){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## 🎯 本週學習目標

完成本週學習後，你將能夠：

### 💻 技能目標
- ✅ **掌握條件判斷**：學會使用「如果...那麼...否則」的邏輯積木
- ✅ **建立快樂度系統**：創建情緒數值管理機制
- ✅ **滑鼠感應互動**：讓電子雞偵測滑鼠接近和離開
- ✅ **複雜變數操作**：同時管理多個狀態數值
- ✅ **智慧回應設計**：根據不同條件做出不同反應

### 🎨 創意目標
- 🌟 **設計互動小遊戲**：創造好玩的點擊互動
- 🌟 **個性化反應系統**：讓電子雞展現獨特個性
- 🌟 **平衡數值設計**：規劃合理的快樂度變化

### 🤝 邏輯目標
- 👥 **條件邏輯思維**：理解程式的判斷和分支概念
- 👥 **系統性思考**：設計完整的互動生態系統
- 👥 **問題分析能力**：學會拆解複雜的互動邏輯

---

## 📚 學習內容

### 1️⃣ 認識條件判斷：電子雞的智慧大腦
{: .text-green-300}

條件判斷就像是電子雞的「大腦」，讓牠能夠根據不同情況做出聰明的反應！

#### 🔸 什麼是條件判斷？

想像條件判斷就像一個**智慧開關**：
- 🧠 **檢查條件**：先看看現在的狀況如何
- 🎯 **做出判斷**：根據條件決定要做什麼
- 🔀 **分支執行**：走向不同的程式路徑

#### 🔸 日常生活中的條件判斷

每天我們都在使用條件判斷：
- ☀️ 「如果天氣好，那麼去公園玩」
- 🌧️ 「如果下雨，那麼在家看書」
- ⏰ 「如果很晚了，那麼去睡覺，否則再玩一下」

#### 💡 實作練習：電子雞的第一個判斷

**目標**：讓電子雞根據飢餓度說出不同的話

**程式邏輯**：
```scratch
當這個角色被點擊
如果 <(飢餓度) < (30)> 那麼
  說 [我好餓...先餵我吧！] 持續 2 秒
否則
  說 [謝謝你跟我玩！] 持續 2 秒
結束
```

### 2️⃣ 建立快樂度系統：電子雞的情緒生活
{: .text-green-300}

除了會餓，電子雞也需要開心！讓我們為牠建立情緒系統。

#### 🔸 創建快樂度變數

**步驟詳解**：
1. 點擊積木區的「變數」分類
2. 點擊「建立一個變數」按鈕
3. 輸入變數名稱：`快樂度`
4. 設定初始值為 50：使用「將 [快樂度] 設為 (50)」

#### 🔸 快樂度的變化機制

**自然下降系統**：

**使用這個事件積木開始程式**：
<img src="../resources/綠旗.jpg" alt="綠旗" class="green-flag-icon"> 當綠旗被點擊

```scratch
當 綠旗 被點擊
重複執行
  等待 (5) 秒
  將 [快樂度] 改變 (-1)
  如果 <(快樂度) < (20)> 那麼
    說 [我有點無聊...] 持續 1 秒
  結束
```

**互動增加系統**：
```scratch
當這個角色被點擊
如果 <(快樂度) < (80)> 那麼
  將 [快樂度] 改變 (10)
  說 [和你玩真開心！] 持續 2 秒
  播放音效 [pop]
否則
  說 [我已經很開心了！] 持續 2 秒
結束
```

### 3️⃣ 滑鼠感應系統：更自然的互動
{: .text-green-300}

讓電子雞能夠感應滑鼠的接近，就像真的寵物一樣敏感！

#### 🔸 滑鼠偵測積木

**重要積木介紹**：
- 🖱️ **「碰到滑鼠游標？」**：檢查滑鼠是否碰到角色
- 📍 **「滑鼠的x座標」**：取得滑鼠的水平位置
- 📍 **「滑鼠的y座標」**：取得滑鼠的垂直位置

#### 💡 實作練習：滑鼠感應互動

**目標**：滑鼠接近時電子雞會有反應

**使用這個事件積木開始程式**：
<img src="../resources/綠旗.jpg" alt="綠旗" class="green-flag-icon"> 當綠旗被點擊

**程式設計**：
```scratch
當 綠旗 被點擊
重複執行
  如果 <碰到滑鼠游標？> 那麼
    如果 <不是 <(造型編號) = (2)>> 那麼
      換成 [好奇] 造型
      說 [你要跟我玩嗎？] 持續 1 秒
    結束
  否則
    換成 [平常] 造型
  結束
  等待 (0.1) 秒
```

### 4️⃣ 複合條件判斷：更聰明的電子雞
{: .text-green-300}

當電子雞需要同時考慮多個因素時，我們需要更複雜的判斷邏輯。

#### 🔸 邏輯運算積木

**重要邏輯積木**：
- 🔗 **「且」積木**：兩個條件都要成立
- 🔀 **「或」積木**：至少一個條件成立
- 🚫 **「不是」積木**：條件相反

#### 💡 實作練習：智慧互動系統

**目標**：根據飢餓度和快樂度的組合決定反應

```scratch
當這個角色被點擊
如果 <<(飢餓度) < (30)> 且 <(快樂度) < (30)>> 那麼
  換成 [難過] 造型
  說 [我又餓又不開心...] 持續 3 秒
否則
  如果 <<(飢餓度) > (70)> 且 <(快樂度) > (70)>> 那麼
    換成 [超開心] 造型
    說 [我現在超級棒！] 持續 2 秒
    重複 (3) 次
      轉動 (120) 度
      等待 (0.2) 秒
    結束
  否則
    換成 [普通] 造型
    說 [還不錯啦！] 持續 2 秒
  結束
結束
```

### 5️⃣ 設計互動小遊戲：拍拍樂
{: .text-green-300}

結合所有學過的技巧，設計一個完整的互動遊戲！

#### 💡 綜合實作：電子雞拍拍樂遊戲

**遊戲概念**：
- 🎯 在30秒內盡量多拍電子雞
- 📊 每拍一次增加快樂度和分數
- ⏱️ 時間結束後顯示成績

**需要的變數**：
- `分數`（初始值：0）
- `遊戲時間`（初始值：30）
- `遊戲中`（初始值：否）

#### 🎮 完整遊戲程式設計

**開始遊戲（按空白鍵）**：
```scratch
當按下 [空白] 鍵
如果 <不是 <(遊戲中) = (是)>> 那麼
  將 [遊戲中] 設為 (是)
  將 [分數] 設為 (0)
  將 [遊戲時間] 設為 (30)
  說 [遊戲開始！快拍我！] 持續 2 秒

  重複直到 <(遊戲時間) = (0)>
    等待 (1) 秒
    將 [遊戲時間] 改變 (-1)

  將 [遊戲中] 設為 (否)
  說 [時間到！你的分數是 (分數)] 持續 3 秒
結束
```

**拍拍互動**：
```scratch
當這個角色被點擊
如果 <(遊戲中) = (是)> 那麼
  將 [分數] 改變 (1)
  將 [快樂度] 改變 (2)

  重複 (3) 次
    將大小改變 (10)
    等待 (0.05) 秒
    將大小改變 (-10)
    等待 (0.05) 秒

  播放音效 [pop]

  如果 <(分數) 是 (10) 的倍數> 那麼
    說 [太棒了！] 持續 1 秒
  結束
否則
  說 [按空白鍵開始遊戲！] 持續 1 秒
結束
```

---

## 🎮 本週小挑戰

<table class="challenge-table">
<thead>
<tr>
<th>🥉 銅牌挑戰<br>邏輯新手</th>
<th>🥈 銀牌挑戰<br>互動設計師</th>
<th>🥇 金牌挑戰<br>遊戲大師</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<strong>目標</strong>：基礎條件判斷系統<br><br>
<strong>必備功能</strong>：<br>
• 建立快樂度變數<br>
• 點擊增加快樂度<br>
• 根據快樂度改變表情<br>
• 滑鼠接近有反應<br><br>
<strong>完成時間</strong>：20分鐘
</td>
<td>
<strong>目標</strong>：在銅牌基礎上增強智慧<br><br>
<strong>新增功能</strong>：<br>
• 複合條件判斷系統<br>
• 同時管理飢餓度和快樂度<br>
• 不同狀態組合的反應<br>
• 簡單的拍拍樂遊戲<br><br>
<strong>完成時間</strong>：30分鐘
</td>
<td>
<strong>目標</strong>：創作完整互動遊戲<br><br>
<strong>進階功能</strong>：<br>
• 完整計時拍拍樂遊戲<br>
• 分數和排行榜系統<br>
• 多種遊戲模式<br>
• 個人創意互動元素<br><br>
<strong>完成時間</strong>：40分鐘
</td>
</tr>
</tbody>
</table>

## 📝 五分鐘課堂反思

**姓名**：＿＿＿＿＿＿　**班級**：＿＿＿＿　**日期**：＿＿＿＿

### 1️⃣ 我學會了什麼？（請勾選）
- [ ] 使用「如果...那麼」條件判斷
- [ ] 建立和管理快樂度變數
- [ ] 讓電子雞感應滑鼠接近
- [ ] 設計複合條件的智慧反應

### 2️⃣ 今天最有成就感的是：
□ 成功做出條件判斷　□ 電子雞變聰明了　□ 完成拍拍樂遊戲　□ 其他：＿＿＿＿

### 3️⃣ 我遇到的困難是：
□ 理解條件判斷邏輯　□ 變數管理太複雜　□ 程式積木組合困難　□ 沒有困難

### 4️⃣ 下次我想讓電子雞：
＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

### 5️⃣ 給自己今天的表現打分數：⭐⭐⭐⭐⭐ （圈選1-5顆星）

---

## 🎊 完成第四週了嗎？

恭喜你讓電子雞變聰明了！現在牠不只會吃會動，還能根據不同情況做出智慧的反應！

---

## 🔮 第五週課程預告：互動遊戲進階版！

### 🎯 即將學習的重點內容

你的電子雞現在已經很聰明了，但我們還能讓牠更厲害！

**第五週**我們將進入更有挑戰性的遊戲設計：

#### 🎲 **隨機系統**：讓遊戲充滿驚喜
- 🎰 學習隨機數的產生和應用
- 🎁 設計隨機事件和驚喜
- 🎪 創造變化豐富的遊戲體驗

#### 🏃 **移動追蹤遊戲**：動態互動挑戰
- 🖱️ 讓電子雞跟隨滑鼠移動
- 🎯 設計追逐和躲避遊戲
- ⚡ 加入速度和方向控制

#### 🎵 **節奏互動**：音樂與程式的結合
- 🎶 配合音樂節拍的互動設計
- 🥁 創造有節奏感的遊戲
- 🎵 多媒體整合應用

### 🎮 你將能夠創造：
- ✨ 充滿驚喜的隨機互動系統
- 🎪 多樣化的互動小遊戲
- 🎵 結合音樂的節奏遊戲
- 🏆 完整的電子雞遊樂園

### 💡 小提示
完成第五週後，你的電子雞將成為一個真正的「遊戲夥伴」！這是程式設計中非常重要的進階階段——學會創造豐富多變的互動體驗。

準備好打造電子雞遊樂園了嗎？ 🎪✨

[📖 返回課程總覽](../){: .btn .btn-outline } [🎲 前往第五週：互動遊戲進階](../week5/){: .btn .btn-primary }

---

<style>
.challenge-table {
  width: 100%;
  border-collapse: collapse;
  margin: 2rem 0;
  font-size: 0.9rem;
}

.challenge-table th,
.challenge-table td {
  border: 2px solid #e1e4e8;
  padding: 1rem;
  vertical-align: top;
  text-align: left;
}

.challenge-table th {
  background: linear-gradient(135deg, #4CAF50, #45a049);
  color: white;
  font-weight: bold;
  text-align: center;
}

.challenge-table td {
  background: #f8f9fa;
}

.challenge-table td:nth-child(1) {
  border-left: 4px solid #CD7F32; /* 銅色 */
}

.challenge-table td:nth-child(2) {
  border-left: 4px solid #C0C0C0; /* 銀色 */
}

.challenge-table td:nth-child(3) {
  border-left: 4px solid #FFD700; /* 金色 */
}

/* 條件判斷相關樣式 */
.logic-example {
  background: #f0f8ff;
  border: 2px solid #4CAF50;
  border-radius: 8px;
  padding: 1rem;
  margin: 1rem 0;
  font-family: 'Courier New', monospace;
}

.logic-example h5 {
  color: #2e7d32;
  margin: 0 0 0.5rem 0;
}

/* 變數顯示樣式 */
.variable-display {
  display: inline-block;
  background: #e8f5e8;
  border: 2px solid #4CAF50;
  border-radius: 4px;
  padding: 0.3rem 0.6rem;
  font-weight: bold;
  color: #2e7d32;
  font-family: 'Courier New', monospace;
}

/* 互動元素樣式 */
.interaction-demo {
  display: flex;
  gap: 1rem;
  margin: 1rem 0;
  flex-wrap: wrap;
}

.interaction-item {
  flex: 1;
  min-width: 200px;
  background: white;
  border: 2px solid #e1e4e8;
  border-radius: 8px;
  padding: 1rem;
  text-align: center;
}

.interaction-item h4 {
  color: #4CAF50;
  margin: 0 0 0.5rem 0;
}

/* 遊戲元素樣式 */
.game-feature {
  background: linear-gradient(45deg, #ff6b35, #ff8c42);
  color: white;
  border-radius: 8px;
  padding: 1rem;
  margin: 1rem 0;
  text-align: center;
}

.game-feature h4 {
  margin: 0 0 0.5rem 0;
  color: white;
}

/* 程式碼區塊樣式 */
.code-block {
  background: #2d3748;
  color: #e2e8f0;
  border-radius: 8px;
  padding: 1rem;
  margin: 1rem 0;
  font-family: 'Courier New', monospace;
  overflow-x: auto;
  border-left: 4px solid #4CAF50;
}

/* 響應式調整 */
@media (max-width: 768px) {
  .challenge-table {
    font-size: 0.8rem;
  }

  .challenge-table th,
  .challenge-table td {
    padding: 0.5rem;
  }

  .interaction-demo {
    flex-direction: column;
  }

  .interaction-item {
    min-width: auto;
  }
}
</style>