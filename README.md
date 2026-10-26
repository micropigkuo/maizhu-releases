# 麥豬輸入法

Android 家庭測試版的下載與更新專用倉庫。

- [最新版本與安裝包](https://github.com/micropigkuo/maizhu-releases/releases/latest)
- 適用 ARM64 Android 手機，目前主要測試設備為 Samsung Galaxy S25。
- 本機語音使用 Qwen；雲端語音及潤飾使用 Gemini，由使用者自行設定 API key。
- 中文辭庫來自小麥注音，英文補字採 CMUdict，Emoji 關鍵字採 Unicode CLDR，輸入引擎使用 Rime。
- Qwen 權重由使用者在 App 選擇下載；個人學習資料、API key、憑證及錄音由使用者自行保存。

## 安裝與更新

首次安裝：在最新版本下載 `Maizhu-版本-arm64.apk`，依 Android 提示安裝，再於系統設定啟用並選取麥豬輸入法。

已有家庭版：進入 App「使用說明與授權 → 版本與更新」，頁面會自動檢查，也可按「檢查更新」。顯示新版後選「下載並安裝」，在系統畫面確認。原地更新保留資料；請保留既有 App，不解除安裝或清除資料。

背景約每日檢查一次，有新版時可發通知；時間受系統排程影響。下載與安裝由使用者確認。通知及安裝未知應用程式需使用者允許。

從舊測試套件首次搬移者，參考 [0.2.38 移轉說明](https://github.com/micropigkuo/maizhu-releases/releases/tag/v0.2.38)，模型另外下載。

## 0.2.40

- 修正字庫準備長時間不結束、英文可打但中文受阻的問題。
- 較長的設定說明顯示摘要，點選可展開全文。
- 更新頁提供「回復穩定版」入口。回復包由發布端指定，使用同簽章及相容的較高版本碼保留資料；目前尚未提供已完成手機驗收的回復包。詳見 [回復說明](https://github.com/micropigkuo/maizhu-releases/releases/download/v0.2.40/Stable-recovery-guide.md)。

184 項 JVM 單元測試、7 項資料驗收及方案名稱一致性檢查通過。本輪沒有 S25 連線，手機更新與畫面操作仍待實測。

## 來源與授權

每版附 `update.json`（版本、大小及 SHA-256）、`NOTICES.md`、`LICENSE.txt`。辭庫固定來源與生成工具見 [辭庫來源包](https://github.com/micropigkuo/maizhu-releases/releases/download/v0.2.39/Maizhu-open-lexicon-sources-0.2.39.zip)。完整辭庫聲明也可在 App「字庫來源與授權」閱讀。

主 App 原始碼保留於開發者的 TWIME 倉庫；需要對應修改及建置來源可於本倉庫 Issues 聯絡。本倉庫提供家庭測試版本，正式上架的素材、授權及政策審查另行處理。
