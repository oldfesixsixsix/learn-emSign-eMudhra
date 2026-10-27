# 暗井 UNDERSHAFT

eMudhra 憑證事件（2025 年金鑰儀式出包、八張中繼憑證被瀏覽器撤銷）互動解謎，Three.js 做的 3D 小遊戲，掛在 `unclereal.com/library/undershaft`。

## 檔案

```
web/
  index.html    整個遊戲（單一頁面，樓層資料在頁面內的 JS 裡，不是分開的檔案）
worker.js       路徑前綴剝除 + 借閱記錄（見 library docs/adr/0001、0003）
wrangler.jsonc  Worker + assets 設定
```

## 開發

```
npm install
npm run dev
```

## 部署

```
npm run deploy
```

部署到 `unclereal.com/library/undershaft*`，細節見 `library` 的 `docs/adr/0001-worker-assets-path-prefix.md`、`docs/adr/0003-borrowing-system.md`。

部署後要到 `library` 的 `/library/admin` 後台登記書目（title/subtitle/category/tags/path=`/library/undershaft`/capacity），才會出現在 `library` 首頁的書目列表——這一步是 owner 手動操作，不含在這個 repo 的部署流程裡（見 oldfesixsixsix/library#14）。
