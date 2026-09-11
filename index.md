---
layout: default
title: 首頁
nav_order: 1
---

# 🐔 Scratch 母雞護衛隊塔防課程
{: .fs-9 }

歡迎來到「母雞護衛隊・保衛飼料大作戰」！在這裡，你將使用 Scratch 設計塔防遊戲，讓守衛母雞阻止老鼠大軍偷走飼料。
{: .fs-6 .fw-300 }

[開始學習](./how-to-learn.html){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [第一週課程](./week1/){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## 🚀 今天第一次上課？快速進入這裡！

<div class="quick-start-box">
  <div class="qr-code">
    <img src="{{ site.baseurl }}/assets/images/qr-week1.png" alt="掃描進入塔防課程" />
    <p>📷 用平板或手機掃描</p>
  </div>
  <div class="quick-start-text">
    <p>不管你用的是<strong>筆電</strong>還是 <strong>iPad</strong>，照著做就能馬上開始：</p>
    <ol>
      <li>打開瀏覽器（Chrome / Safari / Edge 都可以）</li>
      <li>掃描左邊的 QR Code，或是自己打網址：</li>
    </ol>
    <p class="quick-start-url">tinyurl.com/hpchicken1</p>
    <p>3. 進去之後，找到 <strong>「開始學習」</strong> 按鈕，跟著老師一步一步做！</p>
  </div>
</div>

---

## 🎯 課程特色

### 🎮 從真實問題出發
雞舍有老鼠偷飼料，我們用 Scratch 設計守衛母雞和塔防遊戲，想像如何解決身邊的問題。

### 🧩 循序漸進的課程設計
從基礎介面認識到複雜的遊戲邏輯，每一週都有新的挑戰與收穫。

### 🤝 培養多元能力
不只學程式，更培養邏輯思維、創造力、問題解決和團隊合作能力。

### 🌟 展現遊戲創意
設計自己的小路、砲塔、敵人和防守策略，讓每個人的塔防遊戲都有不同玩法！

---

## 📚 課程概覽

<div class="course-overview">

{% for course in site.data.course_structure %}
<div class="week-card {{ course.status }}">
  <div class="week-header">
    <span class="week-number">第 {{ course.week }} 週</span>
    {% if course.status == "available" %}
    <span class="status-badge available">開放學習</span>
    {% else %}
    <span class="status-badge coming-soon">建置中</span>
    {% endif %}
  </div>
  <h3>{{ course.title }}</h3>
  <p>{{ course.description }}</p>
  {% if course.status == "available" %}
  <a href="./week{{ course.week }}/" class="learn-btn">開始學習</a>
  {% else %}
  <button class="learn-btn disabled" disabled>敬請期待</button>
  {% endif %}
</div>
{% endfor %}

</div>

---

## 📋 14 週學習目標

每週約 45 分鐘有效教學時間，先完成一個核心成果，再利用剩餘時間處理操作問題與除錯。表定 90 分鐘中的其他時間，會依學生進度彈性安排練習與協助。

| 週次 | 學生這週要學會什麼 | 關鍵字／核心概念 | 完成後的作品成果 |
|---|---|---|---|
| 第 1 週 | 認識 Scratch，加入 `hen` 並修改角色顏色 | 角色、造型、Scratch 介面 | 擁有自己的守衛母雞角色 |
| 第 2 週 | 補完介面與存檔操作，認識事件和基本移動 | 背景、事件、綠旗、移動、存檔 | 建立塔防背景，開始畫出老鼠小路 |
| 第 3 週 | 使用點擊和條件判斷 | 角色被點擊、條件判斷、顯示／隱藏 | 點擊固定砲位，放置守衛母雞 |
| 第 4 週 | 認識分身和碰撞偵測 | 分身、碰撞、重複、刪除分身 | 母雞發射雞蛋，擊中老鼠 |
| 第 5 週 | 使用造型切換和防呆判斷 | 造型切換、條件判斷、座標、重疊檢查 | 砲塔有開火動畫，不能重複或錯誤放置 |
| 第 6 週 | 使用分身、計時和隨機數 | 分身、計時器、隨機數、速度 | 老鼠會一隻隻出現，並加入第二種老鼠 |
| 第 7 週 | 整合程式並練習測試和除錯 | 程式整合、測試、除錯、遊戲規則 | 完成第一版可以玩一場的塔防遊戲 |
| 第 8 週 | 認識變數、廣播和波次控制 | 變數、廣播、波次、等待 | 老鼠會一波接一波進攻 |
| 第 9 週 | 使用變數運算和條件判斷 | 金幣、運算、比較、如果／否則 | 擊退老鼠賺金幣，放置砲塔需要花錢 |
| 第 10 週 | 設計選單和選擇流程 | 商店、按鈕、廣播、角色造型 | 完成可以選擇砲塔的商店 |
| 第 11 週 | 比較不同砲塔的速度和射程 | 複製角色、射速、射程、平衡 | 新增第二種特色砲塔：戰鬥雞 |
| 第 12 週 | 認識角色專屬變數和血量 | 私有變數、血量、血條、難度 | 老鼠有血條，並能調整遊戲難度 |
| 第 13 週 | 使用範圍判定和多目標攻擊 | 範圍攻擊、多重判定、雷射 | 完成能同時攻擊多隻老鼠的雷射母雞 |
| 第 14 週 | 管理勝負狀態、升級和作品表達 | 生命值、Game Over、升級、廣播、發表 | 完成塔防遊戲、成果發表並分享設計想法 |

---

## 🎯 學習目標

完成這個課程後，你將能夠：

- ✅ **熟練操作 Scratch**：掌握程式設計的基本概念和技能
- ✅ **創作塔防遊戲**：完成從老鼠進攻到砲塔防守的遊戲系統
- ✅ **培養邏輯思維**：學會分析問題和設計解決方案
- ✅ **展現創意能力**：設計獨特的路線、砲塔和防守策略
- ✅ **建立合作精神**：透過互測、除錯和成果發表互相學習

---

## 🛠️ 需要準備什麼？

### 💻 基本設備
- 能上網的電腦或平板
- 正常運作的滑鼠（建議）
- 穩定的網路連線

### 🌐 軟體需求
- 任何現代瀏覽器（Chrome、Firefox、Safari、Edge）
- Scratch 3.0 帳號或可存檔的 Scratch 使用方式

### 🎒 學習用品
- 筆記本和筆（記錄創意想法）
- 彩色筆（設計草圖）
- 充滿好奇心和創造力的心！

---

## 🚀 開始你的學習之旅

### 📖 學習建議
1. **按照順序學習**：每一週的內容都是基於前一週的基礎
2. **動手實作**：程式設計最重要的是多練習
3. **發揮創意**：不要害怕嘗試新想法
4. **互相分享**：和同學互測塔防遊戲，一起找出並修正問題

### 🎯 第一步
如果你是第一次學習，建議從這裡開始：

1. **[如何使用這個網站](./how-to-learn.html)** - 了解網站功能和學習方法
2. **[第一週：初探 Scratch](./week1/)** - 開始你的程式設計之旅

---

## 🌟 學生作品展示

> 這裡將展示同學們的優秀作品，激發更多創意靈感！  
> *作品徵集中...*

---

## 📞 需要幫助？

### 🆘 常見問題
- [網站使用指南](./how-to-learn.html#faq)
- [Scratch 操作疑難排解](./resources/troubleshooting.html)
- [創意發想技巧](./resources/creativity-tips.html)

### 👨‍🏫 聯絡老師
如果遇到問題或有任何建議，歡迎聯絡：
- **LINE**: 私訊老師
- **課堂時間**: 直接向老師提問
- **同學互助**: 和班上同學一起討論

---

## 🎊 準備好了嗎？

讓我們一起踏上這段精彩的程式設計學習之旅！  
記住：每一個偉大的程式設計師都是從第一行程式碼開始的。

**守衛母雞已經就位，快來設計你的防守策略吧！** 🐔🛡️

---

<style>
.course-overview {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1rem;
  margin: 2rem 0;
}

.week-card {
  border: 2px solid #e1e4e8;
  border-radius: 8px;
  padding: 1.5rem;
  background: #f8f9fa;
  transition: transform 0.2s, box-shadow 0.2s;
}

.week-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.week-card.available {
  border-color: #28a745;
  background: #f8fff9;
}

.week-card.coming-soon {
  opacity: 0.7;
}

.week-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.week-number {
  font-weight: bold;
  font-size: 1.1rem;
  color: #6f42c1;
}

.status-badge {
  padding: 0.25rem 0.5rem;
  border-radius: 12px;
  font-size: 0.8rem;
  font-weight: bold;
}

.status-badge.available {
  background: #28a745;
  color: white;
}

.status-badge.coming-soon {
  background: #6c757d;
  color: white;
}

.week-card h3 {
  margin: 0 0 0.5rem 0;
  color: #24292e;
  font-size: 1.2rem;
}

.week-card p {
  margin: 0 0 1rem 0;
  color: #586069;
  line-height: 1.5;
}

.learn-btn {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: #0366d6;
  color: white;
  text-decoration: none;
  border-radius: 4px;
  border: none;
  cursor: pointer;
  font-size: 0.9rem;
  transition: background-color 0.2s;
}

.learn-btn:hover:not(.disabled) {
  background: #0256cc;
  text-decoration: none;
  color: white;
}

.learn-btn.disabled {
  background: #6c757d;
  cursor: not-allowed;
}

@media (max-width: 768px) {
  .course-overview {
    grid-template-columns: 1fr;
  }
}
</style>
