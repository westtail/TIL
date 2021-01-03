## nginx とは
* HTTPおよび、HTTPSでのアクセスに使われる軽量サーバー
* 俗に言うwebサーバー

## 特徴

### イベント駆動
* コールバック関数を利用
    * その関数、イベントが呼ばれた時だけに動く

### ノンブロッキングI/O
* 何かの処理前に、処理待ちが発生する場合、すぐに関数から何か返ってくるという処理
* I/OとはInput/Output
* 処理がすぐできない場合、エラーが返ってきてブロック状態にさせないという処理
* https://techacademy.jp/magazine/16410
### マスタプロセスとワーカプロセスのマルチプロセス構成で稼働する。
* マスタプロセス
    * 全体のプロセスを制御
    * ワーカプロセスに指示を出します。管理や制御
* ワーカプロセス
    * ウェブアプリケーションが実行されるプロセス
    * 実際のクライアントからの接続要求等の一連の処理
* netassist.ne.jp/blog/?p=2712
* https://qiita.com/gigegige/items/3506e24b23f84ef5521d

## confファイルの設定
```
location /some/path/ {
    proxy_pass http://www.example.com/link/;
}
```
* /some/path/page.html URIというリクエストは、http://www.example.com/link/page.htmlにプロキシされる

* nginxの基本
    * https://qiita.com/riita10069/items/5d36dfeb756e3b6c4978
    * http://mogile.web.fc2.com/nginx/admin-guide/reverse-proxy.html