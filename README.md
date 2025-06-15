# Clawcite

> 一款基於 Go + SQLite FTS5 的文本相似度比對系統，靈感來自 Turnitin。  
> 支持模板文檔與草稿句子逐句模糊比對，標註重複率與來源，輕量便攜，適合個人和小團隊使用。

---

## 主要特點

- **高效全文檢索**：採用 SQLite FTS5 實現句子級全文模糊比對  
- **輕量跨平台**：Go 編寫，前端使用 Svelte + Tailwind，最終打包成單一 .exe 可執行文件  
- **即時比對**：Draft 上傳後即時拆句、比對、展示結果，並可清理臨時數據  
- **直觀界面**：簡潔現代的 SPA UI，輕鬆查看重複句子及其來源  
- **開源友好**：完整開發流程及架構，方便二次開發與定制

---

## 技術棧

- **後端**：Go, Gin, SQLite + FTS5, sqlc, embed.FS  
- **前端**：Svelte, TypeScript, Tailwind CSS, Vite  
- **數據庫**：SQLite FTS5（全文索引）  
- **打包**：Go embed 靜態文件，交叉編譯生成跨平台可執行文件

---

## 功能模塊

- 用戶認證（JWT）  
- 模板文檔管理（拆句存入 FTS5）  
- Draft 句子拆分、暫存、全文比對  
- 比對結果計算重複率及來源匹配  
- 比對結果前端展示（高亮、來源標註）  
- 報告生成（未來擴展）  

---

## 快速開始

### 環境要求

- Go 1.20+  
- Node.js 18+（用於前端開發）  

### 本地開發

```bash
# 後端依賴安裝與啟動
go mod tidy
go run main.go

# 前端開發
cd frontend
npm install
npm run dev
````

### 打包

```bash
cd frontend
npm run build

cd ..
go build -o clawcite.exe
```

---

## 項目結構（簡要）

```
/
├─ backend/             # Go 後端代碼
├─ frontend/            # Svelte 前端代碼
├─ templates/           # 模板文檔存儲位置
├─ draft/               # 草稿臨時存儲（可選）
├─ sqlc/                # sqlc 配置與生成代碼
├─ main.go              # 程序入口，靜態文件嵌入
├─ README.md
```

---

## 開發計劃（Roadmap）

* [x] 核心全文比對功能（模板與 Draft）
* [x] 簡易用戶認證
* [x] 前端界面基礎框架
* [ ] 報告導出（PDF/HTML）
* [ ] 多用戶協作支持
* [ ] 性能優化與大規模文檔支持

---

## 參考資源

* [SQLite FTS5 官方文檔](https://www.sqlite.org/fts5.html)
* [Gin 框架](https://gin-gonic.com/)
* [Svelte 官方網站](https://svelte.dev/)
* [Tailwind CSS](https://tailwindcss.com/)

---

## 聯繫我

如果你有任何建議或問題，歡迎通過 Issues 或 Pull Requests 與我交流！

---

## 授權

MIT License © 2025 Clawcite 團隊
