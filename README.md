# Laravel 10 程式碼度量

引入 wnx 的 laravel-stats 套件來擴增解析原始碼，取得一些基本數據，如原始碼行數（loc），會把註解去除後，計算所有程式碼的行數。目的是了解程式碼的現況，並不是設定一個標準數字讓大家完全遵守。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產⽣ Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __stats__ 來執行獲得量測結果。
```sh
$ php artisan stats
```
- 執行 __Artisan__ 指令的 __stats__ 加上 verbose 來執行取得元件量測結果。
```sh
$ php artisan stats --verbose
```

----

## 畫面截圖
![](https://i.imgur.com/eOJwB5v.png)
> 程式碼行數越多，閱讀理論上會花比較多時間，但不是絕對

![](https://i.imgur.com/bElhiFu.png)
> 編寫的程式碼元件獲得客觀和量化的量測結果
