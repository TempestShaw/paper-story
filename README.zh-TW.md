# Paper Story

**把研究主張、證據與關鍵實驗，組織成一篇論證清楚的論文。**

[English](README.md) · [Skill 主指令](skills/paper-story/SKILL.md) · [六種範式](skills/paper-story/references/archetypes.md) · [使用範例](examples/diagnosis.md) · [來源說明](skills/paper-story/references/sources.md)

Paper Story 是用於論文定位、實驗設計、學術寫作和審稿回覆的 Agent Skill。輸入研究想法、初步結果、實驗表格或論文草稿，它會幫你整理：**目前能主張什麼、還缺哪些證據，以及哪個實驗最可能改變結論。**

核心產物是「主張—證據對照表」：每個 contribution 都要對應適用範圍、來源、最強的替代解釋和下一步行動。

## 安裝與使用

在已安裝 Node.js/npm 和 Git 的環境中，透過 [Skills CLI](https://github.com/vercel-labs/skills) 安裝：

```bash
npx skills add TempestShaw/paper-story --skill paper-story
```

依安裝程式提示選擇支援的 agent 和安裝範圍。手動安裝時，把完整的 `skills/paper-story` 資料夾複製到客戶端文件指定的 skills 目錄，保留 `references/`、`assets/` 和 `agents/`。

在支援 `$skill-name` 的客戶端，可以這樣使用：

```text
使用 $paper-story，進入 diagnose 模式。
以下是我的研究問題、現有結果、最接近的相關工作和計算預算。
請找出目前最站得住腳的主張、最強的替代解釋，
以及最值得先做的一個驗證實驗。
```

套件採用 [Agent Skills 格式](https://agentskills.io/specification)，由 Markdown 指令、範本與可選的介面 metadata 組成，沒有執行期程式、必要 API key 或自動啟動實驗的功能。有瀏覽能力時可核對文獻與會議規則；沒有時就根據提供的材料分析，清楚標示未核實事項。各客戶端的安裝行為請以其文件為準。

## 五種模式

| 模式 | 適合的問題 | 主要產出 |
| --- | --- | --- |
| `diagnose` | 這個項目到底有什麼論文貢獻？ | 有邊界的主張、敘事選擇、替代解釋、關鍵下一步 |
| `design` | 要做什麼實驗才能支持這個說法？ | 主張—證據表、按優先次序排列的實驗地圖 |
| `draft` | 幫我寫摘要、Introduction 或大綱。 | 符合證據強度的文字；缺結果處保留明確佔位符 |
| `review` | 用審稿人的角度找問題。 | 對應具體段落的質疑、影響、最小修正與較窄的主張 |
| `rebuttal` | 幫我回覆審稿意見。 | 區分既有證據、已完成補充、尚未執行計劃與合理讓步的回覆 |

可用中文或英文提問；分析跟隨你的語言，論文文字保留原文語言，除非你要求翻譯。只改一句時，就處理那一句。

## 六種敘事範式

| 範式 | 需要站得住腳的地方 |
| --- | --- |
| **根因診斷** | 有足夠證據區分提出的機制與其他解釋。 |
| **重新檢視假設** | 確認原有假設存在，並在公平比較下找出失效條件。 |
| **理論解釋經驗** | 清楚的假設與有效推導，支持有範圍的解釋或預測。 |
| **評測揭露盲點** | 新量尺確實測到重要能力，且排除了捷徑和評分偏差。 |
| **真實世界影響** | 實際檢驗相關人的結果、使用條件、成本和限制。 |
| **統一抽象** | 共通表徵帶來有用的對應、簡化或新的可驗證推論。 |

每次選一條主線，最多加一條輔線，也可以不套任何一種。重現研究、負面結果、描述性研究和漸進式改進，都可以按自身貢獻成立。這些是實用的研究思考工具，沒有中稿率評分，也不保證獲獎。

每種範式都包含：適用條件、論證骨架、最低證據要求、可能推翻它的結果、建議圖表、常見過度宣稱，以及證據不足時的替代表述。

## 簡單例子

**以下為虛構情境與數字：** 文件處理 agent 在 100 個複合任務中，成功數由 52 提升至 78；新版本同時增加具名中間產物、validator，以及三倍推理 token，只測了一個 training seed。

Skill 會指出：這個比較可以支持進一步研究整套改動，還不能把提升歸因於「中間產物引用不清」這個根因。下一步應先匹配 token 預算，再分開檢查表徵和 validator 的作用。該樣本的差異是 **26 個百分點**，可靠性與歸因仍待驗證。

完整範例：[研究定位](examples/diagnosis.md) · [結果未完成時的摘要](examples/abstract-before-results.md)。公開範例均為虛構，不包含私人研究內容。

## 四份可重用範本

| 範本 | 用途 |
| --- | --- |
| [研究簡報](skills/paper-story/assets/paper-brief.md) | 對齊研究問題、核心主張、相關工作、限制與下一個決策。 |
| [主張—證據表](skills/paper-story/assets/claim-evidence-ledger.md) | 區分已檢查、轉述、假設、計劃、矛盾和未知。 |
| [實驗地圖](skills/paper-story/assets/experiment-map.md) | 為每個測試列出問題、對照、替代解釋、預算與推翻條件。 |
| [審稿與回覆表](skills/paper-story/assets/review-and-rebuttal.md) | 讓質疑和回覆對應到實際段落與已完成工作。 |

VERIFIED 只代表已檢查的材料支持該範圍內的陳述，不代表普遍成立或已獨立重現。範本按需要使用，不要求每次填滿。

## 方法原則

- 分開觀察、解釋、介入和計劃。
- 每項主張都保留證據的適用範圍與限制。
- 保留負面結果、不確定性、單位、分母和比較預算。
- 用文獻核對新穎性；用驗證檢查量尺是否合理。
- 未完成實驗也能寫草稿，缺結果處使用明確佔位符。
- 預算有限時，優先安排最可能改變結論的測試。
- 不編造引用、數據、證明、審稿意見或已完成的工作。

方法參考包括 [NeurIPS checklist](https://neurips.cc/public/guides/PaperChecklist)、[Pineau 等人的可重現性研究](https://jmlr.org/papers/v22/20-303.html)和 [Dodge 等人的實驗報告研究](https://aclanthology.org/D19-1224/)。具體來源和適用限制見[來源說明](skills/paper-story/references/sources.md)。

## 驗證與限制

參見[評估案例](evals/README.md)與[首次驗證記錄](evals/validation.md)。這些檢查涵蓋格式和虛構任務上的行為，不構成科學正確性、所有客戶端相容性或投稿效果的證明。引用、分析和正式論文主張仍須核對。

## 靈感與致謝

靈感來自使用者提供、文中署名「人工智能学社」的〈Story Is All You Need：扒透35篇顶会最佳/杰出论文的叙事密码，我们找到了六大范式〉。原文網址和發表日期尚未獨立核實；部分獎項已對照官方資料，但沒有逐篇審核全部 35 篇的技術總結。

本倉庫提供原創的操作流程、判斷規則、範本與虛構範例，不轉載文章全文或論文圖表。完整核對範圍見[來源說明](skills/paper-story/references/sources.md)。

## 貢獻與授權

歡迎改善證據判斷、任務涵蓋、範例和指令精簡度，詳見 [CONTRIBUTING.md](CONTRIBUTING.md)。

[MIT License](LICENSE)，copyright © 2026 Victor Kwong。授權涵蓋本倉庫的原創檔案，外部文章、論文和軟體保留各自權利與授權。
