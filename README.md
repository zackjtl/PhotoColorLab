# PhotoColorLab（調色實驗器）

單一 HTML 檔的照片調色工具，直接在瀏覽器裡運作，不需要安裝，也不會上傳你的照片。
A single-file, in-browser photo color-grading tool. No install, and your photos never leave your machine.

## 功能 Features

- 左側檢視區：調色前後對照（分割線）、取色模式與編號標記點、拖放載入照片，也支援 RAW 檔
- 右側面板：滑桿分組、色彩輪、色調曲線，並有復原／重做
- 三種示波器：含截斷（過曝／死黑）警示，其中一個是向量示波器
- 預設：內建預設加上自訂預設，可匯出／匯入 JSON 預設檔
- 自動跟隨系統的淺色／深色模式
- 沒有載入照片時，會顯示內建的範例色卡

## 使用方式 Usage

1. 直接用瀏覽器開啟 `index.html`，或部署到 GitHub Pages。
2. 按「開啟圖片」，或把照片拖進視窗。
3. 調整後按「匯出」存成 JPG；預設可存在瀏覽器裡，或匯出成 JSON。

### 部署到 GitHub Pages

Settings → Pages → Source 選 `Deploy from a branch`，Branch 選 `main`、資料夾選 `/ (root)`，儲存後等一兩分鐘即可。

## 技術說明 Notes

- 全部在前端執行，沒有後端、沒有建置步驟。
- 字型使用 Google Fonts（Noto Serif TC、Noto Sans TC、IBM Plex Mono），需要連網才會載入。
- RAW 解碼使用 [libraw-mini](https://www.npmjs.com/package/libraw-mini)，由 jsDelivr CDN 載入，第一次開 RAW 檔時需要連網。
- 自訂預設存在瀏覽器的 localStorage（同一個瀏覽器、同一個網址才看得到）；要換電腦請用「匯出」。
- 這個專案最初是在 claude.ai 的 artifact 裡開發。檔案內仍保留偵測 claude.ai 執行環境的程式碼，在一般瀏覽器裡不會啟用，不影響使用。

## 授權 License

尚未指定。公開前請自行選擇授權條款（例如 MIT）。
