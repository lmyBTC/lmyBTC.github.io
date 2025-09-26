# SOP: 新增文章頁面標準作業流程

本文檔定義了為 `LMY's Crypto Blog` 新增一篇文章的標準作業流程 (Standard Operating Procedure)。請嚴格遵循此流程以確保網站的品質、一致性和可維護性。

## 📋 快速檢查清單 (TL;DR)

- [ ] **內容**：在 `post/` 資料夾中建立新文章的 `.html` 檔案。
- [ ] **結構**：使用下方提供的標準範本，填寫所有 `meta` 和 `JSON-LD` 資訊。
- [ ] **目錄**：確保文章中的章節標題使用 `<h2>` 標籤，以便自動生成側邊欄目錄。
- [ ] **列表**：更新 `post/archive.html`，新增指向新文章的文章卡片。
- [ ] **地圖**：更新根目錄的 `sitemap.xml`，加入新文章的 URL。
- [ ] **連結**：在至少一篇相關的舊文章中，加入新文章的內部連結。
- [ ] **驗證**：完成本地端 QA 檢查（無失效連結、無主控台錯誤、響應式正常）。

---

## 📝 詳細步驟指南

### 步驟 1：建立文章檔案

1.  在 `post/` 資料夾下，建立一個新的 HTML 檔案，例如 `my-awesome-article.html`。
    - **命名規則**: 若是介紹特定專案，檔名應直接使用專案的小寫名稱，例如 `chainlink.html` 或 `solana.html`。
    - **主題頁面**: 若是關於某個主題的彙整頁，檔名應使用 `topic-[主題].html` 的格式，例如 `topic-btc.html`。
2.  **複製並貼上**以下標準範本。這是確保頁面結構、樣式、SEO 和動態目錄功能正常的基礎。
    > **重要**: 建議直接複製現有的文章檔案（如 `post/chainlink.html`）來確保所有腳本和結構都是最新的。

```html
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- ▼ SEO Meta - 請務必填寫 ▼ -->
    <title>文章標題 | LMY's Crypto Blog</title>
    <meta name="description" content="這篇文章的簡短描述，約 150 字元，會顯示在 Google 搜尋結果中。">
    <meta name="keywords" content="主要關鍵字, 相關關鍵字, 次要關鍵字">
    <meta name="google-site-verification" content="F1sAja4V6KTk17SiojYOS8UF1GP9-hu8TXI8iVKQ27Y" />
    <!-- ▲ SEO Meta - 請務必填寫 ▲ -->

    <!-- ▼ JSON-LD (結構化資料) - 請務必填寫 ▼ -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Article",
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://lmybtc.github.io/post/project-name.html" // <== 修改為新文章的完整 URL
      },
      "headline": "文章主標題 (應與 <title> 標籤內容相似)",
      "description": "這篇文章的詳細描述 (可與 meta description 相同)",
      "author": {
        "@type": "Organization",
        "name": "LMY's Crypto Blog",
        "url": "https://lmybtc.github.io/"
      },
      "publisher": {
        "@type": "Organization",
        "name": "LMY's Crypto Blog"
      },
      "datePublished": "YYYY-MM-DD", // <== 修改為發布日期
      "dateModified": "YYYY-MM-DD"  // <== 修改為最後修改日期
    }
    </script>
    <!-- ▲ JSON-LD (結構化資料) - 請務必填寫 ▲ -->

    <!-- 樣式檔案 -->
    <link rel="stylesheet" href="../main.css">
    <link rel="stylesheet" href="../assets/css/article.css">
</head>
<body>

    <header class="site-header">
        <!-- Header 內容會由全局樣式和結構定義 -->
    </header>

    <main>
        <div class="article-layout container">
            <aside class="toc-sidebar">
                <nav class="toc">
                    <h3>文章目錄</h3>
                    <ul id="toc-list"></ul>
                </nav>
            </aside>
            <article class="article-container">
                <h1>文章主標題</h1>
                <p class="article-meta">發布日期：YYYY-MM-DD</p>

                <!-- ▼ 文章內容開始 ▼ -->

                <div class="alert alert-tip">
                  <strong>💡 30 秒速讀版：</strong>
                  <ul>
                    <li>重點一</li>
                    <li>重點二</li>
                  </ul>
                </div>

                <h2 id="toc-heading-0">第一章節標題</h2>
                <p>這是第一章節的內容...</p>

                <h2 id="toc-heading-1">第二章節標題</h2>
                <p>這是第二章節的內容...</p>

                <!-- ▲ 文章內容結束 ▲ -->

            </article>
        </div>
    </main>

    <footer class="site-footer">
        <!-- Footer 內容會由全局樣式和結構定義 -->
    </footer>

    <!-- 目錄生成腳本 -->
    <script>
    document.addEventListener('DOMContentLoaded', function() {
        const tocList = document.getElementById('toc-list');
        const article = document.querySelector('.article-container');
        if (!tocList || !article) return;

        const headings = article.querySelectorAll('h2');
        headings.forEach((heading, index) => {
            const id = heading.id || 'toc-heading-' + index;
            heading.id = id;
            const listItem = `<li><a href="#${id}">${heading.textContent}</a></li>`;
            tocList.innerHTML += listItem;
        });
    });
    </script>

</body>
</html>
```

### 步驟 2：更新文章總覽頁面 (`archive.html`)

1.  打開 `post/archive.html`。
2.  在 `<div class="archive-grid">` 內，複製一個現有的 `<div class="article-card">` 區塊並貼上。
3.  修改新卡片的內容：
    -   **`data-category`**：設定文章分類（如 `layer-2`, `infrastructure`, `analysis`）。
    -   **`data-published`** 和 **`data-modified`**：設定發布與修改日期，格式為 `YYYY-MM-DD`。
    -   修改標題、描述、關鍵字和連結，使其指向你的新文章。

### 步驟 3：更新網站地圖 (`sitemap.xml`)

1.  打開根目錄的 `sitemap.xml`。
2.  在 `</urlset>` 標籤前，新增一個 `<url>` 區塊。

    ```xml
    <url>
      <loc>https://lmybtc.github.io/post/project-name.html</loc>
      <lastmod>YYYY-MM-DD</lastmod>
      <changefreq>monthly</changefreq>
      <priority>0.8</priority>
    </url>
    ```
3.  將 `<loc>` 和 `<lastmod>` 更新為新文章的正確資訊。

### 步驟 4：品質保證 (QA)

在提交變更前，執行以下最終檢查：

-   [ ] **本地預覽**：在本地伺服器上打開新頁面，確認樣式正常。
-   [ ] **連結檢查**：點擊頁面上的所有內部和外部連結，確保它們都能正確跳轉，沒有 404 錯誤。
-   [ ] **主控台檢查**：按 `F12` 打開瀏覽器開發者工具，切換到 `Console` (主控台) 分頁，確認沒有任何紅色錯誤訊息。
-   [ ] **響應式檢查**：縮放瀏覽器視窗，或使用開發者工具的裝置模擬功能，檢查在手機寬度下排版是否正常，特別是圖片和表格。

---

## 🏆 進階最佳實踐 (Advanced Best Practices)

除了完成上述基本流程，遵循以下實踐能顯著提升網站的專業度和品質。

### 1. SEO 與無障礙性 (Accessibility)

-   **圖片替代文字 (Alt Text)**：為所有 `<img>` 標籤添加描述性的 `alt` 屬性。這不僅在圖片無法載入時提供備用資訊，更是螢幕閱讀器使用者理解圖片內容的唯一途徑，同時對 Google 圖片搜尋的 SEO 至關重要。
    ```html
    <img src="..." alt="一張圖表，顯示比特幣從2020到2024的價格走勢">
    ```
-   **語意化 HTML**：盡可能使用語意化標籤（如 `<article>`, `<section>`, `<figure>`, `<blockquote>`）來組織您的內容。這有助於搜尋引擎和輔助技術更好地理解您的頁面結構。
-   **友善的 URL**：文章的檔名應簡短、具描述性，並使用連字號 `-` 分隔單字。根據我們的最新規範，一般文章頁請直接使用「項目名稱.html」（例如 `chainlink.html`），主題頁則使用 `topic-[主題].html`。

### 2. 圖片優化

大型圖片是拖慢網站載入速度的主要元兇。在上傳任何圖片到專案之前，請務必進行壓縮。

-   **使用工具**：推薦使用 [TinyPNG](https://tinypng.com/) 或 [Squoosh](https://squoosh.app/) 等線上工具，可以在幾乎不影響視覺品質的情況下，將圖片檔案大小減少 50-80%。
-   **選擇格式**：
    -   **WebP**：優先考慮的現代格式，兼具品質與壓縮率。
    -   **JPEG**：適用於照片和複雜的漸層圖片。
    -   **PNG**：適用於需要透明背景的圖片（如 Logo）。

### 3. 版本控制 (Git)

一個清晰的 Git 提交歷史對於長期維護至關重要。當您新增一篇文章時，請使用以下格式撰寫 Commit Message：

```bash
feat(post): Add new article on [文章主題]

- 撰寫了關於 [文章主題] 的深度分析。
- 新增了對應的文章卡片和網站地圖條目。
```

**範例：**
`feat(post): Add new article on Bitcoin Layer 2 solutions`

### 4. 發布前自我審查 (Self-Review)

在您準備好提交變更之前，花五分鐘時間，像審查別人的程式碼一樣，重新檢查一次自己的變更。這個短暫的步驟能發現許多原本會被忽略的小錯誤。

-   **閱讀流暢性**：從頭到尾通讀一次文章，檢查是否有錯別字或不通順的語句。
-   **程式碼一致性**：檢查新加入的 HTML/CSS 是否遵循了專案現有的風格和縮排。
-   **最終確認**：再次對照本文件的快速檢查清單，確保沒有遺漏任何步驟。


---

> **注意**：關於專案的整體架構、技術棧和部署流程的更詳細資訊，請參閱根目錄的 `README.md` 檔案。
