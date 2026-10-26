# 麥豬輸入法

Android 家庭測試版的下載與更新專用倉庫。

- [最新版本與安裝包](https://github.com/micropigkuo/maizhu-releases/releases/latest)
- 適用 ARM64 Android 手機，目前主要使用設備為 Samsung Galaxy S25。
- APK 不含個人 API key、登入憑證、學習辭庫、錄音或 ASR 模型權重。
- Qwen 模型需在 App 內由使用者選擇下載；Gemini 需自行提供 API key。

## 安裝與更新

首次安裝：從最新版本下載 `Maizhu-版本-arm64.apk`，依 Android 提示安裝，再於系統設定啟用並選取麥豬輸入法。

已安裝家庭版：開啟 App 的「使用說明與授權 → 版本與更新」，進入頁面會自動檢查，也可按「檢查更新」。顯示新版後按「下載並安裝」，依系統提示確認。請勿先解除安裝或清除資料，原地更新會保留個人設定、學習資料及已下載模型。

約每日一次的背景檢查可通知新版，實際時間受 Android 排程影響。通知及安裝未知應用程式需要使用者允許；更新不會靜默安裝。

舊測試版與家庭版是不同套件，首次搬移請保留舊版，參考 [0.2.38 移轉說明](https://github.com/micropigkuo/maizhu-releases/releases/tag/v0.2.38)。模型另行下載。

Google 有限發布方案的裝置授權另由開發者邀請管理，本倉庫不代表免除 Android 的安裝限制。

## 0.2.39 開源辭庫替換

內建中文字音、詞語與詞頻改由小麥注音重建；英文補字使用 CMUdict，Emoji 使用 Unicode CLDR。APK 不再包含先前提取的 SogaType 辭庫與聯想資料。候選排序可能改變，更新後第一次開啟鍵盤會檢查並重建字庫快取。

180 項 JVM 單元測試、7 項資料驗收與桌面 Rime 引擎案例通過。本輪未連接 S25，手機首次升級與更新端到端流程仍待實測。

每個版本附 `update.json`（版本、長度與 SHA-256）、`NOTICES.md` 及 `LICENSE.txt`。0.2.39 另附辭庫來源、生成工具及重建說明；主 App 原始碼保留於開發者的 TWIME 倉庫，需要本版修改及建置來源可透過本倉庫 Issues 聯絡。

這是家庭測試版，辭庫來源可追溯不代表整個 App 的其他素材、授權及 Play Store 審查已完成。詳見該版本的 NOTICES 與 Open-lexicon-guide。歷史版本的資產與限制以各版本說明為準。
