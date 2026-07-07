# 達亞光電 BTM 儲能容量與收益建議

本資料夾是一份靜態 HTML 簡報，用於討論達亞光電高壓三段式電價用戶導入表後儲能的容量設計與收益估算。

## 入口檔案

- `index.html`

## 核心結論

- 目標：契約容量由 1,500 kW 降至 1,200 kW。
- 超約管理：保留 60~120 kW 功率，採事件型控制，不做持續 300 kW 削峰。
- 反推建議：ATMOCE M-ELV BattBank 以 7 packs 為滿配 stack。
- 2 個滿配 stack：112 kVA / 225.12 kWh，可提供約 112 kW、9.3% 的超約管理預度，是降至 1,200 kW 的基準方案。
- 3 個滿配 stack：168 kVA / 337.68 kWh，可提供約 168 kW、14.0% 的超約管理預度，是收益與降額餘裕加強方案。
- 年化毛效益：2 stack 約 973,383 元/年，3 stack 約 1,117,130 元/年；未扣 O&M、衰退、稅費與停機。

## 主要假設

- 產品型號：ATMOCE MS-16K-U。
- 每個 pack 以 16.08 kWh、8 kVA 額定輸出、10 kVA 最大輸出估算。
- 每個 stack 最多堆疊 7 packs；滿配 stack 約 112.56 kWh、56 kVA 額定輸出。
- 1 / 2 / 3 個滿配 stack 分別為 56 / 112 / 168 kVA 額定輸出，對應契約容量 1,200 kW 的 4.7% / 9.3% / 14.0% 預度。
- 電池可用放電容量採名目容量 80%。
- AC-AC 往返效率採 90%。
- 夏月以 2026 年平日 109 天估算，非夏月以 2026 年平日 152 天估算。
- 未納入設備成本、工程費、消防、維運、衰退、稅費、停機、週末與國定假日收益。

## Stack 方案比較

| 方案 | 額定/最大功率 | 名目容量 | 可防超約預度 | 平日價差套利毛收益 |
| --- | ---: | ---: | ---: | ---: |
| 1 stack | 56 / 70 kVA | 112.56 kWh | 56 kW，4.7% | 143,747 元/年 |
| 2 stacks | 112 / 140 kVA | 225.12 kWh | 112 kW，9.3% | 287,493 元/年 |
| 3 stacks | 168 / 210 kVA | 337.68 kWh | 168 kW，14.0% | 431,240 元/年 |

## 來源

- ATMOCE Business Owner: https://www.atmoce.com/en/businessowner
- ATMOCE M-ELV BattBank: https://www.atmoce.com/en/battbank
- 台電詳細電價表: https://www.taipower.com.tw/media/xtofy2yw/%E8%A9%B3%E7%B4%B0%E9%9B%BB%E5%83%B9%E8%A1%A8.pdf?mediaDL=true

正式投資決策需以供應商正式規格書、台電最新費率、現場單線圖與 12 個月 15 分鐘 AMI 資料覆核。
