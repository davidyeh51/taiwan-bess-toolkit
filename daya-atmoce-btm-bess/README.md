# 達亞光電 BTM 儲能容量與收益建議

本資料夾是一份靜態 HTML 簡報，用於討論達亞光電高壓三段式電價用戶導入表後儲能的容量設計與收益估算。

## 入口檔案

- `index.html`

## 核心結論

- 目標：契約容量由 1,500 kW 降至 1,200 kW。
- 超約管理：保留 60~120 kW 功率，採事件型控制，不做持續 300 kW 削峰。
- 建議主方案：ATMOCE M-ELV BattBank，3 組 cluster，約 168 kW / 337.68 kWh。
- 年化毛效益：基本電費節省約 685,890 元/年，平日尖離峰價差套利約 431,240 元/年，合計約 1,117,130 元/年。

## 主要假設

- 每組 cluster 以 7 個 pack 估算。
- 每個 pack 以 16.08 kWh、8 kVA 連續輸出估算。
- 電池可用放電容量採名目容量 80%。
- AC-AC 往返效率採 90%。
- 夏月以 2026 年平日 109 天估算，非夏月以 2026 年平日 152 天估算。
- 未納入設備成本、工程費、消防、維運、衰退、稅費、停機、週末與國定假日收益。

## 來源

- ATMOCE Business Owner: https://www.atmoce.com/en/businessowner
- ATMOCE M-ELV BattBank: https://www.atmoce.com/en/battbank
- 台電詳細電價表: https://www.taipower.com.tw/media/xtofy2yw/%E8%A9%B3%E7%B4%B0%E9%9B%BB%E5%83%B9%E8%A1%A8.pdf?mediaDL=true

正式投資決策需以供應商正式規格書、台電最新費率、現場單線圖與 12 個月 15 分鐘 AMI 資料覆核。
