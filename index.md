---
layout: default
title: 首頁
nav_order: 1
---

# 🐣 Scratch 電子雞創客課程
{: .fs-9 }

歡迎來到充滿創意與樂趣的程式設計世界！在這裡，你將學會如何使用 Scratch 創造屬於自己的電子雞夥伴。
{: .fs-6 .fw-300 }

[開始學習](./how-to-learn.html){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [第一週課程](./week1/){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## 🎯 課程特色

### 🎮 寓教於樂的學習方式
透過大家喜愛的「電子雞」主題，讓程式設計變得生動有趣！

### 🧩 循序漸進的課程設計
從基礎介面認識到複雜的遊戲邏輯，每一週都有新的挑戰與收穫。

### 🤝 培養多元能力
不只學程式，更培養邏輯思維、創造力、問題解決和團隊合作能力。

### 🌟 展現個人創意
每個人的電子雞都是獨一無二的，發揮你的想像力創造專屬夥伴！

---

## 📚 課程概覽

<div class="course-overview">
{% for week in site.data.course_structure %}
<div class="week-card {% if week.status == 'available' %}available{% else %}coming-soon{% endif %}">
  <div class="week-header">
    <span class="week-number">第 {{ week.week }} 週</span>
    {% if week.status == 'available' %}
      <span class="status-badge available">開放學習</span>
    {% else %}
      <span class="status-badge coming-soon">建置中</span>
    {% endif %}
  </div>
  <h3>{{ week.title }}</h3>
  <p>{{ week.description }}</p>
  {% if week.status == 'available' %}
    <a href="./week{{ week.week }}/" class="learn-btn">開始學習</a>
  {% else %}
    <button class="learn-btn disabled" disabled>敬請期待</button>
  {% endif %}
</div>
{% endfor %}
</div>

---

## 🎯 學習目標

完成這個課程後，你將能夠：

- ✅ **熟練操作 Scratch**：掌握程式設計的基本概念和技能
- ✅ **創作電子雞遊戲**：具備完整的照護、互動和成長系統
- ✅ **培養邏輯思維**：學會分析問題和設計解決方案
- ✅ **展現創意能力**：設計獨特的角色和遊戲機制
- ✅ **建立合作精神**：與同學互相學習和幫助

---

## 🛠️ 需要準備什麼？

### 💻 基本設備
- 能上網的電腦或平板
- 正常運作的滑鼠（建議）
- 穩定的網路連線

### 🌐 軟體需求
- 任何現代瀏覽器（Chrome、Firefox、Safari、Edge）
- 免費的 Scratch 帳號（課程中會教你註冊）

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
4. **互相分享**：和同學分享作品，一起學習成長

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
- **Email**: {{ site.custom.contact.email }}
- **課堂時間**: 直接向老師提問
- **同學互助**: 和班上同學一起討論

---

## 🎊 準備好了嗎？

讓我們一起踏上這段精彩的程式設計學習之旅！  
記住：每一個偉大的程式設計師都是從第一行程式碼開始的。

**你的電子雞夥伴正在等待誕生，快來創造它吧！** 🐣✨

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