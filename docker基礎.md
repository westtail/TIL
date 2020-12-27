
# dockerとは?
仮想環境の構築ツール  
コンテナと呼ばれる仮想環境を構築してその中でアプリを動かす。  
## dokcerエンジン
dockerそのものでdockerのイメージやコンテナを動かすことができる。  
## dockrコンテナ
dockerエンジン上で動く仮想環境  
ホストOSのカーネルを利用して動いているので、ホストマシンのリソースを節約しながら動いている。  
なのでdockerエンジンは仮想マシンlinuxを上で動いている

## dockerイメージ
dockerコンテナを作るためのレシピ  
ベースイメージにレイヤと呼ばれるイメーシを重ねることで新しいイメージを作成できる。  

## docker レジストリ
dockerイメージを保管している所

## virtualboxとの違い
ホスト型仮想化、ハイパーバイザ型仮想化の両方は、ホストOS上で仮想ソフト、ゲストOS、アプリの順番で重なっている  
ホストOSの上にゲストOSがあるので非常に手間がかかる  



## 参考URL
* https://kitsune.blog/docker-summary


dockerfile

```
FROM ruby:2.4.2

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /

WORKDIR /app-name

ADD Gemfile /app-name/Gemfile
ADD Gemfile.lock /app-name/Gemfile.lock

RUN bundle install

ADD . /app-name
```

## From	
### ベースイメージを指定

## RUN	
### imageの中で実行するshellコマンド、ターミナルなどで実行するコマンドを載せる

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
## ENV
### 環境変数の指定
変数名を指定してdockerfile内で変数で扱う

## ADD
### ファイル/ディレクトリの追加

## COPY	
### ローカルファイルのコンテナへのコピー

## WORKDIR	
### コンテナ起動時の作業ディレクトリの指定

## CMD
### コンテナ起動時に実行するコマンドの定義

## EXPOSE	
### ホストのPORTの割り当て

### 参考サイト
https://qiita.com/tanan/items/e79a5dc1b54ca830ac21