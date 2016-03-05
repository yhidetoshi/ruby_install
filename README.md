・rubyをソースコードからインストール
```
# yum -y install zlib-devel openssl-devel sqlite sqlite-devel gcc*

1.9.3系
# wget http://cache.ruby-lang.org/pub/ruby/1.9/ruby-1.9.3-p551.tar.gz

2.0系
# wget http://cache.ruby-lang.org/pub/ruby/2.0/ruby-2.0.0-p598.tar.gz

2.1.5系
# wget http://cache.ruby-lang.org/pub/ruby/2.1/ruby-2.1.5.tar.gz

2.2系
# wget http://cache.ruby-lang.org/pub/ruby/2.2/ruby-2.2.0.tar.gz

#tar xvf <wgetしたファイル>.tar.gz

#cd <解凍したディレクトリ>
# ./configure
# make
# make install
# ruby -v
# gem -v
# ln -s /usr/local/bin/ruby /usr/bin/ruby （rubyのパス調整）
```

▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪▪
rvmを用いたRubyのインストール
公開鍵の入手

```
# sudo gpg2 --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
これを実施しないとrvmのインストールの際に「No public key」というエラーが発生することがある（参考：RVMによるrubyのインストール、vagrantのCentOS環境で。 on @Qiita http://qiita.com/uedatakeshi/items/8138d00a762225f01aa3）

rvmのインストール
# curl -sSL https://get.rvm.io | sudo bash -s stable

profileフォルダ内のスクリプトの実行
# source /etc/profile

利用可能なRubyのバージョンを確認
# rvm list -r

ここでインストール可能なRubyのバージョンを確認して、インストールするバージョンを決める。今回は、
# Remote rubies available:

   jruby-1.7.19
   jruby-src-1.7.19
   ruby-1.9.3-p194
   ruby-1.9.3-p286
   ruby-1.9.3-p327
   ruby-1.9.3-p362
   ruby-1.9.3-p392
   ruby-1.9.3-p429
   ruby-1.9.3-p448
   ruby-1.9.3-p484
   ruby-1.9.3-p547
   ruby-1.9.3-p551
   ruby-2.0.0-p0
   ruby-2.0.0-p195
   ruby-2.0.0-p247
   ruby-2.0.0-p353
   ruby-2.0.0-p481
   ruby-2.0.0-p576
   ruby-2.0.0-p598
   ruby-2.1.0
   ruby-2.1.2
   ruby-2.1.3
   ruby-2.1.5
   ruby-2.2.0
   ruby-2.2.1
と表示されたので、その中で最新版である2.2.1を導入した。
Rubyのインストール

# rvm install ruby-2.2.1
インストール確認兼バージョン確認
# ruby -v
```
