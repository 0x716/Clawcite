# 🐾 Clawcite

**Clawcite** 是一款輕量級、可視化、本地部署的資料收集與分析工具，支援檔案上傳、範例對照、即時報表與圖表展示。靈感來自 UptimeKuma 與 Pocketbase，專為需要本地運行、可自定義資料處理邏輯的使用者打造。

> 無需網路連接，一鍵啟動，開箱即用。🖥️📦

---

## ✨ Features

- 🧾 **使用者登入/註冊系統**  
  基於 JWT 的認證與權限管理，確保資料安全。

- 📤 **上傳檔案與參考範例**  
  支援常見格式（CSV、TXT、PDF、圖片等）並自動儲存與歸類。

- 📊 **資料展示與報表生成**  
  可視化圖表、比對參考、摘要說明。

- 💾 **單檔執行，無需安裝資料庫**  
  使用嵌入式 SQLite，自動啟動本地伺服器。

- 🐳 **支援 Docker 部署**  
  提供簡單的 `docker-compose.yml`，方便伺服器佈署。

---

## 🛠️ 技術棧

| 分類      | 技術                                                         |
|-----------|--------------------------------------------------------------|
| 前端      | React + TypeScript + ShadCN UI + TailwindCSS                 |
| 後端      | Go (Golang)                                                  |
| 嵌入靜態頁面 | `embed.FS` 打包 React 網頁作為單一執行檔                   |
| 身份驗證  | JWT / Session 管理                                           |
| 資料庫    | SQLite（可替換為 PostgreSQL）                                |
| 部署      | 單檔執行、Docker、GitHub Release 提供 Windows/Mac/Linux 版本 |

---

## 🚀 快速開始

### 方式 1：下載執行檔（建議）

1. 下載對應平台的單檔執行檔（[Release 頁面](https://github.com/your-user/clawcite/releases)）
2. 點擊啟動，瀏覽器前往 [`http://localhost:8787`](http://localhost:8787)

### 方式 2：Docker 部署

```bash
git clone https://github.com/your-user/clawcite.git
cd clawcite
docker-compose up -d
