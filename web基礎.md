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

### HTML (HyperText Markup Language)
* ハイパーテキストを記述するための言語

### CSS（Cascading Style Sheets、カスケーディング・スタイル・シート）
* ウェブページのスタイルを指定するための言語
  * HTMLの文章などを見やすいスタイルに変更する

### javascript
* ウェブページにて複雑な機能をできるようにするプログラミング言語

### webブラウザ
* ハイパーテキストを解釈して人間が読みやすい形にするためのプログラム

### webサーバー
* ホームページやWebサービスを置くサーバーでクライアントからのリクエストに対して結果を返す
 * webブラウザからのコンテンツの要求に対して必要なコンテンツをネットワークを通してwebブラウザに送信する

#### webサーバーの種類
* Apache・・・オープンソースでありながら高い信頼性と充実した機能を備えた世界中で最も多く使われているWEBサーバであります。Linuxで多く使われています。
* Nginx（エンジンエックス）・・・Apacheと同じくオープンソースであり、同時リクエストの処理に特価していて、軽量で処理が早いWEBサーバ
* IIS（Microsoft Internet Information Services）・・・Microsoft Windowsの標準WEBサーバ

### HTTP (Hyper Text Transfer Protocol)
* クライアントとwebサーバーとのHTMLでの通信のやり取りの手順のこと
* HTTPリクエスト
   * webブラウザからの要求
1. リクエスト行 
   * webサーバーに対するどのような処理をして欲しいかのリクエスト部分
   * メソッド パス名 HTTP/バージョン
2. ヘッダー
   * webブラウザの情報
3. メッセージボディ
   * webサーバーに送るデータなどが入る
* HTTPレスポンス
   * webサーバーからの応答
1. レスポンス行
   * webブラウザにwebサーバーでの処理の結果を伝える
   * HTTP/バージョン ステータス番号 補足メッセージ
2. ヘッダー
   * webサーバーの情報
3. メッセージボディ
   * HTMLや画像などデータを格納する場所

### HTTPメソッド
* クライアントがwebサーバーに要求する処理の種類
* HEAD
   * ヘッダー情報だけを取得する
* GET
   * データの取得がメイン　webサイト閲覧で使用することが多い
* POST
   * webブラウザからwebサーバーにデータを送信
* PUT
   * データの送信、主にデータの更新をメイン
* DELETE
   * データを削除することをメイン
### ステータスコード
* HHTPレスポンスの結果内容
* 100番台はHTTPリクエストを処理している最中
* 200番台はHTTPリクエストが成功した際の通知
* 300番台は転送処理などのwebブラウザ側の追加の処理が必要となる
* 400番台はクライアント側のエラーであることを通知
* 500番台webサーバー側のエラーであることを追知

### メッセージヘッター
* HTTPメッセージに関する詳細な情報を示す
* いくつかのヘッダーフィールドで構成されている
   * フィールド名：　フィールド値
   * 一般ヘッダーフィールド
   * リクエストヘッダーフィールド
   * レスポンスヘッダーフィールド
   * エンティティヘッダーフィールド
### HTTPS (HTTP over SSL/TLS)
* HTTPに暗号化技術を用いることでHTTP通信の安全性を高める
* 盗聴禁止 HTTPでの通信データ内容を見れなくする
* 改竄禁止 HTTPでの送信データを第三者が変更できないようにする
* なりすまし禁止 信用ある相手としか通信を行わないようにする

### SSL（Secure Sockets Layer）/TLS（Transport Layer Security）
* SSL(Secure Socket Layer)は、インターネット上でやりとりされるデータの「盗聴」「改ざん」「なりすまし」を防止するための暗号化プロトコル(通信方法)
* TLSはSSLの最新バージョン

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

### REST API
* URIはリソースを表現しなければならない（リソース名は動詞ではなく、名詞を使用）
* リソースの操作は、HTTPメソッド（GET、POST、PUT、DELETEなど）で表現する
  * POST	対応するURIをリクエストし、リソースを作成する
  * GET	リソースを照会して、当該ドキュメントの詳細情報を取得する
  * PUT	当該リソースを変更する
  * DELETE	リソースを削除する

### クライアントとサーバー
* クライアント
  * 提供されたサービスを利用する側
* サーバー
  * ネットワーク上でサービスを提供する側
### プロトコル
* 何かの動作の手順のこと
* ネットワークに接続された機器同士が通信するときの予めに決めた共通の手順のこと

### TCP/IP TCP「Transmission Control Protocol」とIP「Internet Protocol」
* コンピュータネットワークやインターネットを動かしている通信技術を一式として総称したもの
* ４つの階層(レイヤー)に分かれている  また、OSI参照モデルと呼ばれる7つの層に分かれている
  * アクリケーション層 アプリケーションごとのやり取りを規定 HTTP SMTP FTP
  * トランスポート層 データの分割や品質保証を規定 TCP UDP
  * インターフェース層　ネットワーク間の通信を規定 IP ICMP
  * ネットワークインターフェース層 ハードウェアに関する規定 イーサネット、Wi-fi

### TCPのデータ通信
* コネクションと呼ばれるクライアントとサーバーの通信経路を確立したあとのやりとり
  * SYN クライアントからのサーバーへの接続要求
  * SYN+ACK クライアントに対して確認応答とサーバーからの接続要求
  * ACK サーバーに対する確認応答

### IPアドレス
* インターネット上の住所のような物
* インターネット上に接続された機器が持つナンバーのことで特定のコンピューターにアクセスできる

### ポート番号
* コンピューター内のプログラムを識別するための番号
* コンピューターの通信に使用するプログラムを識別するための番号
  * TCP 22 : SSH
  * TCP 80 : HTTP
  * TCP 443 : HTTPS

### ドメイン
* IPアドレスを人がわかりやすい形にした物

### DNS (Domain Name System)
* ドメインをIPアドレスに変換する仕組み
* DNSサーバーはドメインとIPアドレスを関連付ている
* ドメイン名からDNSサーバーに検索することでIPアドレスを手に入れてアクセスする


### socket
* プログラムとネットワークをつなげる接続口のこと
* プログラムでネットワーク通信部分を担当する奴等
  * 通信をソケットが担当しており、ソケット同士が通信をやり取りし合う

### ユーザーインターフェース (UI)
* コンピューターの機能とユーザーのやり取りの橋渡しを行う

### API(アプリケーションプログラムインターフェース)
* ソフトウェア同士のやり取りの橋渡しをする
* ソフトウェアにAPIという外部とやりとりする窓口を作り、外部アプリとコミュニケーションや連携ができる状態

### web API
* webアプリケーションの処理をネットワークで呼び出す

### webアプリ
* webブラウザをインターフェースとして入出力するアプリケーション

### 永続化、データベース
* アプリを動かす際にデータを保存する場所

### ログイン
* ユーザーがそのwebアプリを使うために行う処理

### Cooki

## HTMLについて
* headタグ
  * 通信に必要な内容
* bodyタグ
  * 文章などのデータの中身

### デーモン
* 待機している常駐プログラムのUNIX系OSにおける呼び名

#### 参考URL
* HTMLについて
  * http://www.htmq.com/htmlkihon/001.shtml
* CSS
  * http://www.htmq.com/csskihon/001.shtml
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
  * http://www.tohoho-web.com/ex/http.htm
* HTTPメソッド
  * https://tsuyopon.xyz/2019/01/31/understand-4-http-methods/
* SSL/TLS
  * https://www.idcf.jp/rentalserver/aossl/basic/ssl-tls/
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
  * https://meetup-jp.toast.com/931
* TCP/IP
  * https://eng-entrance.com/network-tcpip
* IPアドレス
  * https://www.kagoya.jp/howto/network/ipaddress/
* ポート番号
  * https://eng-entrance.com/network-port
* DNS
  * https://www.nic.ad.jp/ja/newsletter/No22/080.html
* デーモン
  * https://wa3.i-3-i.info/word11000.html
