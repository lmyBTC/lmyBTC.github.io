# LMY's Crypto Blog

這是一個基於靜態 HTML 和 CSS 的個人加密貨幣財經部落格。專案旨在提供關於區塊鏈技術、市場趨勢和投資策略的深度分析文章。

## ✨ 主要功能

- **黑色科技感 UI**：全站採用統一的深色主題，提供專業、具科技感的閱讀體驗。
- **響應式設計**：針對桌面、平板和行動裝置進行了優化。
- **動態文章目錄**：文章頁面提供左側浮動目錄，方便讀者在長篇文章中快速導覽。
- **進階文章列表**：文章總覽頁面具備分類篩選、關鍵字搜尋和排序功能，幫助讀者快速找到感興趣的內容。

## 🚀 技術棧

- **HTML5**
- **CSS3** (Flexbox, Grid)
- **JavaScript** (用於實現動態目錄和文章列表的互動功能)

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
    └── test/           # 僅供開發時參考，【此資料夾會被 .gitignore 忽略，不會上傳】

```

**核心規則：**

1.  **樣式分離**：
    - `main.css`：定義全站的基礎樣式，如顏色變數、字體、頁首頁尾等。
    - `assets/css/`：存放**特定頁面**的專屬樣式。例如，`home.css` 只用於 `index.html`，`archive.css` 只用於 `post/archive.html`。
    - **嚴禁**在 `post/` 或其他非 `assets` 資料夾中存放 CSS 檔案。

2.  **內容分離**：
    - **文章**：所有部落格文章的 HTML 檔案都必須存放在 `post/` 資料夾中。
    - **頁面**：非文章類型的獨立頁面（如 `about.html`）應存放在根目錄。

3.  **參考資料**：
    - `doc/test/`：此資料夾用於存放開發過程中的參考檔案或草稿。它已被加入 `.gitignore`，其內容不會、也不應該被推送到 GitHub 倉庫。

## 🔧 維護指南

### 如何新增一篇文章？

1.  **建立 HTML 檔案**：在 `post/` 資料夾下建立一個新的 `.html` 檔案（例如 `my-new-article.html`）。建議複製現有的文章（如 `chainlink-oracle-deep-dive.html`）作為範本，以確保結構和動態目錄功能正常。
2.  **更新文章列表**：打開 `post/archive.html`，在 `<div class="archive-grid">` 中新增一個對應的文章卡片 (`<div class="article-card">...</div>`)。請務必填寫正確的 `data-category` 和 `data-modified` 等屬性，以確保篩選和排序功能正常。
3.  **更新網站地圖**：打開根目錄的 `sitemap.xml`，在其中為您的新文章新增一個 `<url>` 區塊，並更新 `<lastmod>` 日期。

### 如何修改樣式？

-   若要修改**全站通用**的樣式（如主題顏色、字體、頁首頁尾），請編輯根目錄的 `main.css`。
-   若要修改**特定頁面**的樣式（如首頁的英雄區塊、文章列表的篩選器），請到 `assets/css/` 資料夾中找到對應的 CSS 檔案進行編輯。

## 部署

本專案透過 GitHub Actions 自動部署到 GitHub Pages。任何推送到 `main` 分支的提交都會觸發 `.github/workflows/deploy.yml` 中的部署流程。