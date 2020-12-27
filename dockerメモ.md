 * dockerはアプリケーションのモジュールやミドリウェアやライブラリ、OS/ネットワークのインフラ環境設定を全て一つの「コンテナ」にして管理しやすくする
* dockerには「イメージ」がありコンテナの元になる

docker

### コンテナの削除
```
docker rm コンテナ名またはコンテナID
```

### イメーシの削除
```
docker rmi イメージ名またはイメージID
```

### 起動中のコンテナを表示
```
docker ps
```

### 停止中のコンテナを含め、すべてのコンテナを表示
```
docker ps -a
```

```
docker-compose down -v
```


docker-compose

### dockerのイメージからコンテナ作成
```
docker-compose build
```
### コンテナ起動
```
docker-compose up
```
### コンテナ破棄
```
docker-compose down
```
### コンテナ停止
```
docker-compose stop
```
### railsのコマンド実行
```
docker-compose run web コマンド名
```
gemfileのインストール 
```
bundle install 
```

プロセス状況確認
```
docker-compose ps 
```

### volumeの確認
```
docker volume ls
```

### volumeの全削除
```
docker volume rm $(docker volume ls -qf dangling=true)
```
https://qiita.com/Ikumi/items/b319a12d7e2c9f7b904d
https://qiita.com/reflet/items/5caa88abcf1e8964783a


# その他
## dbの永続化
https://note.com/wankoromochi0628/n/nae90aa1d036f

https://note.com/wankoromochi0628/n/nae90aa1d036f

やり方
vokumesを作成して
その出力先を物理メモリに保存する
```
serviecs
  db:
	images:
	volumes:
      - pgdatavol:/var/lib/postgresql/data
      ~~~~~
volumes:
  pgdatavol:
```
