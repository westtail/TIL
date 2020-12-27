
### ステージングをコミットする
```
$ git commit 
#シンプルにコミットする場合

$ git commit -m "コメント"
# コメントをつけてコミットする場合
```
### 変更状況を確認
```
$ git status
```
### ブランチを確認
```
$ git branch
```
### ブランチ変更
```
$ git checkout ブランチ名
# ブランチを変更

$ git checkout -b ブランチ名
# 新しいブランチに変更
```
### 他の変更をプルする
```
$ git pull 
```
githubのデータをローカルに反映する
```
$ git fetch
```
```
$ git rebase master 
```

### ブランチ削除
```
$ git branch -d [ブランチ名]
```

### 
http://www-creators.com/archives/1116
### 他の人がブランチをもらう
```
git pull
でブランチの環境も落ちてくる
```

## gitメッセージの書き方
https://qiita.com/itosho/items/9565c6ad2ffc24c09364

以下の形式をメッセージに追加するとやりやすい
* fix：バグ修正
* add：新規（ファイル）機能追加
* update：機能修正（バグではない）
* remove：削除（ファイルs