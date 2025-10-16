# ✍️ CryptoCompound - 文章風格指南

這份文件旨在為所有 `CryptoCompound` 的文章建立一套統一、高標準的風格與結構。遵循此指南將有助於我們產出高品質、風格一致且對讀者極具吸引力的內容。

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
    -   **B (Brand - 品牌):** 在標題結尾加入「**| CryptoCompound**」。
    -   **R (Recentness - 時效性):** 若內容具時效性，可加入**年份** (例如：「2025年」)。
    -   **A (Amount - 數量):** 使用**具體數字** (例如：「3大主流方案」)。
    -   **V (Velocity - 速度):** 強調**效率** (例如：「5分鐘搞懂」)。
    -   **E (Economy - 經濟性):** 強調**免費或高CP值** (例如：「完整指南」)。

-   **綜合應用範例**：
    -   `比特幣 Layer 2 - 2025年尋找下個 Alpha：5分鐘搞懂 Stacks、閃電網路等3大主流方案的完整指南 | CryptoCompound`

---

## 內容與語氣

### 1. **專業口吻**
   - 適時使用「**分析師洞察**」、「**風險提示**」等提示框，增加內容的權威性。

### 2. **善用比喻**
   - 將複雜的技術概念轉化為簡單易懂的比喻。例如：
     - *Chainlink 是區塊鏈與現實世界之間的「數據橋樑」。*
     - *Layer 2 是以太坊主網的「高速公路」。*

### 3. **強調重點**
   - 對於段落中的關鍵字詞與數據，使用 `<strong>` 標籤或 `<span class="highlight-term">` 來凸顯。

### 4. **善用讀者觀點**
   - 在撰寫前，先思考讀者為何會搜尋這個主題？他們可能遇到了什麼具體問題（例如：Gas Fee 太高、找不到 Alpha），或是有什麼樣的目標（例如：對抗通膨、尋求高額回報）。
   - 從讀者會遇到的日常生活情境出發，分析其背後的意圖與困難，讓文章內容能真正解決他們的問題，而不只是單純的知識陳列。

### 5. **精簡圖示 (Icon) 使用**
   - **原則禁止，例外手動**：為維持版面的專業性與內容的純粹性，**原則上禁止使用任何裝飾性圖示（包含 Emoji）**。
   - 任何圖示的出現，都應是經過審慎評估後，由編輯**手動明確加入**的，絕非自動或常規性添加。
   - 目標是讓視覺焦點完全回歸內容本身，避免任何不必要的視覺干擾。

### 6. **全面專業潤稿 (Full-Pass Proofreading)**
   - **目標**：在完成初稿後，進行一次徹底的專業潤稿，根除所有可能削弱文章權威性的元素。
   - **核心原則**：
     - **消除「內容農場」語氣**：避免使用過於聳動、誇大或缺乏根據的語句。
     - **整合專家觀點**：將「分析師洞察」、「風險提示」等外部標籤，無縫地融入文章的論述脈絡中。讓內容本身直接展現其專業性，而非依賴標籤。
     - **統一沉穩語氣**：確保整篇文章的語氣一致、沉穩且充滿信賴感，避免過於口語化的表達。
     - **優化起承轉合**：檢查各段落間的邏輯連接，確保行文流暢，論述結構嚴謹。
   - **最終成果**：潤稿後的文章應是一份精雕細琢的權威指引，而非僅僅是資訊的堆砌。

### 7. **優化提示框文字分段**
   - 在使用 `.alert` 提示框（如「分析師的投資框架」）時，應適度將長句切分為短句或條列式，以加強語氣和視覺指引，讓核心建議更清晰有力。


---
## 格式化與常用 CSS Class

為了維持視覺上的一致性，請多加利用以下預設的 CSS 樣式。

> **重要規則：** 為維持版面的專業性與內容的純粹性，**原則上禁止在文章內使用任何裝飾性圖示（包含 Emoji）**。所有範例均不應包含圖示，以確保視覺焦點完全回歸內容本身。

### 1. **提示框 (`.alert`)**
   - **一般提示**：`class="alert alert-tip"` (綠色系)
   - **分析師洞察**：`class="alert alert-analyst"` (藍色系)
   - **風險提示**：`class="alert alert-warning"` (紅色系)
   - **排版說明**：提示框的 `<strong>` 標題為區塊元素 (block)，會獨立成行，與下方內容分離，以增強可讀性。

   ```html
   <div class="alert alert-analyst">
     <strong>分析師洞察：</strong>
     <p>比特幣的非對稱回報特性，使其成為機構投資者資產配置中重要的 Alpha 增強劑。</p>
   </div>
   ```

### 2. **資訊卡片 (`.info-cards`)**
   - 用於並列呈現核心觀點或價值主張。
   - **排版規則**：為了維持在所有裝置上的最佳閱讀體驗與排版，一個 `.info-cards` 區塊中，**不應放置超過 3 張**資訊卡片 (`.info-card`)。

   ```html
   <div class="info-cards">
     <div class="info-card">
       <h4 class="info-card-title">價值主張一</h4>
       <p class="info-card-desc">說明此價值主張的詳細內容...</p>
     </div>
     <!-- more cards... -->
   </div>
   ```

### 3. **風險類型卡片 (`.risk-card`)**
   - 用於強調不同類型的投資風險。

   ```html
    <div class="risk-group-cards">
      <div class="risk-card">
        <div class="risk-card-header">
          <h4 class="risk-card-title">技術風險</h4>
        </div>
        <p class="risk-card-desc">智能合約可能存在漏洞，導致資金被盜。</p>
      </div>
      <!-- more cards... -->
    </div>
   ```

### 4. **數據表格 (`.data-table`)**
   - 用於呈現代幣經濟學、市場數據等量化資訊。

   ```html
   <table class="data-table">
     <thead>
       <tr><th>指標</th><th>數值</th><th>說明</th></tr>
     </thead>
     <tbody>
       <tr><td>市值</td><td><strong>$1.2T</strong></td><td>截至 2025 Q4</td></tr>
       <!-- more rows... -->
     </tbody>
   </table>
   ```

### 5. **進階比較表格 (`.comparison-table`)**
   - 用於多個協議或技術方案的詳細優劣比較，特別是當有「推薦選項」時。
   - 此表格設計更具視覺引導性，能幫助讀者快速抓住重點。

   ```html
   <div class="comparison-table-container">
       <table class="comparison-table">
           <thead>
               <tr>
                   <th class="comparison-header-main">比較項目</th>
                   <th class="comparison-header-option">
                       <div class="option-badge">推薦</div>
                       <strong>方案 A (Optimistic Rollup)</strong>
                   </th>
                   <th class="comparison-header-option comparison-recommended">
                       <strong>方案 B (ZK Rollup)</strong>
                   </th>
               </tr>
           </thead>
           <tbody>
               <tr class="comparison-row">
                   <td class="comparison-label">生物利用率</td>
                   <td class="comparison-cell comparison-recommended">
                       <div class="rating-badge rating-high">中</div>
                   </td>
                   <td class="comparison-cell">
                       <div class="rating-badge rating-very-high">高</div>
                   </td>
               </tr>
               <tr class="comparison-row">
                   <td class="comparison-label">優缺點</td>
                   <td class="comparison-cell comparison-recommended">
                       <div class="pros-cons">
                           <div class="pros">+ EVM 兼容性高、技術成熟</div>
                           <div class="cons">- 提款等待期長</div>
                       </div>
                   </td>
                   <td class="comparison-cell">
                       <div class="pros-cons">
                           <div class="pros">+ 安全性高、提款快速</div>
                           <div class="cons">- EVM 兼容性較差、生成證明計算量大</div>
                       </div>
                   </td>
               </tr>
           </tbody>
       </table>
   </div>
   ```
   > **注意**: 此表格的完整 CSS 樣式較為複雜，已內建於各文章頁面的 `<style>` 區塊中。

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
        "name": "Crypto Compound",
        "url": "https://lmybtc.github.io/"
      },
      "publisher": {
        "@type": "Organization",
        "name": "Crypto Compound"
      },
      "datePublished": "YYYY-MM-DD",
      "dateModified": "YYYY-MM-DD"
    }
    </script>
    ```
