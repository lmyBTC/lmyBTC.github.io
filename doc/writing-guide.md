# ✍️ LMY's Crypto Blog - 文章風格指南

這份文件旨在為所有 `LMY's Crypto Blog` 的文章建立一套統一、高標準的風格與結構。遵循此指南將有助於我們產出高品質、風格一致且對讀者極具吸引力的內容。

> **技術檢查清單請參考** [`doc/new-page-checklist.md`](new-page-checklist.md) - 專注於 HTML 結構、SEO 設定等技術層面。

---

## 總體風格與核心理念

文章的整體風格應為**「專業、權威、具前瞻性」**。我們透過嚴謹的數據分析建立權威，用深入淺出的方式解釋複雜的技術與市場動態，並為讀者提供具備前瞻性的洞察。

---

## 內容策略與結構

### 問題解決導向敘事 (PSMA 流程)

為提升閱讀完成率與讀者洞察，建議採用「PSMA：Pain → Solution → Mechanism → Action」的敘事順序，將資訊陳列調整為「問題解決導向」。

- **Pain (痛點)**：用讀者語言點名困擾與族群 (例如：高昂的 Gas Fee、網路壅塞、找不到 Alpha)，建立共鳴。
- **Solution (解方)**：給出此協議/技術作為核心解方與關鍵價值主張。
- **Mechanism (原理)**：挑重點講技術，用 1-2 個關鍵機制詞彙 (例如：ZK-Rollups、去中心化預言機)，讓說服更有力。
- **Action (行動)**：提供清晰的指南 (例如：如何參與生態、評估專案、避開風險)，讓讀者可以實際應用。

### 標準文章結構 (模組化)

每篇文章都應遵循以下核心章節結構，以確保內容的完整性。在包含這8個核心章節的前提下，作者可根據主題的深度與廣度，自由增加額外的延伸章節。

1.  **`<h2>` 基本資訊：[協議/技術]是什麼？**
    -   **目的**：建立基礎認知。
    -   **內容**：定義與分類、比較不同技術路徑的差異 (例如：Optimistic vs. ZK Rollups)。

2.  **`<h2>` 核心價值：[協議/技術]解決了什麼問題？**
    -   **目的**：闡述其核心價值主張 (Value Proposition)。
    -   **內容**：使用 `.info-cards` 樣式，列出 3-4 個最核心的解決方案。

3.  **`<h2>` 代幣經濟學與關鍵指標**
    -   **目的**：提供量化數據以評估其價值。
    -   **內容**：使用 `.data-table` 呈現代幣總量、通膨率、市值、TVL、活躍用戶數等關鍵指標。

4.  **`<h2>` 生態系發展：有哪些主要專案？**
    -   **目的**：展示其生態系的廣度與活力。
    -   **內容**：介紹其生態系中的主要 dApp 或合作夥伴。

5.  **`<h2>` 目標客群與應用場景**
    -   **目的**：精準定位其市場。
    -   **內容**：分析該技術主要為開發者、交易員還是企業用戶服務，並列舉典型應用場景。

6.  **`<h2>` 如何評估與比較？**
    -   **目的**：提供決策框架。
    -   **內容**：使用 `.comparison-table` 比較相似協議的優缺點，並提供評估框架。

7.  **`<h2>` 風險與挑戰**
    -   **目的**：建立信任感，展現內容的完整與客觀。
    -   **內容**：說明技術風險、經濟模型風險、中心化風險等。務必加入 `<div class="alert alert-warning">` 的風險提示。

8.  **`<h2>` 常見問題 (FAQ)**
    -   **目的**：解答讀者的次要疑問。
    -   **內容**：以 Q&A 形式，回答 3-5 個常見問題。

### 標題撰寫策略：V.I.P. + B.R.A.V.E. 混合框架

-   **核心要求**：標題不怕長，但**必須**精準且全面，融合 V.I.P. 與 B.R.A.V.E. 框架的元素，但**首要原則是「文要對題」**。
-   **V.I.P. 框架 (內容核心)**
    -   **V (Value-Driven - 價值驅動):** 明確點出對讀者的核心**益處** (例如：尋找下一個 Alpha)。
    -   **I (Intriguing - 引發好奇):** 使用**比喻、提問或知識缺口** (例如：Stacks 和閃電網路誰是未來？)。
    -   **P (Problem-Solving - 解決問題):** 直接命中讀者的**痛點** (例如：比特幣網路擁堵、手續費高)。
-   **B.R.A.V.E. 框架 (點擊觸發器)**
    -   **B (Brand - 品牌):** 在標題結尾加入「**| LMY's Crypto Blog**」。
    -   **R (Recentness - 時效性):** 若內容具時效性，可加入**年份** (例如：「2025年」)。
    -   **A (Amount - 數量):** 使用**具體數字** (例如：「3大主流方案」)。
    -   **V (Velocity - 速度):** 強調**效率** (例如：「5分鐘搞懂」)。
    -   **E (Economy - 經濟性):** 強調**免費或高CP值** (例如：「完整指南」)。

-   **綜合應用範例**：
    -   `比特幣 Layer 2 - 2025年尋找下個 Alpha：5分鐘搞懂 Stacks、閃電網路等3大主流方案的完整指南 | LMY's Crypto Blog`

---

## 內容與語氣

-   **專業口吻**：適時使用「**技術重點**」、「**風險提示**」等提示框，增加內容的權威性。
-   **善用比喻**：將複雜的技術概念轉化為簡單易懂的比喻 (例如：*閃電網路是比特幣主幹道旁的「高速公路」*)。
-   **強調重點**：對於段落中的關鍵字詞，使用 `<strong>` 標籤或 `<span class="highlight-term">` 來凸顯。
-   **讀者觀點**：從讀者會遇到的具體問題出發，讓文章內容能真正解決他們的問題。
-   **精簡圖示**：**原則上禁止使用任何裝飾性圖示（包含 Emoji）**，以維持版面的專業性。僅在功能性提示框中由 CSS 自動添加。

---

## 格式化與常用 CSS Class

### 1. 提示框 (`.alert`)
   - **一般提示**：`class="alert alert-tip"` (藍色系)
   - **技術重點**：`class="alert alert-tech"` (綠色系)
   - **風險警告**：`class="alert alert-warning"` (紅色系)

   ```html
   <div class="alert alert-tech">
     <strong>技術重點：</strong> Ordinals 協議利用了比特幣 Taproot 升級的特性。
   </div>
   ```
   > **CSS 實作**：圖示應由 CSS `::before` 偽元素添加，而非手動插入。例如：`.alert-tech > strong::before { content: '💡'; margin-right: 8px; }`

### 2. 資訊卡片 (`.info-cards`)
   - 用於並列呈現 3-4 個核心觀點或價值主張。

   ```html
   <div class="info-cards">
     <div class="info-card">
       <h4 class="info-card-title">高速交易</h4>
       <p class="info-card-desc">提供近乎即時且低成本的交易體驗。</p>
     </div>
     <!-- more cards... -->
   </div>
   ```

### 3. 比較表格 (`.comparison-table`)
   - 用於多個協議的詳細優劣比較。

   ```html
   <div class="comparison-table-container">
       <table class="comparison-table">
           <thead>
               <tr>
                   <th>比較項目</th>
                   <th>協議 A (推薦)</th>
                   <th>協議 B</th>
               </tr>
           </thead>
           <tbody>
               <tr>
                   <td>交易速度</td>
                   <td>~1,000 TPS</td>
                   <td>~100 TPS</td>
               </tr>
               <!-- more rows... -->
           </tbody>
       </table>
   </div>
   ```

### 4. 數據表格 (`.data-table`)
   - 用於呈現代幣經濟學或生態數據。

   ```html
   <table class="data-table">
     <thead>
       <tr><th>排名</th><th>項目</th><th>TVL</th></tr>
     </thead>
     <tbody>
       <tr><td>🥇 TVL 冠軍</td><td><strong>Merlin Chain</strong></td><td><strong>$2.5B</strong></td></tr>
       <!-- more rows... -->
     </tbody>
   </table>
   ```

---

## 發布前檢查

在您完成一篇文章的撰寫後，請務必完成以下兩個關鍵步驟，以確保網站的完整性：

1.  **更新文章總覽頁面**：手動打開 `/post/archive.html` 檔案，將新文章的卡片資訊新增至列表頂端。
2.  **更新 Sitemap**：手動打開 `/sitemap.xml` 檔案，加入新文章的 `<url>` 資訊。

> 更詳細的檢查清單，請參考 `doc/new-page-checklist.md` 文件。

---

## SEO 與 Metadata

1.  **基礎 Meta 標籤**：確實填寫 `<title>`、`<meta name="description">` 和 `<meta name="keywords">`。
    -   `description` 應控制在 150 字元左右，並包含核心關鍵字。

2.  **JSON-LD 結構化資料**：**此為必填項目**。請務G必複製並修改以下範本，填入正確的文章資訊。

    ```html
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Article",
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://lmybtc.github.io/post/your-new-page.html" // 修改為新頁面的完整網址
      },
      "headline": "文章主標題",
      "description": "文章的詳細描述",
      "author": {
        "@type": "Organization",
        "name": "LMY's Crypto Blog",
        "url": "https://lmybtc.github.io/"
      },
      "publisher": {
        "@type": "Organization",
        "name": "LMY's Crypto Blog"
      },
      "datePublished": "YYYY-MM-DD",
      "dateModified": "YYYY-MM-DD"
    }
    </script>
    ```
