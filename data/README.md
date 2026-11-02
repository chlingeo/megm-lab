# MEGM 網站共用內容資料
H-00-S05、U-00、U-01 讀取 data/publications.json；H-00-S06 和 N-00 讀取 data/news.json。新增資料時不必修改首頁 HTML。

## 論文
於 publications.json 陣列加入物件，必要欄位：year（數字）、title、journal、doi；featured=true 代表列入首頁候選，可加 date (YYYY-MM-DD) 排序、published=false 隱藏。
首頁只顯示符合 featured=true 的最新四篇；學術成果頁顯示所有已發布論文。

## 消息
於 news.json 陣列加入物件，欄位 date（YYYY-MM-DD）、title、summary、url（連向詳細內容或對應頁面），published=false 可隱藏。
首頁顯示最新三則，N-00 顯示完整清單；目前尚未有確認的消息，因此 news.json 初始是 []。

注意：檔案必須是合法 JSON；提交 GitHub 並完成 Pages 部署後生效。未來 CMS 可管理這些資料。
