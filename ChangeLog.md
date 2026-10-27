# 614A EWOD Firmware Change Log

此文件記錄 614A EWOD Firmware 各版本主要修改內容。
詳細程式差異請搭配 Git Commit / Tag 查詢。

---

## 2026-10-27

### 基本資訊

- Hardware: YXT000614A / YXT000615A
- MCU: STM32H7B0ZBT6
- Git Tag: V0.1.0
- Git Commit: 9594068
- Firmware HEX: HEX/614A_STM32H7B0ZBT6_EWOD_20261014.hex
- FPGA POF: HEX/FPGA_EWOD_V9723.pof
- Version Type: release

### 新增功能

- NA

### 修改內容

- 修改部份函數引用 ui.c 內函數, 會帶出非預期的文字打印，這些文字打印為新增加給 UI 辨識資料截取區域使用。
- 修改 Bomber 分離功能。

### 修正問題

- 修正部份函數回傳 UI 出餘字元內容。
- 修正 Bomber 中繼母體回收多餘液珠時,中繼母體上電不完全問題。
- 修正 Bomber 中繼母體回收多餘液珠時,多餘液珠未成功分出時會取消上電區並記錄資料會清除為預設值。
- 修正 Bomber 分離液珠時, 中繼母體上電區演算法; 減小中繼母體的拉力, 讓吸力弱的面板增加分離成功率。

### 測試內容

- [V] Keil Build PASS
- [V] MCU Programming PASS
- [V] UI Command Test PASS
- [V] EWOD Panel Test PASS

### 已知問題

- 其他問題：無 / 待確認。

### 備註

此版本開始將對應的 HEX Firmware 存放於 `HEX/` 目錄，
並與 Source Code 一起納入 Git Commit。
之後可透過 Git Tag 同時取得該版本 Source Code 與 Firmware HEX。

---
