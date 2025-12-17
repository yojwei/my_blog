---
title: 30 天學習 Flask 計畫 - Weather App
date: 2025-12-17
tags:
  - Flask
  - Python
  - Web Development
  - Weather App
categories:
  - Learning Plan
---

## 專案概述

專案目標：使用 Flask 建立一個功能完整的天氣應用程式，整合天氣 API、資料視覺化與用戶管理功能。

---

## 第一週：基礎建立（Day 1-7）

### Day 1-2：環境設定與 uv 管理

- 安裝 uv 套件管理工具
- 建立 Flask 專案結構
- 第一個 Hello World 應用程式
- Git 版本控制初始化

### Day 3-4：路由與請求處理

- URL 路由基礎（首頁、搜尋頁面）
- HTTP 方法（GET、POST）
- 請求物件與回應物件
- 動態路由參數（城市名稱）
- 錯誤處理（404、500 頁面）

### Day 5-6：模板引擎 Jinja2

- 模板基礎語法
- 建立基礎模板（base.html）
- 首頁模板設計
- 天氣顯示卡片設計
- Bootstrap/Tailwind CSS 整合

### Day 7：表單處理

- 城市搜尋表單
- Flask-WTF 表單驗證
- CSRF 保護
- 輸入驗證與錯誤訊息

---

<!-- more -->

## 第二週：API 整合與資料處理（Day 8-14）

### Day 8-9：天氣 API 整合

- 註冊 OpenWeatherMap API（免費方案）
- API 金鑰管理（環境變數）
- requests 套件使用
- 獲取當前天氣資料
- API 錯誤處理

### Day 10-11：資料庫設計

- SQLite 資料庫設定
- Flask-SQLAlchemy ORM
- 資料模型設計：
  - User（用戶）
  - SavedCity（收藏城市）
  - SearchHistory（搜尋歷史）
- 資料庫遷移（Flask-Migrate）

### Day 12-13：用戶認證系統

- 用戶註冊與登入功能
- 密碼雜湊（werkzeug.security）
- Session 管理
- Flask-Login 整合
- 受保護的路由（收藏功能）

### Day 14：資料快取機制

- Flask-Caching 設定
- API 回應快取（避免頻繁請求）
- 快取過期策略
- Redis 快取（選用）

---

## 第三週：Weather App 核心功能開發（Day 15-21）

### Day 15-16：天氣查詢功能

- 依城市名稱查詢天氣
- 顯示當前天氣資訊：
  - 溫度、濕度、風速
  - 天氣狀況描述
  - 天氣圖示
- 攝氏/華氏溫度切換
- 地理定位整合（選用）

### Day 17-18：多日天氣預報

- 5 天天氣預報 API 整合
- 預報資料處理與格式化
- 時間序列資料顯示
- 圖表視覺化（Chart.js）
  - 溫度趨勢圖
  - 降雨機率圖

### Day 19-20：收藏與管理功能

- 用戶收藏城市功能
- 收藏清單管理
- 批次查詢收藏城市天氣
- 拖曳排序功能（JavaScript）
- 搜尋歷史記錄

### Day 21：進階功能

- 天氣警報通知
- 空氣品質指數（AQI）整合
- 日出日落時間
- UV 指數顯示
- 體感溫度計算

---

## 第四週：優化與部署（Day 22-30）

### Day 22-23：前端優化

- 響應式設計（RWD）
- 載入動畫與骨架屏
- 天氣背景動態變化
- 深色模式支援
- PWA 功能（離線支援）

### Day 24-25：效能與安全

- API 請求限流（Flask-Limiter）
- SQL Injection 防護
- XSS 防護
- API 金鑰保護
- 資料庫查詢優化
- 分頁功能

### Day 26-27：測試與品質保證

- 單元測試（pytest）
- API 模擬測試
- 表單驗證測試
- 使用者流程測試
- 程式碼覆蓋率

### Day 28：Docker 容器化

- Dockerfile 撰寫
- docker-compose.yml 設定
- PostgreSQL 資料庫遷移
- 環境變數配置
- 容器測試

### Day 29：雲端部署

- 選擇部署平台（Render/Railway/Fly.io）
- PostgreSQL 資料庫設定
- 環境變數配置
- Gunicorn + Nginx 設定
- HTTPS 憑證設定

### Day 30：文件與收尾

- README.md 撰寫
- API 使用說明
- 專案架構文件
- 部署指南
- 未來功能規劃：
  - 多語言支援
  - 社群分享功能
  - 天氣推播通知
  - 數據分析儀表板

---

## Weather App 功能清單

### 核心功能

- ✅ 城市天氣查詢
- ✅ 5 天天氣預報
- ✅ 溫度單位切換
- ✅ 天氣視覺化圖表
- ✅ 用戶註冊/登入
- ✅ 收藏城市管理
- ✅ 搜尋歷史

### 進階功能

- ✅ 空氣品質指數
- ✅ 天氣警報
- ✅ 響應式設計
- ✅ 深色模式
- ✅ API 快取機制

---

## 使用技術棧

### 後端

- **Python 3.11+**
- **Flask** - Web 框架
- **Flask-SQLAlchemy** - ORM
- **Flask-Login** - 認證
- **Flask-WTF** - 表單處理
- **Flask-Migrate** - 資料庫遷移
- **Flask-Caching** - 快取
- **uv** - 套件管理

### 前端

- **Jinja2** - 模板引擎
- **Bootstrap 5** / **Tailwind CSS**
- **Chart.js** - 圖表
- **Alpine.js** - 輕量互動

### 資料庫

- **SQLite** (開發)
- **PostgreSQL** (正式環境)

### API

- **OpenWeatherMap API**
- **Geolocation API**

### 部署

- **Docker**
- **Gunicorn**
- **Nginx**
- **Render/Railway**

---

## 學習資源

### 官方文件

- [Flask Documentation](https://flask.palletsprojects.com/)
- [OpenWeatherMap API](https://openweathermap.org/api)
- [uv Documentation](https://github.com/astral-sh/uv)

### 推薦教學

- Flask Mega-Tutorial
- Real Python Flask 系列
- Corey Schafer Flask 影片

---

**開始日期**：2025-12-17  
**預計完成**：2026-01-15  
**每日時間**：2-3 小時

Let's build something amazing! 🌤️
