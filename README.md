# LOL12thBalloon - LOL週年活動搶氣球程式
> 使用自動程式皆有風險，請自行評估是否使用

## balloonCMD.exe (推薦使用)
使用token在背景執行，可自動取得token

### 功能
- 爬取Garena新聞下方的最新評論，並輸入序號
- 搶完60顆氣球後自動兌換獎勵（背景執行，**不需**圖資支持）
- 完成後自動停止並播放通知，大約**3分鐘**可以搶完60顆氣球
- 自動於安裝路徑下獲取活動網頁token，無需手動獲取

### 使用說明
1. 開啟LOL主程式並**進入活動頁面**（不能只開主程式）
2. 打開程式，正常情況下會自動獲取token並開始運行
   - 若無法自動獲取token請輸入LOL安裝路徑下`LeagueClient Logs`資料夾之完整路徑，如 `C:\Garena\Games\32775\Game\Logs\LeagueClient Logs`（請自行依安裝路徑調整）
   - 也可自行獲取token後，輸入64位長度的token、或是包含token的活動網址

### 參數設置
需cd到程式所在目錄，以命令列參數方式設置（正常使用可忽略此部分）
- `-d`或`--dir`或`--folder`：LOL主程式LOG檔案路徑，預設為`C:\Garena\Games\32775\Game\Logs\LeagueClient Logs`
- `-t`或`--token`：也可以此方式手動輸入token，預設為空字串。
- `-f`或`--site`或`--from`：邀請碼來源站點，默認為`Garena`，可改為`Bahamut`，但不推薦，約需花兩倍時間
- `-n`或`--num`：單次載入的最新留言數量，預設為5則
- `-s`或`--sucDelay`：輸入成功後延遲多少秒，預設為1.25秒
- `-e`或`--errDelay`：輸入失敗後延遲多少秒，預設為0.5秒
- 範例：$ `balloonCMD.exe -s 0.1 -e 0.1 -n 3`

### ~~獲取token~~ (已改為自動獲取token)

> 1.開啟LOL主程式並進入活動頁面

> 2.開啟 `C:\Garena\Games\32775\Game\Logs\LeagueClient Logs` 資料夾（請自行依安裝路徑調整）

> 3.使用記事本打開最新的 `_LeagueClientUx.log` 文件 [點我看圖](https://i.imgur.com/NUZV33G.png)

> 4.在其中搜尋 `https://bargain.lol.garena.tw/?token=` [點我看圖](https://i.imgur.com/ZQNwUbU.png)

> 5.複製網址貼上到程式中

## balloon.exe
仰賴圖片辨識，會因使用者顯示設定而需個別設定

### 環境
- LOL大廳解析度：**1280*720**
- Windows顯示比例：**125%**
- 需以**管理員**身分執行

### 功能
- 爬取Garena新聞下方的最新評論，並輸入序號
- 搶完60顆氣球後自動兌換獎勵（**需**圖資支持）
- 完成後自動停止並播放通知，大約**10分鐘**可以搶完60顆氣球

### 個人化
- 若使用者無法和開發環境相同，可自行截圖並替換以下檔案
  - confirm.png
  - inBox1.png
  - inBox2.png
  - submit1.png
  - submit2.png