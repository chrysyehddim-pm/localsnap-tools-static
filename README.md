# LocalSnap Tools Static

LocalSnap Tools 是一個純靜態、瀏覽器本機處理的檔案小工具箱。

## 為什麼改成 Static 版？

這版沒有 Next.js、沒有 npm install、沒有 build step，所以比較適合只用 GitHub 網頁版 / github.dev 維護的人。

你可以直接把 `index.html` 放到 GitHub Pages、Vercel 或任何靜態網站空間。

## 功能

- PDF 安全優化 / 基礎壓縮
- 多 PDF 合併
- JPG / PNG / WebP 壓縮
- JPG / PNG / WebP 轉檔
- 圖片尺寸調整
- 純色背景去背，輸出透明 PNG
- PPTX 內嵌圖片壓縮

## 隱私原則

- 沒有後端 API
- 沒有資料庫
- 沒有登入
- 沒有檔案上傳
- 檔案只在瀏覽器本機記憶體中處理

注意：此靜態版會從 CDN 載入 JSZip 與 PDF-Lib 程式庫。CDN 只提供程式碼下載，不會收到你選擇的檔案內容。

## GitHub Pages 部署

1. 建立一個新的 GitHub repo，例如 `localsnap-tools-static`
2. 上傳本資料夾內的所有檔案到 repo 根目錄
3. 進入 repo 的 Settings → Pages
4. Source 選 `Deploy from a branch`
5. Branch 選 `main`，資料夾選 `/root`
6. 儲存後等待 GitHub Pages 產生網址

## Vercel 部署

1. 建立一個新的 GitHub repo
2. 上傳本資料夾內的所有檔案到 repo 根目錄
3. 到 Vercel 新增專案並匯入該 repo
4. Framework Preset 選 `Other`
5. Build Command 留空
6. Output Directory 留空或填 `.`
7. Deploy

## 正確檔案結構

repo 根目錄應該長這樣：

```text
index.html
README.md
UPLOAD_CHECKLIST.txt
```

不需要 `package.json`、`package-lock.json`、`node_modules`。
