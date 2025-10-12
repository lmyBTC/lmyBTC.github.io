### 檔案用途與 AI 協作指南

> 這份 `todo.md` 文件是您與 AI 協作管理此網站開發專案的核心任務清單。它的主要目的是將大型的開發目標，拆解成清晰、可執行的步驟，並追蹤其進度。

**協作流程：**

1.  **您下達指令**：您向 AI 提出一個高層次的開發需求（例如：「將整個網站重構為使用 Tailwind CSS」或「新增一個『專案比較』功能頁面」）。
2.  **AI 拆解任務**：AI 會分析您的需求，將其拆解成數個邏輯上連貫的「階段 (Phase)」，並在每個階段下規劃出具體的「任務 (Task)」。
3.  **AI 記錄與更新**：AI 會將拆解後的計畫更新到這份文件中，並在每次完成一項任務後，標記其狀態。

**文件結構說明：**

*   `## Phase [編號]: [階段性目標] (預計完成日期: YYYY-MM-DD)`
    *   代表一個主要的開發里程碑。
    *   每個階段都應包含一個編號和預計的完成日期。

*   `*   **Task [編號.子編號]: [具體任務描述] (狀態)`
    *   是構成一個階段的具體執行步驟。
    *   **狀態** 包含：`(To Do)`、`(In Progress)` 或 `(Completed: YYYY-MM-DD)`。

---

## 任務 20240521-01: 建立「核心概念」系列文章頁面

根據 `post/topic-core.html` 的規劃，完成四篇核心概念文章的頁面建置，並確保其內容結構符合 `doc/writing-guide.md` 的規範。

---

### Phase 1: 建立文章模板與首篇文章 (預計完成日期: 2024-05-24)

*   **Task 1.1:** 根據 `writing-guide.md` 中的規範，建立一個可重複使用的文章頁面 HTML 模板 (`article-template.html`)。 (To Do)
*   **Task 1.2:** 使用新模板建立第一篇文章 `post/core-btc.html`，並填入符合指南的內容結構。 (To Do)
*   **Task 1.3:** 根據 `writing-guide.md` 的發布流程，將 `core-btc.html` 的資訊更新至 `archive.html` 與 `sitemap.xml`。 (To Do)

### Phase 2: 完成其餘核心概念文章 (預計完成日期: 2024-05-31)

*   **Task 2.1:** 複製模板，建立 `post/core-eth-alt.html` 頁面。 (To Do)
*   **Task 2.2:** 複製模板，建立 `post/core-meme.html` 頁面。 (To Do)
*   **Task 2.3:** 複製模板，建立 `post/core-rwa.html` 頁面。 (To Do)
*   **Task 2.4:** 將上述三篇文章的資訊，批次更新至 `archive.html` 與 `sitemap.xml`。 (To Do)
