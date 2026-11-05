# 麥豬輸入法

Android ARM64 輸入法的正式安裝與更新專用儲存庫。目前主要測試裝置為 Samsung Galaxy S25。

- [最新版本與安裝包](https://github.com/micropigkuo/maizhu-releases/releases/latest)
- 注音字庫來自小麥注音，英文補字使用 CMUdict，Emoji 關鍵字使用 Unicode CLDR，輸入引擎使用 Rime。
- 個人學習資料、API key、憑證與錄音不放入公開儲存庫。

## 0.2.49：三種語音輸入

| 選項 | 使用方式 |
| --- | --- |
| 本機 | Qwen3-ASR 0.6B，直接輸出辨識文字，離線使用。 |
| 潤飾 | Gemma 4 E2B，直接理解錄音並整理文字，離線使用。 |
| 雲端 | 固定使用 Gemini 3.5 Transcribe，需要網路及使用者自行設定的 API key。 |

移除翻譯、舊 Gemini 語音及模型版本選擇，保留 API key 輸入和已儲存的憑證。Gemma 要求輸出台灣繁體中文與英文；若出現阿拉伯文等其他文字系統，顯示錯誤而不提交。

APK 已完成編譯與基本檢查，實際語音品質仍需手機測試。本機模型不打包進 APK，請到 App 語音設定管理模型。Gemma 每次錄音最長 30 秒，點擊開始，再次點擊結束。

## 安裝與更新

首次安裝：到最新版本下載 `Maizhu-0.2.49-arm64.apk`，依 Android 提示安裝，再到系統設定啟用並切換麥豬輸入法。此版適用 Android 7.0 以上 ARM64 手機。

已有正式版：進入 App「使用說明與授權 → 版本與更新」，按「檢查更新」，選「下載並安裝」，再依系統畫面確認。原地更新保留既有設定、個人字庫、API key 及模型，請保留原 App，不要解除安裝或清除資料。

語音設定或鍵盤的語音來源選單只提供「本機、潤飾、雲端」。長按語音來源按鈕可切換。雲端的 API key 欄位保留在「雲端 · Gemini 3.5 Transcribe」。

背景約每日檢查一次更新，時間受系統排程影響。下載與安裝由使用者確認；通知及安裝未知應用程式的權限由使用者允許。

從舊測試套件首次搬遷者，請參考 [0.2.38 移轉說明](https://github.com/micropigkuo/maizhu-releases/releases/tag/v0.2.38)。更新頁保留「恢復穩定版」入口；是否提供相容恢復包以發佈內容為準，詳見 [恢復說明](https://github.com/micropigkuo/maizhu-releases/releases/download/v0.2.40/Stable-recovery-guide.md)。

## 來源與授權

每版附 `update.json`（版本、大小與 SHA-256）、`NOTICES.md`、`LICENSE.txt`。字庫固定來源與生成工具見 [字庫來源包](https://github.com/micropigkuo/maizhu-releases/releases/download/v0.2.39/Maizhu-open-lexicon-sources-0.2.39.zip)，完整字庫授權亦可在 App「字庫來源與授權」閱讀。

主 App 原始碼保留在開發者的 TWIME 儲存庫；需要對應修改或建置來源，可於本儲存庫 Issues 聯絡。此儲存庫提供正式版安裝與更新，不含模型權重。
