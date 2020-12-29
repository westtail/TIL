## webの基礎的な用語

### web,www(world wide web)
* 文章などをインターネット上で公開、閲覧するためのシステム
  * インターネット上の様々な情報（テキスト・画像・動画など）を関連付け、結びつけるシステム
  * ハイパーテキストと呼ばれるテキストを用いて自分の文章や画像、動画を公開できる

### webサイト
* 一つのドメインにある複数のwebページの集まり

### webページ 
* インターネットの世界で見られる文書ファイルのこと
  * webページはハイパーテキストを用いて構成されている

### ハイパーテキスト（HyperText）
* ハイパーリンクを埋め込むことができる高機能なテキストです

### ハイパーリンク
* 別のwebページへ移動するリンクのこと

### HTML (HyperText Markup Language)とは
* ハイパーテキストを記述するための言語

### webブラウザ
* ハイパーテキストを解釈して人間が読みやすい形にするためのプログラム

### webサーバー
* ホームページやWebサービスを置くサーバーでクライアントからのリクエストに対して結果を返す
 * webブラウザからのコンテンツの要求に対して必要なコンテンツをネットワークを通してwebブラウザに送信する

#### webサーバーの種類
* Apache・・・オープンソースでありながら高い信頼性と充実した機能を備えた世界中で最も多く使われているWEBサーバであります。Linuxで多く使われています。
* Nginx（エンジンエックス）・・・Apacheと同じくオープンソースであり、同時リクエストの処理に特価していて、軽量で処理が早いWEBサーバであります
* IIS（Microsoft Internet Information Services）・・・Microsoft Windowsの標準WEBサーバであります

### HTTP (Hyper Text Transfer Protocol)
* クライアントとwebサーバーとのHTMLでの通信のやり取りの手順のこと

### URL Uniform Resource Locator（ユニフォームリソースロケータ）
* インターネット上にあるホームページやファイルの位置や情報を示すもの
  * URLは「IPアドレス」を人間が読みやすいように変換したもの
  * 「どのやり取りの手順」「どのwebサーバー」「何のコンテンツ」を取りに行くかの情報が載っている
  * http://www.test.jp/index.html を例えで解析すると  
    * 1 http://  HTTPの方法で
    * 2 www.test.jp  どのwebサーバーにアクセスするか 
    * 3 index.html  どのコンテンツか
### 静的ページ
* いつ誰が見ても同じ内容が表示される、表示される内容が変わらないホームページ（の中の1ページ）のこと

### 動的ページ
* あれやこれやの要因によって表示される内容が変わるかもしれないホームページ（の中の1ページ）のこと
* ページに対して動きが入ることでコンテンツの内容が変化する

### CGI (Common Gateway Interface)
* webサーバーとプログラムがやり取りするためのインターフェース
* リクエストが来てwebサーバーがプログラムを実行して作成されたHTMLを返す方法
* リクエストごとにプログラムを動かすので重たい→昔の主流

### webアプリケーションサーバー
* Webサーバから動的処理を依頼されるサーバ
* webサーバーから処理を依頼されて処理をする
* CGIとの違いは常に動いているか、リクエストのたびに動いているかの違い？

### RESTful (REpresentational State Transfer)
* ４つの原則からなるシンプルな設計
  * アドレス可能性(Addressability)
    * 提供する情報がURIを通して表現できること
    * URLだけで何を行うかがわかるようにすること
  * ステートレス性
    * すべてのHTTPリクエストが完全に分離している性質であること。セッションなどの状態管理は行われないこと
  * 接続製
     * 情報の内部に、別の情報や(その情報の別の)状態へのリンクを含めることができること
  * 統一インターフェース
    * 情報の操作(取得、作成、更新、削除)は全てHTTPメソッド(GET、POST、PUT、DELETE)を利用すること

### socket
* プログラムとネットワークをつなげる接続口のこと
* プログラムでネットワーク通信部分を担当する奴等
  * 通信をソケットが担当しており、ソケット同士が通信をやり取りし合う

### ユーザーインターフェース (UI)
* コンピューターの機能とユーザーのやり取りの橋渡しを行う

### API(アプリケーションプログラムインターフェース)
* ソフトウェア同士のやり取りの橋渡しをする
* ソフトウェアにAPIという外部とやりとりする窓口を作り、外部アプリとコミュニケーションや連携ができる状態

## HTMLについて
* headタグ
  * 通信に必要な内容
* bodyタグ
  * 文章などのデータの中身


### webアプリ
* webブラウザをインターフェースとして入出力するアプリケーション

#### 参考URL
* HTMLについて
  * http://www.htmq.com/htmlkihon/001.shtml
* webサイトについて
  * https://www.axis-corp.com/quest/website-homepage-difference/
* ユーザーインターフェース
  * https://hataraku.vivivit.com/works/ui
* API
  * https://data.wingarc.com/what-is-api-16084
* webページとは
  * https://wa3.i-3-i.info/word1545.html
* webサーバー
  * https://wa3.i-3-i.info/word1128.html
  * https://www.no1web.jp/blog/15004/
* HTTP
  * https://cybersecurity-jp.com/security-measures/25772
* URL
  * https://ferret-plus.com/8736
* 静的ページ
  * https://wa3.i-3-i.info/word11862.html
* 動的ページ
  * https://wa3.i-3-i.info/word11861.html
* ソケット
  * https://wa3.i-3-i.info/word168.html 
* CGI
  * http://www.tohoho-web.com/wwwcgi1.htm
* webサーバー　アプリケーションサーバーについて
  * https://qiita.com/tamago3keran/items/f470593926458b7ef52a
* RESTful
  * https://qiita.com/NagaokaKenichi/items/0647c30ef596cedf4bf2
  * https://blog.api.rakuten.net/ja/jp-restful-api/#:~:text=REpresentational%20State%20Transfer%E3%81%AE%E7%95%A5,%E3%81%AE%E3%81%93%E3%81%A8%E3%82%92%E6%8C%87%E3%81%97%E3%81%BE%E3%81%99%E3%80%82
* 
