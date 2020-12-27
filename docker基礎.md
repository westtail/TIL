
# dockerとは?
仮想環境の構築ツール  
コンテナと呼ばれる仮想環境を構築してその中でアプリを動かす。  
## dokcerエンジン
dockerそのものでdockerのイメージやコンテナを動かすことができる。  
dockerデーモンとして動作する
## dockrコンテナ
dockerエンジン上で動く仮想環境  
ホストOSのカーネルを利用して動いているので、ホストマシンのリソースを節約しながら動いている。  
なのでdockerエンジンは仮想マシンlinuxを上で動いている

## dockerイメージ
dockerコンテナを作るためのレシピ、設計図  
ベースイメージにレイヤと呼ばれるイメーシを重ねることで新しいイメージを作成できる。  

## docker レジストリ
dockerイメージを保管している所

## docker compose 
複数のコンテナを一括で管理するシステム

## リンク機能
コンテナなどはdocker上で動いているためコンテナ間の通信は可能
## virtualboxとの違い
ホスト型仮想化、ハイパーバイザ型仮想化の両方は、ホストOS上で仮想ソフト、ゲストOS、アプリの順番で重なっている  
ホストOSの上にゲストOSがあるので非常に手間がかかる  

* dockerにより環境構築を手軽に行うことができる
    * 環境構築をファイルに記述できる
    * 環境構築を破棄しても、同じものが作れる
    * 軽くて早く以上のことを行うことができる

## dockerfileの説明

### buildコマンド
dockerfileからdockerのイメージを作成する

### レイヤー 
build時にイメージを１から作るのではなく、すでにあるイメージはそのままで、差分を積み重ねて管理している  

### FROM
ベースイメージを指定 このベースイメージにレイヤーを重ねる

```
FROM centos
```

### ENV
コンテナ内の環境変数を設定する

```
ENV hoge=hogehoge
```

## RUN
コンテナの中で実行するコマンドを載せる  
Dockerイメージからコンテナを作成するためのコマンド  
コンテナを作成するために必要なインストールなどのコマンド

```
RUN yum -y install httpd
```

### ADD
ファイル/ディレクトリの追加  
ファイルやディレクトリを取得する命令。

### COPY
ローカルファイルのコンテナへのコピー  
ホストOS上のローカルファイルのみ可

### WORKDIR	
場所(ディレクトリ)を移動する命令  
コンテナ起動時の作業ディレクトリの指定


### EXPOSE	
ホストのPORTの割り当て  
コンテナにアクセスする公開ポート番号を設定する


### CMD
コンテナ起動時に実行するコマンドの定義  
Dockerイメージが起動してから実行されるコマンド  
イメージが出来上がってからのインストール以外のコマンドなど

## 参考URL
* https://kitsune.blog/docker-summary
* https://qiita.com/gold-kou/items/44860fbda1a34a001fc1
* https://qiita.com/tanan/items/e79a5dc1b54ca830ac21

dockerfile

```
FROM ruby:2.4.2 # rubyのイメージをベースイメージとして持ってくる

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
# イメージ作成のためのイメージインストールなどを実行

RUN mkdir /

WORKDIR /app-name

ADD Gemfile /app-name/Gemfile
ADD Gemfile.lock /app-name/Gemfile.lock

RUN bundle install

ADD . /app-name
```

### apt-get
パッケージの操作・管理を行うコマンド https://webkaru.net/linux/apt-get-command

* install　パッケージ 指定したパッケージをインストールします
* update　ライブラリのインデックスを更新
* -q　quietモードです。進捗状況を表示しません
* -y　インタラクティブ（ユーザーへの問い合わせ）に「yes」と答えます

### build-essential
名前の通り, 開発に必須のビルドツールを提供しているパッケージ.

### libpq-dev 
PostgreSQLの略語でPostgreSQLインストールパッケージ

### node.js
node.jsはjavascript用のランタイム サーバーサイドのJavaScript実行環境です。