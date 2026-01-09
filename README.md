# 🚶 全台行人與無障礙導航系統 (Taiwan Sidewalk Navigation)

這是一個致力於改善台灣行人交通與無障礙環境的開源專案。
透過視覺化全台人行道數據，我們期望為身障人士、輪椅使用者及一般行人打造更友善的步行導航體驗。

![Project Status](https://img.shields.io/badge/Status-Prototype-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 🔗 線上展示 (Live Demo)
👉 **[點擊這裡查看地圖](https://您的帳號.github.io/taiwan-sidewalk-nav/)**
*(請將此處連結替換為您 Settings > Pages 中的網址)*

## 📊 資料來源與處理 (Data Source)

本專案之核心地理圖資來自 **中華民國內政部國土管理署 (National Land Management Agency)** 之公開資料。

* **原始來源**：市區道路人行道資料 (Sidewalk Layer)
* **原始格式**：Shapefile (TWD97 座標系統)
* **目前格式**：GeoJSON (WGS84 經緯度)
* **資料內容**：包含人行道幾何形狀、通行寬度、淨寬（無障礙寬度）等關鍵屬性。

> **特別感謝**：苗栗縣政府工務處協助轉介，以及國土管理署維護之開放資料平台。

## 🛠️ 技術架構 (Tech Stack)

* **前端顯示**：HTML5, CSS3
* **地圖引擎**：[Leaflet.js](https://leafletjs.com/) (Open-Source JavaScript Library)
* **底圖來源**：OpenStreetMap (OSM)
* **資料處理**：Python (使用 `geopandas` 進行座標轉換 TWD97 -> WGS84)

## 📂 檔案結構

* `index.html`: 主地圖介面程式碼。
* `final_sidewalk_map.geojson`: 經過轉換處理的全台人行道圖資檔案。
* `README.md`: 專案說明文件。

## 🚀 未來展望 (Roadmap)

1.  **路徑規劃 (Routing)**：實作 A* 或 Dijkstra 演算法，計算點對點的「純人行道」導航路徑。
2.  **無障礙過濾**：增加篩選功能，僅顯示淨寬大於 90cm 且無障礙礙物之路徑。
3.  **整合更多圖資**：疊加騎樓整平、標線型人行道及路口號誌數據。
4.  **手機版優化**：改善行動裝置上的瀏覽體驗。

## 🤝 如何參與貢獻

歡迎任何對「人本交通」與「科技公益」有興趣的朋友參與！
您可以透過提交 Issue 或 Pull Request 來協助改進這個專案。

---
*免責聲明：本專案為民間開發之原型系統，圖資僅供參考，實際路況請以現場為準。*
