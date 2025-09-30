# LMY's Crypto Blog

這是一個專為內容創作者設計的、高度優化的靜態網站解決方案。專案旨在提供一個**零依賴、無建置步驟**的純粹 HTML/CSS/JS 環境，讓創作者可以完全專注於內容本身，同時確保網站具備高效能、易於維護和對 SEO 友好的特性。

## 核心設計理念

1.  **簡潔至上 (Simplicity First)**：專案不使用任何前端框架 (React, Vue) 或複雜的建置工具 (Webpack, Vite)。這意味著沒有 `node_modules`，沒有編譯過程，您可以直接在瀏覽器中預覽任何 HTML 檔案。
2.  **關注點分離 (Separation of Concerns)**：嚴格劃分 HTML (結構)、CSS (表現) 和 JavaScript (行為) 的職責。全域樣式、頁面專用樣式和文章樣式被明確分離，便於管理和擴充。
3.  **手動控制的確定性 (Manual & Deterministic)**：所有內容更新（如文章列表、Sitemap）均為手動操作。這雖然犧牲了部分自動化，但換來了對網站結構和內容的 100% 控制權，避免了自動化工具可能帶來的意外錯誤。

## 🚀 技術棧

- **HTML5**
- **CSS3** (Flexbox, Grid, Custom Properties)
- **JavaScript** (ES6, 用於實現客戶端互動功能，無外部依賴)

## 🛠️ 本地開發

由於本專案是純靜態網站，您不需要安裝任何伺服器環境。

1.  **安裝 Live Server**：建議在 VS Code 中安裝 Live Server 擴充套件。
2.  **啟動預覽**：在 VS Code 中，右鍵點擊任何 `.html` 檔案，選擇 `Open with Live Server`。
3.  **即時預覽**：任何對 HTML、CSS 或 JS 檔案的修改都會自動在瀏覽器中重新整理。

## 📂 專案結構與資料夾分類規則

為了保持專案的整潔和可維護性，本專案遵循嚴格的資料夾分類規則。所有網站內容都位於 `lmyBTC.github.io/` 資料夾下。

```
lmyBTC.github.io/
│
├── index.html          # 網站首頁
├── about.html          # 關於我頁面
├── main.css            # 全局核心樣式檔案
├── sitemap.xml         # 網站地圖 (SEO用)
├── robots.txt          # 爬蟲規則 (SEO用)
│
├── assets/
│   └── css/            # 存放所有【頁面專用】的 CSS 檔案
│       ├── home.css
│       ├── about.css
│       ├── archive.css
│       └── article.css
│
├── post/
│   ├── archive.html    # 文章總覽頁面
│   └── *.html          # 所有【文章頁面】都存放在此
│
└── doc/
    └── draft/          # 存放文章草稿與參考文稿，【此資料夾會同步至 GitHub】

```

**核心規則：**

1.  **CSS 存放規則**：
    - 所有頁面專用的 CSS 檔案都必須存放在 `assets/css` 資料夾中。
    - 唯一的例外是位於根目錄的 `main.css`，它是全站的基礎樣式。
    - **嚴禁**在 `post/` 或其他任何非規定位置存放 CSS 檔案。

2.  **內容分離**：
    - **文章**：所有部落格文章的 HTML 檔案都必須存放在 `post/` 資料夾中。
    - **頁面**：非文章類型的獨立頁面（如 `about.html`）應存放在根目錄。

3.  **參考資料**：
    - `doc/test/`：此資料夾用於存放開發過程中的參考檔案或草稿。它已被加入 `.gitignore`，其內容不會、也不應該被推送到 GitHub 倉庫。

## 🔧 維護指南

本指南定義了專案的標準操作流程 (SOP)。

### 內容管理工作流

> [!IMPORTANT]
> **核心規範：** 在新增或修改任何內容前，請務必詳閱以下兩份核心文件：
> 1.  **寫作風格指南**: `doc/writing-guide.md` - 定義了內容語氣、結構和 SEO 標準。
> 2.  **新增頁面檢查清單**: `doc/new-page-checklist.md` - 提供了從建立到發布的完整步驟。

#### 新增一篇文章

1.  **建立文章檔案**: 在 `post/` 目錄下，複製 `chainlink.html` 並重新命名。
    -   **命名規則**: 專案介紹文章應直接使用專案名稱，例如 `chainlink.html` 或 `solana.html`。主題頁面可使用前綴，如 `topic-btc.html`。
    -   **使用範本**: 務必使用現有文章作為範本，以確保頁面具備左側動態目錄功能。
2.  **撰寫內容**: 根據 `doc/writing-guide.md` 的規範進行撰寫，並填寫頁首的 SEO Meta 資訊。
3.  **更新索引**:
    -   打開 `post/archive.html`，在 `<div class="archive-grid">` 中新增對應的文章卡片。
    -   (可選) 若希望文章出現在首頁，請同步更新 `index.html` 的精選文章區塊。
4.  **更新網站地圖**: 打開根目錄的 `sitemap.xml`，為新文章新增一個 `<url>` 區塊。

#### 修改頁面樣式

-   **全域樣式**: 若要修改**全站通用**的樣式（如主題顏色、字體、頁首頁尾），請編輯根目錄的 `main.css`。
-   **專用樣式**: 若要修改**特定頁面**的樣式（如首頁的英雄區塊、文章列表的篩選器），請到 `assets/css/` 資料夾中找到對應的 CSS 檔案進行編輯。

## 部署

本專案透過 GitHub Actions 自動部署到 GitHub Pages。任何推送到 `main` 分支的提交都會觸發 `.github/workflows/deploy.yml` 中的部署流程。

**部署目標**: `lmyBTC/lmyBTC.github.io`
**來源目錄**: `lmyBTC.github.io/`
**目標分支**: `main`

**部署目標**: `lmyBTC/lmyBTC.github.io`
**來源目錄**: `lmyBTC.github.io/`
**目標分支**: `main`