## dockerを用いたCentOS7のpython3の開発環境の作成
``` dockerfile
# centOS7を持ってくる
FROM centos:centos7

# 各パッケージをインストール
RUN yum -y update
RUN yum -y groupinstall "Development Tools"
RUN yum -y install \ 
           kernel-devel \
           kernel-headers \
           gcc-c++ \
           patch \
           libyaml-devel \
           libffi-devel \
           autoconf \
           automake \
           make \
           libtool \
           bison \
           tk-devel \
           zip \
           wget \
           tar \
           gcc \
           zlib \
           zlib-devel \
           bzip2 \
           bzip2-devel \
           readline \
           readline-devel \
           sqlite \
           sqlite-devel \
           openssl \
           openssl-devel \
           git \
           gdbm-devel \
           python-devel 
 
# Python3.6.0をダウンロード
WORKDIR /root
RUN wget https://www.python.org/ftp/python/3.6.0/Python-3.6.0.tgz
RUN tar xzvf Python-3.6.0.tgz

# makeでインストール
WORKDIR ./Python-3.6.0
RUN ./configure --with-threads
RUN make install

# pipインストール(最新版)
RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python get-pip.py

RUN pip3 install --upgrade pip
RUN pip3 install --upgrade setuptools

COPY . /root/test
WORKDIR /root/test

RUN pip3 install -r requirements.txt
CMD ["/bin/bash"]
```

## 参考URL
* CentOS+pythonのdockerfile
  * https://qiita.com/RyosukeKamei/items/eca9687162b7fe122094#3-1-pipをインストール
* pipのテキストベースでのインストール
  * https://techacademy.jp/magazine/47408
  * https://pleiades.io/help/pycharm/managing-dependencies.html#create-requirements
* エラー対策
  * https://qastack.jp/ubuntu/237576/no-acceptable-c-compiler-found-in-path
  * https://stackoverflow.com/questions/51479458/getting-error-could-not-import-pil-image-the-use-of-array-to-img-requires-pi
*  OS確認 
  * https://webkaru.net/linux/centos-version/
* インストールエラ-
  * https://zenn.dev/gz/articles/ad65e162d13cfc1baae8
  * https://stackoverflow.com/questions/65308694/error-importing-librosa-for-tensorflow-sndfile-library-not-found
  * https://anton0825.hatenablog.com/entry/2017/01/09/000000
  * https://qiita.com/nikola-f/items/798547356dcc47239702
  * https://ja.stackoverflow.com/questions/67674/ffmpeg%E3%82%92%E6%89%8B%E5%8B%95%E3%81%A7ubuntu18-04%E3%81%AB%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%97%E3%81%9F%E3%81%84
