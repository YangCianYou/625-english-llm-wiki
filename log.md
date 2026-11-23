# 維護紀錄

## [2026-11-23] discussion-confirmed | 正式啟動 Wiki

- 使用者確認以 625 英文學習法作為 LLM Wiki 主題。
- 建立 `wiki/discussion-record.md`，保存受眾、目標、單字卡欄位、學習節奏與 AI 風險決策。
- 本次先完成 Wiki 與五份來源 ingest；HTML 簡報留待下一階段，需先由使用者確認 Wiki 結構與來源方向。

## [2026-11-23] ingest-verified | 使用者指定五份資料

- 使用者確認第一批來源固定為：625 法影片、Fluent Forever Appendix 5、LL2019、Cepeda et al. (2006)、Your First 625。
- 將使用者提供的三份 PDF 原檔保存到 `rawpaper/`，並核對其 SHA-256。
- 建立 `wiki/synthesis.md`，區分方法說明、詞表內容、發音研究與複習研究各自可支持的主張。

## [2026-11-23] generate | Wiki → 教學 HTML 簡報

- 查詢 `wiki/synthesis.md`、概念頁與 `teaching-rationale.md`，建立 10 張給初學者的 HTML 簡報。
- 每張含重要主張的投影片皆標示 Wiki 對應頁與來源代號。
- 未將方法提出者的建議誇大為已保證的學習成效。

## [2026-11-23] setup | 建立 625 英文學習法 LLM Wiki 骨架

- 與使用者確認：教學導向為「同學今天開始實行 625 法」。
- 確認：內文使用繁體中文（台灣慣用語）；英文術語、模型名稱、指標與論文題名保留原文。
- 確認：論文／來源頁採選項 A 命名 `P-YYYY-ShortName.md`；概念頁採小寫 kebab-case。
- 確認：不綁定 Anki、Quizlet 或紙本卡；提供 30 天與 3 個月版本。
- 新增：`rawpaper/`、`wiki/`、概念頁、來源登錄、教學推導頁與 `AGENTS.md`。
- 新增來源登錄：`P-2014-Wyner625`，待完整 ingest。
- 待辦：討論、選定並逐一 ingest 其餘至少 4 份來源。

## [2026-11-23] ingest | 完成五份來源整合

- Ingest `P-2014-Wyner625`：確認字表為 625 個具體日常詞彙的資源；不把字表本身當成成效證據。
- Ingest `S-UND-WynerVideo`：保存使用者提供的 625 法流程摘要，標記為方法參考而非獨立實證。
- Ingest `S-2014-FFAppendix`：登錄官方 625 Word List 資源頁，用以界定方法脈絡。
- Ingest `P-2006-CepedaSpacing`：更新 spaced repetition、active recall 與兩種學習計畫的證據邊界。
- Ingest `P-2019-SaitoPlonskyPronunciation`：更新 pronunciation 頁，將發音活動改為可觀察的聽辨與受控產出練習。
- 檢查結果：已達 5 / 5 來源；發現原先「待 ingest」的教學推導仍留在表中，下一次 lint 須改成已整合狀態或刪除重複項。

## [2026-11-23] lint + generate | 修正推導表並產生教學 HTML 簡報

- Lint：移除 `teaching-rationale.md` 中已被研究來源取代的兩筆「待 ingest」列。
- Lint：補上 `study-plans.md` 的間隔複習來源。
- Generate：完成 8 張 HTML 投影片，放入 `outputs/slides/625-teaching-challenges/`。
- Validate：每張投影片只使用 Wiki 已整理的教學主張；發音頁對應 `P-2019-SaitoPlonskyPronunciation`，複習與進度頁對應 `P-2006-CepedaSpacing`。
