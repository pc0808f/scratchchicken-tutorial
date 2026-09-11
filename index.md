---
layout: default
title: 首頁
nav_order: 1
---

<div class="landing-page">
  <section class="hero-panel">
    <div class="hero-copy">
      <p class="eyebrow">SCRATCH CREATIVE CODING · 14 WEEK COURSE</p>
      <h1>母雞護衛隊<br><span>保衛飼料大作戰</span></h1>
      <p class="hero-lead">從雞舍裡的真實問題出發，帶孩子用 Scratch 做出一款自己的塔防遊戲。</p>
      <div class="hero-actions">
        <a href="#course-roadmap" class="hero-button primary">查看課程地圖 <span>→</span></a>
        <a href="./how-to-learn.html" class="hero-button ghost">如何開始</a>
      </div>
      <div class="hero-meta">
        <span><strong>14</strong> 週循序課程</span>
        <span><strong>45</strong> 分鐘有效實作</span>
        <span><strong>100%</strong> 觸控友善</span>
      </div>
    </div>
    <div class="hero-art" aria-label="守衛母雞保護飼料桶的塔防示意圖">
      <div class="art-grid"></div>
      <div class="feed-bucket">FEED<br><small>100</small></div>
      <div class="path-line"></div>
      <div class="tower tower-one"><span>✦</span></div>
      <div class="tower tower-two"><span>✦</span></div>
      <div class="mouse mouse-one">●</div>
      <div class="mouse mouse-two">●</div>
      <div class="art-label label-top">DEFEND<br><strong>THE FARM</strong></div>
      <div class="art-label label-bottom">WAVE 01 <span>●</span></div>
    </div>
  </section>

  <section class="trust-strip">
    <span>給國小四、五年級</span>
    <span>Scratch 3.0</span>
    <span>電腦與 iPad 都能操作</span>
    <span>每週完成一個可玩的成果</span>
  </section>

  <section class="story-section section-block">
    <div class="section-heading">
      <p class="eyebrow">WHY THIS COURSE</p>
      <h2>不是只學積木，<br><em>是把問題變成遊戲。</em></h2>
    </div>
    <div class="story-grid">
      <div class="story-intro">
        <p>雞舍真的有老鼠來偷飼料。孩子從觀察身邊的問題開始，設計守衛母雞、安排防守路線，再一步步把想法變成能玩的作品。</p>
        <p class="story-note">每週約 45 分鐘核心教學，保留時間給操作落差、個別協助與除錯。</p>
      </div>
      <div class="feature-card"><span class="feature-number">01</span><h3>任務式學習</h3><p>每週都有清楚任務，不會只做零散練習。</p></div>
      <div class="feature-card"><span class="feature-number">02</span><h3>看得見的成果</h3><p>從一隻母雞開始，最後完成自己的塔防遊戲。</p></div>
      <div class="feature-card"><span class="feature-number">03</span><h3>學會除錯</h3><p>用互測和實作找問題，培養真正的問題解決能力。</p></div>
    </div>
  </section>

  <section id="course-roadmap" class="roadmap-section section-block">
    <div class="section-heading split-heading">
      <div><p class="eyebrow">THE COURSE ROADMAP</p><h2>14 週，從角色到完整遊戲。</h2></div>
      <p>先做出能玩的核心版本，再逐步加入波次、金幣、商店與升級。</p>
    </div>
    <div class="course-overview">
      {% for course in site.data.course_structure %}
      <article class="week-card {{ course.status }}">
        <div class="week-topline"><span class="week-index">{{ course.week | prepend: '0' | slice: -2, 2 }}</span><span class="week-status">{% if course.status == "available" %}OPEN{% else %}SOON{% endif %}</span></div>
        <h3>{{ course.title }}</h3>
        <p>{{ course.description }}</p>
        {% if course.status == "available" %}
        <a href="./week{{ course.week }}/" class="week-link">進入課程 <span>→</span></a>
        {% else %}
        <span class="week-link muted">準備中</span>
        {% endif %}
      </article>
      {% endfor %}
    </div>
  </section>

  <section class="outcomes-section section-block">
    <div class="outcomes-card">
      <div><p class="eyebrow">BY THE END</p><h2>孩子會帶走什麼？</h2></div>
      <div class="outcome-list">
        <div><span>01</span><strong>Scratch 基礎</strong><p>角色、造型、背景與事件</p></div>
        <div><span>02</span><strong>程式邏輯</strong><p>條件、變數、廣播與分身</p></div>
        <div><span>03</span><strong>遊戲設計</strong><p>規則、平衡、測試與除錯</p></div>
        <div><span>04</span><strong>作品表達</strong><p>展示玩法並說明設計想法</p></div>
      </div>
    </div>
  </section>

  <section class="goals-section section-block">
    <div class="section-heading"><p class="eyebrow">WEEK BY WEEK</p><h2>每週都知道自己正在學什麼。</h2></div>
    <div class="goals-table-wrap">
      <table class="goals-table">
        <thead><tr><th>週次</th><th>學習目標</th><th>核心概念</th><th>作品成果</th></tr></thead>
        <tbody>
          <tr><td>01</td><td>加入 hen，修改守衛母雞</td><td>角色、造型</td><td>自己的守衛母雞</td></tr>
          <tr><td>02</td><td>補完介面與存檔，建立塔防背景與道路</td><td>背景、舞台、繪圖工具、存檔</td><td>老鼠洞、道路與飼料盒背景</td></tr>
          <tr><td>03</td><td>點擊固定砲位放置母雞</td><td>點擊、條件判斷</td><td>第一座守衛砲塔</td></tr>
          <tr><td>04</td><td>讓砲塔發射雞蛋</td><td>分身、碰撞</td><td>雞蛋擊中老鼠</td></tr>
          <tr><td>05</td><td>加入動畫與放置防呆</td><td>造型、座標判斷</td><td>更完整的砲塔</td></tr>
          <tr><td>06</td><td>建立老鼠生成器</td><td>分身、計時、隨機</td><td>兩種不同老鼠</td></tr>
          <tr><td>07</td><td>整合、測試並修正問題</td><td>整合、除錯</td><td>第一版可玩塔防</td></tr>
          <tr><td>08</td><td>控制一波又一波的進攻</td><td>變數、廣播、波次</td><td>波次系統</td></tr>
          <tr><td>09</td><td>讓防守需要花費資源</td><td>金幣、運算、比較</td><td>金幣經濟</td></tr>
          <tr><td>10</td><td>設計砲塔選擇介面</td><td>商店、按鈕、廣播</td><td>砲塔商店</td></tr>
          <tr><td>11</td><td>比較不同砲塔的特色</td><td>射速、射程、平衡</td><td>戰鬥雞砲塔</td></tr>
          <tr><td>12</td><td>管理每隻老鼠的血量</td><td>角色專屬變數、血條</td><td>血量與難度</td></tr>
          <tr><td>13</td><td>製作能攻擊多隻敵人的武器</td><td>範圍、多重判定</td><td>雷射母雞</td></tr>
          <tr><td>14</td><td>完成遊戲並發表作品</td><td>生命值、Game Over、升級</td><td>完整塔防作品</td></tr>
        </tbody>
      </table>
    </div>
  </section>

  <section class="final-cta section-block">
    <p class="eyebrow">READY TO DEFEND?</p>
    <h2>你的第一座砲塔，<br>現在開始。</h2>
    <a href="./how-to-learn.html" class="hero-button primary">了解學習方式 <span>→</span></a>
  </section>
</div>

<style>
.site-header { background: #17221e; border-top: 4px solid #d7f36b; border-bottom: 0; }
.site-header .wrapper { max-width: 1440px; padding-left: clamp(1.5rem, 7vw, 8rem); padding-right: clamp(1.5rem, 7vw, 8rem); }
.site-header .site-title, .site-header .page-link { color: #fff; }
.site-header .site-title { font-weight: 700; letter-spacing: -.03em; }
.site-header .page-link:hover { color: #d7f36b; text-decoration: none; }
.site-header .menu-icon > svg path { fill: #d7f36b; }
.page-content { padding: 0; }
.page-content > .wrapper { max-width: none; padding: 0; }
.landing-page { --ink: #17221e; --cream: #f5f1e8; --lime: #d7f36b; --orange: #ff704b; --muted: #68746d; color: var(--ink); margin: -1rem calc(50% - 50vw) 0; background: var(--cream); overflow: hidden; font-family: "Avenir Next", "Noto Sans TC", "Microsoft JhengHei", sans-serif; }
.landing-page * { box-sizing: border-box; }
.hero-panel { min-height: 620px; display: grid; grid-template-columns: minmax(0, 1fr) minmax(360px, .85fr); gap: 3rem; padding: 5.5rem clamp(1.5rem, 7vw, 8rem) 4rem; background: var(--ink); color: #fff; position: relative; }
.hero-panel:after { content: ""; position: absolute; inset: auto 0 0; height: 90px; background: var(--cream); clip-path: polygon(0 100%, 100% 0, 100% 100%); }
.hero-copy { max-width: 680px; position: relative; z-index: 1; }
.eyebrow { color: var(--orange); font-size: .72rem; letter-spacing: .18em; font-weight: 800; margin: 0 0 1.2rem; }
.hero-copy h1 { color: #fff; font-size: clamp(3rem, 6vw, 5.5rem); line-height: .98; letter-spacing: -.07em; margin: 0 0 1.6rem; }
.hero-copy h1 span { color: var(--lime); white-space: nowrap; }
.hero-lead { color: #c8d0c9; font-size: clamp(1rem, 1.6vw, 1.3rem); line-height: 1.8; max-width: 510px; margin-bottom: 2rem; }
.hero-actions { display: flex; flex-wrap: wrap; gap: .8rem; }
.hero-button { display: inline-flex; align-items: center; gap: 1rem; border-radius: 999px; padding: .9rem 1.4rem; font-weight: 800; text-decoration: none; transition: transform .2s, background .2s; }
.hero-button:hover { transform: translateY(-3px); text-decoration: none; }
.hero-button.primary { color: var(--ink); background: var(--lime); }
.hero-button.primary:hover { background: #e6ff8d; color: var(--ink); }
.hero-button.ghost { color: #fff; border: 1px solid #68746d; }
.hero-button.ghost:hover { color: #fff; border-color: #fff; }
.hero-meta { display: flex; flex-wrap: wrap; gap: 1.5rem; color: #91a198; font-size: .8rem; margin-top: 3rem; }
.hero-meta strong { color: #fff; font-size: 1.2rem; margin-right: .25rem; }
.hero-art { align-self: center; min-height: 390px; max-width: 490px; width: 100%; position: relative; border: 1px solid #44514a; background: #202d27; border-radius: 2rem; overflow: hidden; transform: rotate(2deg); box-shadow: 18px 20px 0 rgba(215,243,107,.16); }
.art-grid { position: absolute; inset: 0; opacity: .35; background-image: linear-gradient(#62736a 1px, transparent 1px), linear-gradient(90deg, #62736a 1px, transparent 1px); background-size: 42px 42px; }
.path-line { position: absolute; width: 68%; height: 80%; left: 15%; top: 12%; border: 12px solid #b49b72; border-left-color: transparent; border-radius: 48%; transform: rotate(-25deg); opacity: .9; }
.feed-bucket { position: absolute; right: 8%; top: 40%; border: 3px solid var(--lime); color: var(--lime); border-radius: .4rem; padding: .55rem .8rem; font-size: .68rem; line-height: 1.1; font-weight: 900; text-align: center; transform: rotate(-8deg); }
.feed-bucket small { font-size: 1rem; }
.tower { position: absolute; width: 58px; height: 58px; border: 4px solid var(--lime); background: var(--ink); border-radius: 50%; display: grid; place-items: center; color: var(--lime); font-size: 1.3rem; box-shadow: 0 0 0 8px rgba(215,243,107,.12); }
.tower-one { left: 25%; top: 28%; }.tower-two { left: 58%; bottom: 17%; }
.mouse { position: absolute; color: var(--orange); font-size: 2.2rem; text-shadow: 0 0 14px var(--orange); }.mouse-one { left: 19%; bottom: 25%; }.mouse-two { left: 42%; top: 21%; font-size: 1.4rem; }
.art-label { position: absolute; color: #9baa9f; font-size: .65rem; letter-spacing: .15em; font-weight: 800; }.label-top { left: 1.5rem; top: 1.5rem; }.label-top strong { color: #fff; font-size: .9rem; }.label-bottom { right: 1.5rem; bottom: 1.5rem; }.label-bottom span { color: var(--orange); }
.trust-strip { display: flex; justify-content: space-around; flex-wrap: wrap; gap: 1rem; padding: 1.3rem clamp(1.5rem, 7vw, 8rem); color: var(--muted); background: var(--cream); font-size: .75rem; font-weight: 800; letter-spacing: .04em; }
.section-block { padding: 5rem clamp(1.5rem, 7vw, 8rem); max-width: 1440px; margin: auto; }
.section-heading h2, .final-cta h2 { color: var(--ink); font-size: clamp(2rem, 4vw, 4rem); line-height: 1.05; letter-spacing: -.06em; margin: 0; }.section-heading h2 em { color: var(--orange); font-style: normal; }.section-heading { margin-bottom: 2.5rem; }
.story-grid { display: grid; grid-template-columns: 1.4fr repeat(3, 1fr); gap: 1rem; }.story-intro { padding: 1rem 2rem 1rem 0; color: var(--muted); line-height: 1.8; }.story-note { color: var(--ink); border-left: 3px solid var(--orange); padding-left: 1rem; font-size: .9rem; }.feature-card { min-height: 220px; padding: 1.5rem; border-top: 4px solid var(--ink); background: #fff; }.feature-number { color: var(--orange); font-size: .75rem; font-weight: 900; }.feature-card h3 { margin: 3.5rem 0 .5rem; color: var(--ink); }.feature-card p { color: var(--muted); font-size: .9rem; line-height: 1.6; margin: 0; }
.roadmap-section { background: #e3e9d4; max-width: none; }.split-heading { display: flex; justify-content: space-between; align-items: end; gap: 2rem; }.split-heading > p { max-width: 330px; color: var(--muted); line-height: 1.7; margin: 0; }.course-overview { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1rem; }.week-card { min-height: 230px; padding: 1.4rem; background: #fff; border-radius: 1rem; display: flex; flex-direction: column; border: 1px solid transparent; }.week-card.available { border-color: var(--orange); box-shadow: 7px 7px 0 var(--orange); }.week-card.coming_soon { opacity: .68; }.week-topline { display: flex; justify-content: space-between; align-items: center; }.week-index { color: var(--orange); font-size: 1.5rem; font-weight: 900; }.week-status { font-size: .62rem; letter-spacing: .12em; font-weight: 900; color: var(--muted); }.week-card h3 { color: var(--ink); font-size: 1.1rem; line-height: 1.3; margin: 1.8rem 0 .6rem; }.week-card p { color: var(--muted); font-size: .85rem; line-height: 1.5; margin: 0; }.week-link { color: var(--ink); font-size: .8rem; font-weight: 900; margin-top: auto; padding-top: 1rem; }.week-link span { color: var(--orange); font-size: 1.2rem; }.week-link:hover { color: var(--orange); text-decoration: none; }.week-link.muted { color: #aab1a7; }
.outcomes-section { background: var(--cream); }.outcomes-card { display: grid; grid-template-columns: .8fr 1.6fr; gap: 3rem; background: var(--ink); color: #fff; border-radius: 1.5rem; padding: clamp(2rem, 5vw, 4rem); }.outcomes-card h2 { color: #fff; margin: 0; font-size: clamp(2rem, 4vw, 3.5rem); letter-spacing: -.06em; }.outcome-list { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.5rem; }.outcome-list div { border-top: 1px solid #536158; padding-top: 1rem; }.outcome-list span { color: var(--lime); font-size: .7rem; font-weight: 900; }.outcome-list strong { display: block; font-size: 1.1rem; margin: .7rem 0 .3rem; }.outcome-list p { color: #aebbb2; font-size: .85rem; margin: 0; }
.goals-section { background: #fff; }.goals-table-wrap { overflow-x: auto; }.goals-table { width: 100%; min-width: 720px; border-collapse: collapse; font-size: .86rem; }.goals-table th { background: var(--ink); color: var(--lime); text-align: left; padding: 1rem; font-size: .72rem; letter-spacing: .08em; }.goals-table td { border-bottom: 1px solid #e5e9e3; padding: 1rem; color: var(--muted); }.goals-table td:first-child { color: var(--orange); font-weight: 900; }.goals-table tr:hover td { background: #f7f9f2; }
.final-cta { text-align: center; background: var(--lime); max-width: none; padding-top: 6rem; padding-bottom: 6rem; }.final-cta .eyebrow { color: var(--ink); }.final-cta h2 { margin-bottom: 2rem; }.final-cta .hero-button { background: var(--ink); color: #fff; }.final-cta .hero-button:hover { color: var(--lime); }
@media (max-width: 1050px) { .hero-panel { grid-template-columns: 1fr; }.hero-art { margin: 0 auto; }.story-grid { grid-template-columns: repeat(2, 1fr); }.story-intro { grid-column: span 2; }.course-overview { grid-template-columns: repeat(3, 1fr); }.outcomes-card { grid-template-columns: 1fr; } }
@media (max-width: 650px) { .hero-panel { min-height: auto; padding-top: 3.5rem; }.hero-copy h1 { font-size: 3.5rem; }.hero-copy h1 span { white-space: normal; }.hero-art { min-height: 300px; transform: none; }.hero-meta { gap: .8rem; }.trust-strip { justify-content: flex-start; }.section-block { padding-top: 3.5rem; padding-bottom: 3.5rem; }.story-grid, .outcome-list { grid-template-columns: 1fr; }.story-intro { grid-column: auto; padding: 0; }.feature-card { min-height: 180px; }.feature-card h3 { margin-top: 2rem; }.split-heading { display: block; }.split-heading > p { margin-top: 1rem; }.course-overview { grid-template-columns: repeat(2, 1fr); }.week-card { min-height: 210px; padding: 1rem; }.week-card h3 { font-size: .95rem; margin-top: 1rem; }.outcomes-card { padding: 1.5rem; }.outcome-list { gap: 1rem; } }
</style>
