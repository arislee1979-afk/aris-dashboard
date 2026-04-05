# 網頁發布規則

## 路徑規則（必遵守）
- 導航連結一律用**相對路徑**（`./`、`sleep.html`、`body.html`）
- 絕對不要用 `/gym/` 等根目錄路徑
- GitHub Pages 部署路徑是 `/aris-dashboard/gym-dashboard/`，用絕對路徑會 404

## 發布前檢查（必執行）
1. 改完後在 VM 跑測試 server：
   ```bash
   cd ~/.openclaw/workspace/webpage/aris-dashboard/gym-dashboard
   python3 -m http.server 9999 --bind 0.0.0.0
   ```
2. 用瀏覽器開 `http://100.79.89.116:9999/` 確認：
   - 統計卡片有數字（不是 `--`）
   - 圖表有渲染
   - 導航連結點得通（不 404）
3. 確認沒問題後再 push：
   ```bash
   cd ~/.openclaw/workspace/webpage/aris-dashboard
   git add . && git commit -m 'update' && git push
   ```

## JS 規則
- Chart.js 用 CDN：`https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js`
- IIFE 內的變數要加 namespace prefix（如 `_bd_`、`_sl_`），避免跟 index.html 合併頁衝突
- 資料內嵌在 HTML 裡（const DATA = [...]），不用外部 API

## 檔案結構
```
gym-dashboard/
├── index.html      ← 合併頁（Training + Sleep + Body tabs）
├── training.html   ← 獨立頁
├── sleep.html      ← 獨立頁
└── body.html       ← 獨立頁
```
