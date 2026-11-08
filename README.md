# 月糰所 Tsuki Dango

三色糰的虛擬甜點品牌網站，以天竺鼠甜點師為主角。提供商品瀏覽、購物袋、三串糰子 NT$199 優惠、模擬結帳與訂單卡。

> 本網站為作品與虛擬購物體驗，不收費、不出貨，不需要真實姓名、地址或付款資料。

## 檔案

- `index.html`：網站內容與結帳視窗
- `style.css`：響應式版面與品牌配色
- `app.js`：商品、購物袋、模擬結帳與事件
- `config.js`：GA4 衡量 ID 設定
- `assets/`：品牌與商品素材（含透明背景店長與三色色票）

## 本機查看

在此資料夾執行 `python3 -m http.server 8000`，再開啟 http://localhost:8000 。無須安裝 npm 套件或執行建置。

## GA4

在 `config.js` 的 `ga4MeasurementId` 填入自己的 `G-` 開頭衡量 ID，部署後驗證事件。ID 留白時不載入 GA4。

預留事件：`view_item_list`、`view_item`、`add_to_cart`、`remove_from_cart`、`view_cart`、`begin_checkout`、`simulation_complete`。模擬完成使用 `simulated_value`，不使用真實購買事件 `purchase`。

## 上線

此儲存庫已含可直接提供服務的靜態網站檔案，首頁位於根目錄。上傳到 GitHub 不等於已啟用 GitHub Pages；若使用 Pages，需另外設定託管，能否從私人儲存庫啟用依帳號方案而定。

## 配色

- 月餅橘 `#F0831E`
- 月光米 `#FEEBBE`
- 焦糖棕 `#BC6E2E`

購物袋儲存於使用者瀏覽器的 localStorage，模擬訂單不會寫入伺服器。
