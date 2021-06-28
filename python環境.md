## big sur python環境準備
### pyenv のインストール
#### エラー内容
```
$pyenv install バージョン

エラー

python-build: use openssl@1.1 from homebrew
python-build: use readline from homebrew
Downloading Python-3.7.2.tar.xz...
-> https://www.python.org/ftp/python/3.7.2/Python-3.7.2.tar.xz
Installing Python-3.7.2...
python-build: use readline from homebrew
python-build: use zlib from xcode sdk

BUILD FAILED (OS X 11.4 using python-build 20180424)

Inspect or clean up the working tree at /tmp/python-build.20210628152408.14318
Results logged to /tmp/python-build.20210628152408.14318.log
```
#### 対策
対応するインストール方法
```
CFLAGS="-I$(brew --prefix openssl)/include -I$(brew --prefix bzip2)/include -I$(brew --prefix readline)/include -I$(xcrun --show-sdk-path)/usr/include" LDFLAGS="-L$(brew --prefix openssl)/lib -L$(brew --prefix readline)/lib -L$(brew --prefix zlib)/lib -L$(brew --prefix bzip2)/lib" pyenv install --patch バージョン < <(curl -sSL https://github.com/python/cpython/commit/8ea6353.patch\?full_index\=1)
```
* https://qiita.com/Butterthon/items/e7d1f379c828b41f3e19
