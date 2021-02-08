
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

### gitの勉強

1. https://qiita.com/kyoyyy/items/161b6905f45bee2efe21 の「難易度：★☆☆」を読む
1. チーム開発では git flow や github flow みたいな感じで使う。ブランチ操作が必要。https://qiita.com/mint__/items/bfc58589b5b1e0a1856a を読む
1. 次のコマンドを使えるようにする。
```
      git init
      git add
      git status
      git commit
      git branch (ブランチ作成, ブランチ名前変更)
      git checkout (ブランチ切り替え)
```
1. tig をインストールする (mac なら brew install tig)
2. 次の流れで操作してみる。
      1. ``` git init ``` で初期化
      2. README.md を作る
      3. ``` git add README.md ``` をする
         -> ``` git status``` をすると README.md がコミット待ちの状態になっている
　    4. ```git commit``` して初期コミットを作る
      5. ```git branch feature/modify_readme``` で master ブランチを元に feature/modify_readme ブランチを作る
      6. ```git checkout feature/modify_readme``` でブランチを切り替える
         -> ```git status``` をするとブランチが feature/modify_readme に切り替わっている
         -> ```tig``` をすると master と  feature/modify_readme が同じものになっている
      7. README.md を更新する
         -> ```git status``` をすると README.md が変更点として出ている
         -> ```tig status``` をすると README.md が変更点として出ている、また差分も見える
      8. ```tig status``` から README.md  をコミット対象にする
      9. ```git commit``` でコミットする
         -> ```tig``` すると master と  feature/modify_readme が違うものになっている
     10. ```git checkout master``` で master ブランチに切り替える
　 11. ```git merge feature/modify_readme --no-ff``` で feature/modify_readme の変更を master にマージする
         -> README.md を見ると更新されている


* https://qiita.com/kyoyyy/items/161b6905f45bee2efe21   gitの簡単な説明
* https://techacademy.jp/magazine/10172   git log 
* https://git-scm.com/book/ja/v1/Git-の基本-コミット履歴の閲覧
* https://qiita.com/sunstripe2011/items/30f46a7bf451c1a85c2b    git branch
* http://www-creators.com/archives/1282   git resetq


* tigについて
* https://qiita.com/YusukeHosonuma/items/d81397ab70a8c26a2902
