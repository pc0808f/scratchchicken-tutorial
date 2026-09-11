# Fuelvin 塔防教學系列摘要

來源播放清單：

<https://www.youtube.com/playlist?list=PLYXukbXFJeKtr_EFxDK0Ofa7OoR4kjjWa>

系列名稱：**(COMPLETE) How to Make a Tower Defense Game in Scratch**

資料來源：YouTube 播放清單 RSS 與各集公開影片描述。播放清單目前包含 12 集正篇與 1 集 Bonus。

## 全系列目錄

| 集數 | 影片 | 核心內容 | 可教概念 |
|---|---|---|---|
| Part 1 | [影片](https://www.youtube.com/watch?v=emaXCb2pXWY) | 建立第一批敵人與路徑追蹤系統 | 路徑角色、顏色判斷、速度、方向、老鼠移動 |
| Part 2 | [影片](https://www.youtube.com/watch?v=myAD68X-BfQ) | 建立第一座可放置的砲塔，並建立追蹤敵人的清單 | 固定／可放置砲塔、清單、敵人追蹤 |
| Part 3 | [影片](https://www.youtube.com/watch?v=mBU0tsl3zBg) | 讓砲塔瞄準範圍內的敵人、發射攻擊，加入敵人死亡動畫 | 範圍判定、瞄準、攻擊、死亡動畫 |
| Part 4 | [影片](https://www.youtube.com/watch?v=iUsbxTBRDI4) | 加入砲塔底座與開火動畫，禁止放在道路或其他砲塔上 | 造型切換、條件判斷、放置防呆 |
| Part 5 | [影片](https://www.youtube.com/watch?v=u0mSlMwsi7k) | 建立砲塔選擇系統、敵人生成器與新敵人種類 | 選擇系統、分身生成、新敵人 |
| Part 6 | [影片](https://www.youtube.com/watch?v=lbShUrHWzfA) | 建立波次系統、開始波次按鈕、波次計數與砲塔改良 | 變數、廣播、波次、計時 |
| Part 7 | [影片](https://www.youtube.com/watch?v=hEp1Uxk8nNI) | 修正砲塔放置問題，加入金幣系統與砲塔價格 | 金幣、比較、購買條件、扣款 |
| Part 8 | [影片](https://www.youtube.com/watch?v=CBukKYZBtWQ) | 建立完整的砲塔商店 | 商店介面、砲塔選擇、價格 |
| Part 9 | [影片](https://www.youtube.com/watch?v=a1DvsRdgOKA) | 建立射速更快、攻擊範圍不同的新砲塔 | 複製系統、射速、射程、平衡 |
| Part 10 | [影片](https://www.youtube.com/watch?v=qSrSuaPu4_0) | 建立敵人血條，加入更多敵人與波次 | 角色專屬變數、血量、血條、難度 |
| Part 11 | [影片](https://www.youtube.com/watch?v=zyjZwQNpScw) | 建立可同時傷害多個敵人的雷射砲塔 | 範圍攻擊、多重判定、雷射 |
| Part 12 (FINAL) | [影片](https://www.youtube.com/watch?v=v1idXslMb6w) | 加入玩家生命值、Game Over、取消購買圖示、圖層系統與放置／購買 bug 修正 | 生命值、遊戲狀態、停止、重設、除錯 |
| Part 13 (BONUS) | [影片](https://www.youtube.com/watch?v=WqVpJkz_RH4) | 砲塔升級系統、三條升級路線與出售砲塔 | 升級、分支選擇、出售、進階變數 |

## Part 1 流程重點

Part 1 是目前第 3～7 週敵人系統的主要參考來源，流程不可跳過：

1. 先讓一隻老鼠沿著路徑前進。
2. 建立速度與方向參數。
3. 使用紅／藍路徑判斷老鼠轉彎。
4. 調整數值，避免老鼠飛出道路。
5. 判斷老鼠抵達終點或離開路徑。
6. 讓老鼠消失或廣播到達訊息。
7. 將單隻老鼠改成分身生成。
8. 設定每隔一段時間產生一隻老鼠。

## 與目前課程的初步對照

這張表是功能對照，不是最後的週次決定；每週仍需依 45 分鐘有效教學時間拆分。

| 課程週次 | 課程階段 | 主要影片來源 |
|---|---|---|
| 第 1 週 | Scratch 入門、hen、角色改色 | 無，課程導入 |
| 第 2 週 | 介面、存檔、草地、道路、老鼠洞、飼料盒 | 無，遊戲場景準備 |
| 第 3 週 | 路徑角色、老鼠造型、起點、速度、方向、轉彎 | Part 1 |
| 第 4 週 | 老鼠抵達終點、消失、到達事件 | Part 1 |
| 第 5 週 | 老鼠分身、生成間隔、敵人初始化 | Part 1、Part 5 |
| 第 6 週 | 固定砲位與第一座可放置砲塔 | Part 2 |
| 第 7 週 | 砲塔瞄準、雞蛋攻擊、老鼠死亡 | Part 3 |
| 第 8 週 | 砲塔美化與道路／重疊防呆 | Part 4 |
| 第 9 週 | 整合與第一版可玩遊戲 | Part 1～4 |
| 第 10 週 | 波次、開始波次、波次計數 | Part 6 |
| 第 11 週 | 金幣與砲塔購買 | Part 7 |
| 第 12 週 | 砲塔商店與第二種砲塔 | Part 8、Part 9 |
| 第 13 週 | 血條、更多敵人、雷射砲塔 | Part 10、Part 11 |
| 第 14 週 | 生命值、Game Over、升級、成果發表 | Part 12、Part 13 |

## 尚待確認的教學細節

- Part 1 內部各功能的精確時間點，需實際觀看影片後再拆成課堂步驟。
- Part 2 的清單系統是否要完整教給四、五年級學生，需決定是否改用簡化版固定砲位。
- Part 5 的敵人生成器與 Part 1 的分身生成，需確認哪些程式可以合併教學。
- Part 12 的圖層系統、取消購買圖示與 bug 修正，建議只挑必要部分。
- Part 13 三路線升級樹不適合直接照搬，課程可簡化成單一路線升級。
