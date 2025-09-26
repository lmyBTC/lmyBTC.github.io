# 📋 新增頁面檢查清單

當您要為網站新增頁面時，請按照以下步驟確保頁面完整且符合網站標準。

## 🎯 快速檢查清單

- [ ] 建立 HTML 檔案
- [ ] 加入 GA4 分析組件
- [ ] 加入 Header 組件
- [ ] 加入 Footer 組件
- [ ] **更新文章彙整頁面**
- [ ] **新增內部連結**
- [ ] 更新 sitemap.xml
- [ ] **最終驗證**

---

## 📝 詳細步驟指南

### 1️⃣ **建立基本 HTML 結構**

使用以下模板作為新頁面的起點：

```html
<!DOCTYPE html>
<html lang="zh-TW">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>頁面標題 | CryptoPulse</title>
    <meta name="description" content="頁面描述（建議 150-160 字元）" />
    <meta name="keywords" content="關鍵字1, 關鍵字2, 關鍵字3" />
    
    <!-- Favicon -->
    <link rel="icon" type="image/svg+xml" href="../favicon.svg">
    <link rel="shortcut icon" type="image/svg+xml" href="../favicon.svg">

    <!-- JSON-LD for Structured Data (SEO) -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Article",
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://your-crypto-pulse-domain.xyz/post/your-new-page.html"
      },
      "headline": "文章主標題",
      "description": "文章的詳細描述",
      "image": "https://your-crypto-pulse-domain.xyz/assets/images/your-og-image.jpg",
      "author": {
        "@type": "Organization",
        "name": "CryptoPulse",
        "url": "https://your-crypto-pulse-domain.xyz/"
      },
      "publisher": {
        "@type": "Organization",
        "name": "CryptoPulse",
        "logo": {
          "@type": "ImageObject",
          "url": "https://your-crypto-pulse-domain.xyz/assets/images/logo-for-google.png"
        }
      },
      "datePublished": "YYYY-MM-DD",
      "dateModified": "YYYY-MM-DD"
    }
    </script>

    <style>
      /* 頁面樣式 */
    </style>
  </head>
  <body>
    <!-- Header Component Container -->
    <div id="header-component"></div>

    <!-- 主要內容區域 -->
    <main>
      <!-- 您的頁面內容 -->
    </main>

    <!-- Footer Component Container -->
    <div id="footer-component"></div>

    <!-- Load Components -->
    <script src="../assets/js/deus-analytics-component.js"></script>
    <script src="../assets/js/deus-header-component.js"></script>
    <script src="../assets/js/deus-footer-component.js"></script>

    <script>
      // 初始化組件
    </script>
  </body>
</html>
```

### 2️⃣ **加入 GA4 分析追蹤**

在 `<script>` 標籤中加入以下初始化代碼：

```javascript
// Initialize Components
document.addEventListener("DOMContentLoaded", function () {
  // Initialize Analytics Component
  if (window.DeusAnalyticsComponent) {
    new window.DeusAnalyticsComponent().setDebug(false).setEnvironment("production");
  }

  // 其他組件初始化...
});
```

### 3️⃣ **加入 Header 組件**

在初始化代碼中繼續加入：

```javascript
// Initialize Header Component
const headerContainer = document.getElementById("header-component");
if (headerContainer && window.DeusHeaderComponent) {
  new window.DeusHeaderComponent(headerContainer).setDebug(false);
}
```

### 4️⃣ **加入 Footer 組件**

在初始化代碼中加入：

```javascript
// Initialize Footer Component
const footerContainer = document.getElementById("footer-component");
if (footerContainer && window.DeusFooterComponent) {
  new window.DeusFooterComponent(footerContainer).setDebug(false);
}
```

### 5️⃣ **更新文章彙整頁面**

若新增的是文章頁面，請打開 `/post/archive.html`，手動新增該篇文章的卡片資訊，以確保目錄同步更新。

### 6️⃣ **新增內部連結**

思考新頁面與既有頁面的關聯性，在至少 1-2 個相關的舊頁面中，加入連向此新頁面的文字連結，以建立更緊密的站內連結結構。

### 7️⃣ **更新 sitemap.xml**

打開 `/sitemap.xml` 檔案，在 `</urlset>` 標籤前加入新頁面：

```xml
<url>
  <loc>https://your-crypto-pulse-domain.xyz/post/your-new-page.html</loc>
  <lastmod>YYYY-MM-DD</lastmod>
  <changefreq>monthly</changefreq>
  <priority>0.8</priority>
</url>
```

**優先級建議：**

- 首頁: `1.0`
- 重要文章/分類頁: `0.8`
- 一般文章: `0.6-0.7`
- 輔助頁面: `0.4-0.5`

**更新頻率建議：**

- `daily`: 每日更新的內容
- `weekly`: 每週更新的內容
- `monthly`: 每月更新的內容
- `yearly`: 很少更新的內容

### 8️⃣ **最終驗證**

- **響應式檢查**：在桌面和手機兩種尺寸下，檢查頁面排版是否正常。
- **連結檢查**：點擊頁面上的所有連結，確保沒有失效連結 (404)。
- **主控台檢查**：在瀏覽器中打開開發者工具 (F12)，確認 Console 面板沒有任何紅色錯誤訊息。

### 9️⃣ **路徑注意事項**

根據頁面位置調整腳本路徑：

| 頁面位置                             | 腳本路徑範例                   |
| ------------------------------------ | ------------------------------ |
| 根目錄 `/index.html`                 | `src="assets/js/xxx.js"`       |
| 子目錄 `/post/xxx.html`              | `src="../assets/js/xxx.js"`    |
| 二級子目錄 `/post/category/xxx.html` | `src="../../assets/js/xxx.js"` |

---

## 📚 專案技術參考

此處記錄專案的技術細節與部署流程，作為維護時的參考。

### 🚀 專案特色

- **現代化設計**：採用深色主題，提供專注的閱讀體驗。
- **靜態化生成**：純 HTML/CSS/JS，無需複雜後端，易於部署在 GitHub Pages 或任何靜態主機上。
- **組件化**：頁首 (Header)、頁尾 (Footer) 和分析 (Analytics) 均為可重用組件。
- **SEO 友好**：內建 JSON-LD 結構化資料和標準 Meta 標籤，優化搜尋引擎排名。
- **響應式設計**：自動適應桌面、平板和手機裝置。

### 🛠️ 技術堆疊

- **HTML5**
- **CSS3** (使用 CSS 變數)
- **JavaScript (ES6)**

### 🏗️ 專案結構

```
lmyBTC.github.io/
├── index.html                   # 網站首頁
├── post/                        # 文章目錄
├── assets/                      # 靜態資源 (CSS, JS, 圖片)
├── doc/                         # 專案文件
├── .github/workflows/deploy.yml # 自動化部署腳本
├── sitemap.xml                  # 網站地圖
└── README.md                    # 專案入口
```

### 自動化部署

本專案已設定 GitHub Actions (`.github/workflows/deploy.yml`)。當 `main` 分支有任何更新時，會自動將網站內容部署到公開的 `lmyBTC/lmyBTC.github.io` 倉庫。