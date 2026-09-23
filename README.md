# 📺 第四台去哪了？台灣有線電視近五年訂戶變化分析

> Cable TV｜MOD｜OTT Taiwan Market Analysis

<img width="1280" height="720" alt="project-cover" src="https://github.com/user-attachments/assets/098e4a82-b9f8-457b-9f88-f10b16e2ea28" />

## 🔗 Project Links｜專題連結

- 📊 **Power BI Interactive Dashboard：** [View Dashboard](https://app.powerbi.com/view?r=eyJrIjoiOWRiNjc2OTYtODVhMS00YmNiLThiZTgtNmQ0NjBiYWFjZDQ3IiwidCI6IjcwODk3ZDZmLTBhNDgtNDlkZS04ODBmLTI3ZDhhZDQ1ZDc2ZSIsImMiOjEwfQ%3D%3D)

本專題以台灣有線電視市場為主題，整理 111Q1～115Q2 公開資料，
觀察第四台訂戶與市場占有率的變化，並與 MOD 同期趨勢進行比較，
再透過 OTT 消費者調查，進一步了解台灣觀眾的收視習慣是否正在改變。

---

## 📌 Project Overview｜研究背景

過去家庭收看電視，多半以「第四台」為主要選擇。

但近年 MOD、Netflix、YouTube 等影音服務逐漸普及，
觀眾的影音選擇變得更加多元，也讓我產生一個問題：

**「第四台真的正在被其他影音服務取代嗎？」**

因此，本專題從有線電視訂戶變化出發，
進一步加入 MOD 與 OTT 資料，希望從數據觀察台灣電視市場近年的變化。

---

## ❓ Business Questions｜分析問題

本專題主要希望回答三個問題：

1. 台灣第四台訂戶是否持續流失？
2. MOD 是否承接了流失的第四台用戶？
3. OTT 的使用情況是否反映觀眾收視習慣正在改變？

---

## 🗂️ Data Source｜資料來源

### 有線電視
- 資料期間：111Q1～115Q2
- 資料內容：訂戶數、占有率、縣市、經營區等
- 資料來源：NCC 公開資料

### MOD
- 資料期間：111Q1～115Q2
- 資料內容：累計訂戶數
- 資料來源：NCC 公開資料

### OTT
- 資料期間：114年
- 資料內容：OTT 平台使用比例、年齡層及使用原因
- 資料來源：NCC 傳播內容消費行為調查

> OTT 資料為消費者調查比例，與有線電視及 MOD 的訂戶數資料性質不同，
> 因此主要用於觀察收視習慣與影音選擇，不直接與訂戶數進行比較。

---

## 🔄 Data Workflow｜資料處理流程

Public Data  
↓  
Python / pandas  
↓  
Excel  
↓  
SQL Server  
↓  
Power BI

### Python / pandas
用於公開資料的整理與清理，包括欄位整理、資料格式統一及後續分析前處理。

### Excel
用於資料檢視、確認與部分資料整理。

### SQL Server
將整理後的資料以資料表方式儲存，練習資料查詢、資料表管理及不同資料表之間的關聯。

### Power BI
建立資料模型、量值與互動式 Dashboard，進行趨勢、地區及不同影音服務的比較分析。

---

## 📊 Dashboard｜分析內容

### 1. 台灣有線電視訂戶趨勢

觀察第四台總訂戶數、市場占有率及各年度 YoY 變化。

主要觀察：
- 111Q1～115Q2 第四台累計流失約 47.8 萬戶
- 市場占有率由約 52.4% 降至 42.8%
- 113年各季 YoY 下降幅度較明顯
- 114年起下降幅度逐漸縮小
- 115年截至 Q2 仍維持負成長

<img width="1280" height="720" alt="cable-tv-trend" src="https://github.com/user-attachments/assets/ae35ab0a-41e3-4219-a34a-d151529ac3ab" />


---

### 2. 第四台 vs MOD

比較第四台與 MOD 在相同期間的用戶變化，
進一步觀察第四台流失的用戶是否明顯轉向 MOD。

分析結果顯示，第四台訂戶持續下降的同時，
MOD 用戶並未出現相對應的明顯成長。

因此，目前資料不足以支持
「第四台流失的用戶主要轉向 MOD」的推論。

<img width="1280" height="720" alt="cable-tv-vs-mod" src="https://github.com/user-attachments/assets/66197373-244b-42d1-84f7-ba5cd5e60521" />


---

### 3. 第四台市場結構

透過縣市、經營區及系統業者進一步探索第四台市場結構，
並觀察不同地區的訂戶分布。

在第四台訂戶流失地區中，
新北市的流失戶數最高，其次包含臺中市、桃園市、高雄市及臺北市。

---

### 4. OTT 使用分析

透過 NCC 114年傳播內容消費行為調查，
觀察 OTT 平台使用情況、不同年齡層的使用差異及使用 OTT 的主要原因。

主要觀察：
- Netflix 使用比例最高，達 91.0%
- 不同年齡層皆可觀察到 OTT 平台使用
- 「傳統電視服務沒有想看的電視節目」為主要使用原因之一，占 40.2%
- OTT 的使用情況顯示觀眾的影音選擇更加多元

<img width="1280" height="720" alt="ott-analysis" src="https://github.com/user-attachments/assets/a32d0c65-c953-4193-8750-1c5cd9fa9474" />


---

## 💡 Key Findings｜分析結論

### 01｜第四台持續流失

111Q1～115Q2 期間，
第四台訂戶累計減少約 **47.8萬戶**，
市場占有率也由約 **52.4% 降至 42.8%**。

### 02｜流失沒有明顯轉向 MOD

第四台下降期間，MOD 用戶並未出現明顯成長，
111Q1～115Q2 MOD 用戶同期變化約為 **-3.0%**。

因此，從目前資料無法判斷第四台流失用戶主要轉向 MOD。

### 03｜收視選擇逐漸分散

OTT 調查顯示觀眾的影音選擇更加多元。

114年調查中 Netflix 使用比例達 **91.0%**，
而「傳統電視服務沒有想看的電視節目」為使用 OTT 的主要原因之一，
比例為 **40.2%**。

### 整體結論

**有線電視並沒有消失，但觀眾有了更多選擇。**

第四台訂戶持續減少，但流失並未明顯轉向 MOD；
結合 OTT 消費者調查結果，可以觀察到台灣觀眾的影音選擇正在逐漸分散。

---

## 🛠️ Tools｜使用工具

| Tool | Application |
|---|---|
| Power BI | Dashboard、資料模型、量值與資料視覺化 |
| Python / pandas | 資料整理與清理 |
| SQL Server | 資料儲存、基礎查詢與資料表管理 |
| Excel | 資料檢視與整理 |

---

## 👩‍💻 My Role｜我的實作內容

本專題為個人資料分析專題，由我完成：

- 研究主題與分析問題設定
- 公開資料蒐集與整理
- Python / pandas 資料清理
- SQL Server 資料表建立與基礎查詢
- Power BI 資料模型與 Dashboard 製作
- 分析結果整理與視覺化呈現

透過本專題，我練習從問題設定、資料整理、資料儲存到 Power BI 視覺化的完整分析流程，
並嘗試將資料結果轉化為可以回答實際問題的分析內容。
