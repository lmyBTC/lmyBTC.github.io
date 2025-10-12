# SOP: 新增文章頁面標準作業流程

本文檔定義了為 `CryptoCompound` 新增一篇文章的標準作業流程 (SOP)。請嚴格遵循此流程以確保網站的品質、一致性和可維護性。

> **文章寫作風格與內容結構的詳細指引，請參考** [`doc/writing-guide.md`](writing-guide.md)。

---

## 📋 快速檢查清單 (TL;DR)

- [ ] **建立檔案**: 複製現有文章 (如 `core-btc.html`)，並根據主題重新命名。
- [ ] **撰寫內容**: 遵循 `writing-guide.md` 的 PSMA 結構與8大章節指引。
- [ ] **更新文章總覽**: 手動在 `post/archive.html` 中新增文章卡片。
- [ ] **更新分類頁面**: (如果適用) 手動在對應的 `topic-xxx.html` 頁面新增文章卡片。
- [ ] **更新網站地圖**: 手動在 `sitemap.xml` 中新增文章的 URL。
- [ ] **新增內部連結**: 在至少一篇相關的舊文章中，加入新文章的內部連結。
- [ ] **完成最終驗證**: 執行 SEO、內容品質與技術功能檢查。

---

## 📝 詳細步驟指南

### 步驟 1：建立文章檔案

1.  在 `post/` 資料夾下，**複製一篇結構類似的現有文章** (例如 `core-btc.html` 或 `chainlink.html`) 作為範本。
2.  將複製的檔案根據文章主題重新命名。
    -   **專案介紹文章**: 直接使用專案的小寫名稱 (例如 `solana.html`)。
    -   **主題彙整頁面**: 使用 `topic-[主題].html` 的格式 (例如 `topic-layer2.html`)。
3.  打開新檔案，開始修改內容。

### 步驟 2：撰寫與編輯內容

1.  **填寫 Meta 資訊**: 修改 `<title>`, `<meta name="description">`, `<meta name="keywords">`。
2.  **填寫 JSON-LD**: 修改 `Article` 結構化資料，特別是 `@id` (新文章的完整 URL) 以及 `datePublished` / `dateModified`。
3.  **撰寫文章**: 嚴格遵循 `doc/writing-guide.md` 中定義的 **PSMA 敘事流程** 和 **8大核心章節** 結構進行撰寫。
4.  **使用正確的 CSS Class**: 根據 `writing-guide.md` 的規範，使用如 `.alert-tech`, `.info-cards`, `.comparison-table` 等樣式來豐富內容。

### 步驟 3：更新網站索引

1.  **更新文章總覽頁面 (`archive.html`)**
    -   打開 `post/archive.html`。
    -   在 `<div class="archive-grid">` 內，複製一個現有的 `<div class="article-card">` 區塊並貼上。
    -   修改新卡片的內容，包含 `data-category`, `data-published`, `data-modified` 以及標題、描述和連結，使其指向你的新文章。

2.  **更新分類主題頁面 (如果適用)**
    -   如果您的文章隸屬於某個核心系列 (如 `topic-core.html`)，請打開對應的分類頁面。
    -   同樣在其中新增文章卡片。

3.  **更新網站地圖 (`sitemap.xml`)**
    -   打開根目錄的 `sitemap.xml`。
    -   在 `</urlset>` 標籤前，新增一個 `<url>` 區塊，並將 `<loc>` 和 `<lastmod>` 更新為新文章的正確資訊。

    ```xml
    <url>
      <loc>https://lmybtc.github.io/post/your-new-article.html</loc>
      <lastmod>YYYY-MM-DD</lastmod>
      <changefreq>monthly</changefreq>
      <priority>0.8</priority>
    </url>
    ```

### 步驟 4：品質保證 (QA)

在提交變更前，執行以下最終檢查。

#### 內容品質檢查
- [ ] **標題策略**: 確認標題符合 V.I.P. + B.R.A.V.E. 框架。
- [ ] **章節完整性**: 檢查是否包含 `writing-guide.md` 中定義的8個標準章節。
- [ ] **敘事順序**: 採用 PSMA (痛點→解方→原理→行動) 流程。
- [ ] **CSS Class 使用**: 確認已使用如 `.alert`, `.info-cards` 等樣式來組織內容。

#### SEO 優化檢查
- [ ] `<title>` 長度適中且具吸引力。
- [ ] `<meta description>` 長度在 150 字元左右，並包含核心關鍵字。
- [ ] **JSON-LD 驗證**: 確認 `Article` 結構化資料中的 URL 和日期都已更新。
- [ ] **內部連結**: 確認已在至少一篇舊文章中加入了新文章的連結。

#### 技術功能檢查
- [ ] **本地預覽**: 在本地伺服器上打開新頁面，確認樣式正常。
- [ ] **連結檢查**: 點擊頁面上的所有內部和外部連結，確保沒有 404 錯誤。
- [ ] **主控台檢查**: 按 `F12` 打開瀏覽器開發者工具，確認 `Console` (主控台) 分頁沒有任何紅色錯誤訊息。
- [ ] **響應式檢查**: 縮放瀏覽器視窗，檢查在手機寬度下排版是否正常。
