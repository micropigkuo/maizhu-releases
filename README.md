# 麥豬輸入法

Android 家庭測試版的下載與更新專用倉庫。

- [最新版本與安裝包](https://github.com/micropigkuo/maizhu-releases/releases/latest)
- 適用 ARM64 Android 手機；目前主要使用設備為 Samsung Galaxy S25。
- APK 不含個人 API key、登入憑證、學習辭庫、錄音或 ASR 模型權重。
- Qwen 模型需在 App 內由使用者選擇下載；Gemini 需自行提供 API key。

首次安裝家庭版與舊測試版是不同套件，請保留舊版，資料不會自動搬移。
在 Android 設定啟用並選取麥豬；App 的「使用說明與授權 → 版本與更新」可檢查更新。
每日約檢查一次新版，有新版時通知；下載、安裝由使用者確認，需允許更新通知與安裝未知應用程式。
Google 有限發布方案的裝置授權另由開發者邀請管理，本倉庫不代表免除 Android 的安裝限制。

每個版本附 update.json（版本、長度與 SHA-256）及 NOTICES.md／LICENSE.txt。
這是個人及家庭測試版，現有部分從 SogaType 資產分析取得的字庫重發授權尚未核清，詳見隨版本的 NOTICES，不能視為已完成商業授權審查。
原始碼保留於開發者的 TWIME 倉庫；若需本版修改及建置來源，可透過本倉庫 Issues 聯絡。

首個版本正在建置及驗證，完成後提供 Release 下載。