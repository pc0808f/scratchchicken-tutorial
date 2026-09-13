---
layout: default
title: 第四週：老鼠上路②：轉彎與抵達
nav_order: 6
has_children: true
---

<div class="ebook-course week-four-book">
  <div class="ebook-toolbar"><strong>Scratch 母雞護衛隊</strong><span>第四週：老鼠上路②轉彎與抵達</span><span>A4 教材預覽</span></div>
  <main class="book-spread">
    <section class="book-page cover-page"><div class="page-kicker">SCRATCH CREATIVE CODING</div><div class="cover-number">04</div><div class="cover-art">➤</div><h1>轉彎<br><em>走完！</em></h1><p class="cover-subtitle">第四週學習單・轉彎與抵達</p><div class="cover-rule"></div><p class="cover-description">用老鼠身上的紅藍標壓在路線上判斷方向，讓老鼠在轉角轉彎、走完整條路，最後抵達飼料桶。</p><div class="cover-footer"><span>母雞護衛隊・保衛飼料大作戰</span><span>01</span></div></section>

    <section class="book-page content-page"><div class="page-header"><span>WEEK 04</span><span>學習目標</span></div><h2>今天要完成什麼？</h2><p class="lead">上週老鼠已經會「直線前進」。這週要讓牠學會<strong>轉彎</strong>：靠老鼠身上的紅藍標壓到路線來修正方向，走完整條彎路，最後抵達飼料桶消失。</p><div class="goal-box"><span>CORE MISSION</span><strong>讓老鼠轉彎走完全程</strong><p>老鼠沿著路前進，在轉角用紅藍判斷轉彎，最後抵達飼料桶。</p></div><h3>本週學習目標</h3><ul class="check-list"><li>了解老鼠怎麼「知道自己壓在路上」</li><li>藍標壓到路線就往右修正方向</li><li>紅標壓到路線就往左修正方向</li><li>調整移動與轉彎數值，避免老鼠飛出道路</li><li>讓老鼠抵達飼料桶時消失</li></ul><div class="note-box"><strong>本週完成標準：</strong>按綠旗後，老鼠能從起點出發、在轉角正確轉彎、走完整條路並抵達飼料桶消失。若 45 分鐘不夠，改用老師準備好的起始檔接續，不刪掉紅藍判斷。</div><div class="page-footer"><span>Scratch 母雞護衛隊</span><span>02</span></div></section>

    <section class="book-page content-page"><div class="page-header"><span>STEP 01</span><span>位置判斷原理</span></div><h2>老鼠怎麼知道自己在路上？</h2><p class="lead">轉彎的關鍵，是讓老鼠隨時知道自己「有沒有壓在路線上」。先理解這個原理，後面的紅藍判斷才看得懂。</p><div class="image-grid three"><div><img src="{{ '/week4/resources/collision/調整藍紅老鼠位置1-壓到線.jpg' | relative_url }}" alt="老鼠壓到路線"><span>壓到路線</span></div><div><img src="{{ '/week4/resources/collision/調整藍紅老鼠位置2-沒壓到線.jpg' | relative_url }}" alt="老鼠沒有壓到路線"><span>沒壓到路線</span></div><div><img src="{{ '/week4/resources/collision/調整藍紅老鼠位置3-用目前位置做為老鼠的開始位置.jpg' | relative_url }}" alt="使用目前位置作為起點"><span>用目前位置設起點</span></div></div><div class="teacher-note"><strong>概念：</strong>老鼠前面有一紅一藍兩個標（像感應器）。程式看哪個標壓到路線（就是 W3 做的路徑角色，畫面上預設叫 Sprite1）：藍標壓到就往右修正、紅標壓到就往左修正，老鼠就會一直沿著路走。</div><div class="page-footer"><span>第四週・位置判斷</span><span>03</span></div></section>

    <section class="book-page content-page"><div class="page-header"><span>STEP 02</span><span>藍標判斷</span></div><h2>藍標壓到路線就往右修正</h2><p class="lead">在 mousemove 裡切換到藍框造型，加入判斷：如果藍標壓到路線（路徑角色）就向右轉一點點。這是老鼠第一個會自己修正方向的地方。</p><div class="large-process"><div><img src="{{ '/week4/resources/collision/調整藍紅老鼠位置8-換到藍框造型.jpg' | relative_url }}" alt="切換藍框造型"><span>01 換到藍框造型</span></div><div><img src="{{ '/week4/resources/collision/調整藍紅老鼠位置9-加上是否有撞到藍色的判斷和處理.jpg' | relative_url }}" alt="藍標壓到路線的判斷"><span>02 加入藍標判斷</span></div></div><div class="code-card"><div class="code-title">MOUSEMOVE / BLUE</div><div class="flow-layout"><div class="flow-panel"><strong>藍標轉彎流程</strong><div class="flow-node flow-motion">移動 10 點</div><div class="flow-arrow" aria-hidden="true">↓</div><div class="flow-node flow-definition">造型換成 藍框</div><div class="flow-arrow" aria-hidden="true">↓</div><div class="flow-node flow-condition">如果藍標碰到路徑角色</div><div class="flow-arrow" aria-hidden="true">↓</div><div class="flow-node flow-action">向右轉一點點</div></div></div><p class="flow-caption">藍框是老鼠身上的感應器；藍標壓到路線時，老鼠向右修正方向。</p></div><div class="page-footer"><span>第四週・藍標判斷</span><span>04</span></div></section>

    <section class="book-page content-page"><div class="page-header"><span>STEP 03</span><span>紅標判斷</span></div><h2>紅標壓到路線就往左修正</h2><p class="lead">用同樣的方法檢查紅標：切換到紅框造型後，如果紅標壓到路線就向左轉（和藍標相反方向），老鼠在不同轉角都能走對方向。</p><div class="large-process"><div><img src="{{ '/week4/resources/collision/調整藍紅老鼠位置10-加上是否有撞到紅色的判斷和處理.jpg' | relative_url }}" alt="紅標壓到路線的判斷"><span>01 加入紅標判斷</span></div></div><div class="code-card"><div class="code-title">MOUSEMOVE / RED</div><div class="flow-layout"><div class="flow-panel"><strong>紅標轉彎流程</strong><div class="flow-node flow-definition">造型換成 紅框</div><div class="flow-arrow" aria-hidden="true">↓</div><div class="flow-node flow-condition">如果紅標碰到路徑角色</div><div class="flow-arrow" aria-hidden="true">↓</div><div class="flow-node flow-action">向左轉一點點</div></div></div><p class="flow-caption">紅框是老鼠身上的感應器；紅標壓到路線時，老鼠向左修正方向。</p></div><div class="teacher-note"><strong>提醒：</strong>藍標往右、紅標往左，方向相反，老鼠才能沿著彎路一直修正著走。</div><div class="page-footer"><span>第四週・紅標判斷</span><span>05</span></div></section>

    <section class="book-page content-page"><div class="page-header"><span>STEP 04</span><span>調整數值</span></div><h2>不要讓老鼠飛出路線</h2><p class="lead">老鼠常常會衝太快飛出路線。這時不要重寫程式，只要調整「移動幾點」和「轉幾度」這些數字，慢慢試到剛好。</p><div class="large-process"><div><img src="{{ '/week4/resources/collision/調整藍紅老鼠位置11-如果會飛出去可以改變這些數字.jpg' | relative_url }}" alt="調整老鼠移動數值"><span>調整移動與轉彎數值</span></div></div><div class="teacher-note"><strong>除錯重點：</strong>一次只改一個數字、按綠旗看結果，再決定要調大還是調小——這就是「用測試找答案」，不是亂試。</div><div class="page-footer"><span>第四週・調整數值</span><span>06</span></div></section>

    <section class="book-page content-page"><div class="page-header"><span>STEP 05</span><span>抵達終點</span></div><h2>抵達飼料桶就消失</h2><p class="lead">老鼠走到飼料桶時要消失，代表牠「走完路線」了。加入一個判斷：碰到飼料桶就隱藏。</p><div class="code-card"><div class="code-title">MOUSE / ARRIVE</div><div class="flow-layout"><div class="flow-panel"><strong>抵達終點流程</strong><div class="flow-node flow-condition">碰到飼料桶嗎？</div><div class="flow-arrow" aria-hidden="true">↓</div><div class="flow-node flow-action">隱藏老鼠</div></div></div><p class="flow-caption">W4 先用「隱藏」表示老鼠完成路線；之後改成分身時，再改為刪除分身。</p></div><div class="mini-check"><strong>完成標準</strong><span>按綠旗 → 老鼠出發 → 沿路轉彎 → 抵達飼料桶 → 消失</span></div><div class="page-footer"><span>第四週・抵達終點</span><span>07</span></div></section>

    <section class="book-page content-page"><div class="page-header"><span>PLUS</span><span>加分挑戰</span></div><h2>自己畫一條新路線</h2><p class="lead">這是給已經完成基本任務的同學的加分挑戰，<strong>不是全班必做</strong>。</p><div class="missing-box"><span>CHALLENGE</span><h3>改背景＝換地圖</h3><p>因為老鼠是靠身上的紅藍標壓路線才轉彎，只要回到背景重畫一條新路線、並把路徑角色一起更新，老鼠就會走你設計的新路！記得新路線的起點要和老鼠的出發位置一致。</p></div><div class="teacher-note"><strong>差異化：</strong>程度快的同學挑戰自己畫路線；時間不足的同學用老師的固定路線即可，不強迫。</div><div class="page-footer"><span>第四週・加分挑戰</span><span>08</span></div></section>

    <section class="book-page content-page final-page"><div class="page-header"><span>CHECKPOINT</span><span>下課前檢查</span></div><h2>老鼠走完整條路了！</h2><div class="print-checklist"><label><input type="checkbox"> 我知道老鼠靠身上的紅藍標壓路線判斷方向</label><label><input type="checkbox"> 藍標壓到路線會往右修正</label><label><input type="checkbox"> 紅標壓到路線會往左修正</label><label><input type="checkbox"> 調好數值，老鼠不會飛出路線</label><label><input type="checkbox"> 老鼠抵達飼料桶會消失</label></div><div class="next-page-box"><span>NEXT WEEK</span><h3>母雞就位！免費放置砲塔</h3><p>下週在道路旁安排固定砲位，點擊空砲位就放上守衛母雞（這週先不用花錢）。</p></div><div class="page-footer"><span>母雞護衛隊・第四週</span><span>09</span></div></section>
  </main>
</div>

<style>
.site-header{background:#fff;border-top:4px solid #17221e;border-bottom:1px solid #d9ded7}.site-header .site-title,.site-header .page-link{color:#17221e}.site-header .page-link:hover{color:#ff704b;text-decoration:none}.page-content{padding:0}.page-content>.wrapper{max-width:none;padding:0}.ebook-course{--ink:#17221e;--paper:#fff;--cream:#e8ebe6;--lime:#d7f36b;--orange:#ff704b;background:var(--cream);padding:2.5rem 1.5rem 5rem;color:var(--ink);font-family:"Noto Sans TC","Microsoft JhengHei",sans-serif}.ebook-toolbar{max-width:210mm;margin:0 auto 1.2rem;display:flex;justify-content:space-between;gap:1rem;color:#657169;font-size:.75rem}.book-spread{max-width:210mm;margin:auto}.book-page{width:210mm;max-width:100%;min-height:297mm;margin:0 auto 1.5rem;background:var(--paper);padding:16mm 14mm 14mm;position:relative;box-shadow:0 4px 18px rgba(23,34,30,.13);break-after:page}.cover-page{background:var(--ink);color:#fff;overflow:hidden}.page-kicker,.page-header,.cover-footer{font-size:8pt;letter-spacing:.16em;font-weight:900}.page-kicker{color:var(--orange)}.cover-number{font-size:70pt;color:var(--lime);font-weight:900;line-height:1;margin-top:18mm}.cover-art{position:absolute;right:18mm;top:32mm;color:var(--lime);font-size:85pt}.cover-page h1{color:#fff;font-size:35pt;letter-spacing:-.09em;line-height:.95;margin:48mm 0 4mm}.cover-page h1 em{color:var(--lime);font-style:normal}.cover-subtitle{color:#b8c3ba}.cover-rule{height:3px;background:var(--orange);width:24mm;margin:15mm 0 7mm}.cover-description{color:#b8c3ba;font-size:10pt;line-height:1.8;max-width:65mm}.cover-footer{position:absolute;bottom:10mm;left:14mm;right:14mm;display:flex;justify-content:space-between;color:#93a096}.page-header{display:flex;justify-content:space-between;color:#758078;border-bottom:1px solid #d9ded7;padding-bottom:4mm}.content-page h2{font-size:25pt;letter-spacing:-.07em;line-height:1.1;margin:12mm 0 5mm}.lead{font-size:10.5pt;line-height:1.8;color:#536158}.goal-box{background:#eaf3c9;border-left:5px solid var(--lime);padding:6mm;margin:10mm 0}.goal-box span,.next-page-box span,.missing-box span{display:block;color:#63703c;font-size:8pt;letter-spacing:.16em;font-weight:900}.goal-box strong{display:block;font-size:17pt;margin:2mm 0}.goal-box p,.next-page-box p,.missing-box p{font-size:9.5pt;line-height:1.6;margin:0}.check-list{list-style:none;padding:0}.check-list li{padding:3mm 0;border-bottom:1px solid #e5e8e3;font-size:10pt}.check-list li:before{content:"✓";color:var(--orange);font-weight:900;margin-right:3mm}.note-box,.teacher-note{margin-top:12mm;border:1px solid #cbd3cb;padding:4mm;font-size:9pt;line-height:1.7}.image-grid{display:grid;gap:3mm;margin-top:8mm}.image-grid.six{grid-template-columns:repeat(3,1fr)}.image-grid.three{grid-template-columns:repeat(3,1fr)}.image-grid.four{grid-template-columns:repeat(2,1fr)}.image-grid div{border:1px solid #cbd3cb;background:#f7f8f5;padding:2mm}.image-grid img{display:block;width:100%;height:28mm;object-fit:contain}.image-grid span{display:block;margin-top:2mm;font-size:7.5pt;color:#536158}.code-card{border:1px solid #cbd3cb;margin:9mm 0;padding:5mm}.code-title{font-size:8pt;letter-spacing:.15em;font-weight:900;color:#758078;margin-bottom:4mm}.code-block{display:grid;gap:2mm}.code-block span{padding:3mm 4mm;border-radius:2mm;font-size:9pt;font-weight:700}.event-block{background:#ffbf3f}.motion-block{background:#5cb8ed}.looks-block{background:#9f79db;color:#fff}.numbered-step{display:flex;gap:4mm;padding:3mm 0;border-bottom:1px solid #e5e8e3}.numbered-step span{width:8mm;height:8mm;border-radius:50%;background:var(--ink);color:var(--lime);display:grid;place-items:center;font-size:8pt;font-weight:900;flex:none}.numbered-step p{margin:1mm 0;font-size:9.5pt}.mini-check{margin-top:10mm;padding:5mm;background:var(--ink);color:#fff}.mini-check strong,.mini-check span{display:block}.mini-check strong{color:var(--lime);font-size:8pt;letter-spacing:.15em}.mini-check span{margin-top:2mm;font-size:10pt}.print-checklist{display:grid;gap:4mm;margin:10mm 0}.print-checklist label{border:1px solid #cbd3cb;padding:5mm;font-size:10pt}.print-checklist input{width:5mm;height:5mm;margin-right:3mm}.missing-box{border:2px dashed var(--orange);padding:6mm;margin:12mm 0}.missing-box h3,.next-page-box h3{font-size:19pt;margin:2mm 0}.next-page-box{background:#eaf3c9;padding:6mm}.page-footer{position:absolute;bottom:8mm;left:14mm;right:14mm;border-top:1px solid #d9ded7;padding-top:3mm;display:flex;justify-content:space-between;color:#758078;font-size:8pt}.route-steps{display:none}@media(max-width:600px){.ebook-course{padding:1rem .75rem 3rem}.ebook-toolbar{font-size:.65rem}.image-grid.six,.image-grid.three,.image-grid.four{grid-template-columns:1fr 1fr}}@media print{@page{size:A4;margin:0}.site-header,.site-footer,.ebook-toolbar{display:none!important}.page-content,.page-content>.wrapper{padding:0!important}.ebook-course{padding:0;background:#fff}.book-page{width:210mm;height:297mm;min-height:297mm;box-shadow:none;margin:0;padding:16mm 15mm 14mm;break-after:page;overflow:hidden}.book-page:last-child{break-after:auto}.cover-page,.mini-check{-webkit-print-color-adjust:exact;print-color-adjust:exact}.image-grid,.code-card,.missing-box{break-inside:avoid}}
.final-image{margin:8mm 0;border:1px solid #cbd3cb;background:#f7f8f5;padding:3mm}.final-image img{display:block;width:100%;height:60mm;object-fit:contain}.final-image span{display:block;margin-top:2mm;color:#536158;font-size:8pt}
.large-process{display:grid;grid-template-columns:1fr;gap:5mm;margin-top:8mm}.large-process div{border:1px solid #cbd3cb;background:#f7f8f5;padding:3mm}.large-process img{display:block;width:100%;height:68mm;object-fit:contain}.large-process span{display:block;margin-top:2mm;color:#536158;font-size:10pt;font-weight:700}.image-grid span{font-size:10pt;font-weight:700}
.collision-grid{display:grid;grid-template-columns:1fr 1fr;gap:5mm;margin-top:8mm}.collision-grid div{border:1px solid #cbd3cb;background:#f7f8f5;padding:3mm}.collision-grid img{display:block;width:100%;height:48mm;object-fit:contain}.collision-grid span{display:block;margin-top:2mm;color:#536158;font-size:9pt;font-weight:700}.collision-appendix h2{font-size:22pt}

/* W4 typography: 16px is the minimum readable size on every page. */
.week-four-book{--text-min:16px;--text-body:18px;--text-emphasis:20px;--text-subheading:22px;--text-heading:32px;font-size:var(--text-body)}
.week-four-book .ebook-toolbar,
.week-four-book .page-kicker,
.week-four-book .page-header,
.week-four-book .cover-footer,
.week-four-book .page-footer{font-size:var(--text-min)}
.week-four-book .cover-description,
.week-four-book .lead,
.week-four-book .goal-box,
.week-four-book .check-list,
.week-four-book .note-box,
.week-four-book .teacher-note,
.week-four-book .code-card,
.week-four-book .code-title,
.week-four-book .code-block,
.week-four-book .mini-check,
.week-four-book .next-page-box,
.week-four-book .print-checklist,
.week-four-book .final-image span{font-size:var(--text-body);line-height:1.7}
.week-four-book .content-page h2{font-size:var(--text-heading)}
.week-four-book .content-page h3,
.week-four-book .goal-box strong,
.week-four-book .next-page-box h3{font-size:var(--text-subheading)}
.week-four-book .check-list li{font-size:var(--text-body);line-height:1.8;margin-bottom:3mm}
.week-four-book .large-process span,
.week-four-book .collision-grid span,
.week-four-book .image-grid span{font-size:var(--text-emphasis)}
.week-four-book .code-title{font-weight:700;letter-spacing:.04em}
.week-four-book .code-block span{font-size:var(--text-body);line-height:1.8}
.week-four-book .print-checklist label{font-size:var(--text-body);line-height:1.8}
.week-four-book .flow-layout{display:grid;grid-template-columns:1fr;gap:5mm;margin-top:5mm}
.week-four-book .flow-panel{padding:5mm;border:2px solid #cbd3cb;background:#f7f8f5;border-radius:3mm}
.week-four-book .flow-panel>strong{display:block;margin-bottom:4mm;font-size:var(--text-emphasis);color:var(--ink)}
.week-four-book .flow-node{padding:4mm 3mm;border-radius:2mm;text-align:center;font-size:var(--text-body);font-weight:700;line-height:1.35}
.week-four-book .flow-motion{background:#dcecff;border:2px solid #6b9bd2}
.week-four-book .flow-definition{background:#ffb3a5;border:2px solid #d75843}
.week-four-book .flow-condition{background:#f0ddff;border:2px solid #9a65c4}
.week-four-book .flow-action{background:#d9f0b5;border:2px solid #78a848}
.week-four-book .flow-arrow{text-align:center;color:#536158;font-size:24px;font-weight:900;line-height:1.1;padding:1mm 0}
.week-four-book .flow-caption{margin:5mm 0 0;color:#536158;font-size:var(--text-min);line-height:1.6}
</style>
