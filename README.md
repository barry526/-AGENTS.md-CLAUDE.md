# AGENTS.md - 專案開發規範與 AI 協作指南

## 1. 專案目的與範疇 (Project Purpose)
本專案為「個人技術與工程知識庫」，旨在收錄機器學習、C++ / Python 實作與半導體工程相關筆記。所有頁面均須遵循統一的模組化 HTML 設計。

## 2. 檔案命名與目錄結構 (Directory & Naming Standard)
- 所有主題內頁必須放置於 `pages/` 資料夾下。
- 檔案命名一律使用小寫英文字母與連字符號（kebab-case），例如：`pages/icp-algorithm.html`。
- 靜態樣式檔一律參照 `css/style.css`，嚴禁在個別 HTML 中撰寫重複的大量 `<style>` 區塊。

## 3. UI 與整體視覺風格 (Design System)
- **色調主題**：科技深藍（主色 `#0f172a`）、極簡白（背景 `#f8fafc`）、強烈對比藍（標示色 `#2563eb`）。
- **字體設定**：優先採用 System UI Font (`-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`)。
- **排版佈局**：頂端需有固定導覽列（Navbar），左側/頂部提供專案章節快速切換連結。

## 4. 頁面結構與規範 (Page Template Standard)
新增任何頁面時，必須嚴格依照 `pages/template.html` 的結構生成：
1. `<header>`：包含專案標題與主選單連結。
2. `<main>`：
   - 區塊一：`<h1>` 頁面名稱與摘要描述（Abstract）。
   - 區塊二：`<h2>` 核心原理 / 內容說明。
   - 區塊三：`<code>` 或 `<pre>` 程式碼與配置範例（必須套用語法高亮樣式）。
3. `<footer>`：版權宣告與返回首頁連結。

## 5. AI 修改與新增內容守則 (AI Action Rules)
當使用者要求「新增一個頁面」或「修改既有頁面」時，AI 必須遵循以下規則：
1. 讀取 `pages/template.html` 複製標準 HTML 結構。
2. 檢查 `index.html` 的目錄清單，自動將新頁面的相對連結更新至首頁列表中。
3. 確保所有內部連結一律使用相對路徑（例如：`../index.html` 或 `./pages/xxxx.html`）。
4. 新增頁面後，主動回報修改的檔案清單與新增的頁面 URL 路徑。

6.網頁連結https://barry526.github.io/-AGENTS.md-CLAUDE.md/
