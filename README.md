# Beeinfo

## 環境構築

### Linux環境の場合
必要なもの:  
* rbenv  
* ruby-build  

### rbenvのインストール
#### Step1 パッケージのインストール
最初にrbenvをインストールする為、以下のコマンドを実行  

    $ sudo apt-get update  
    $ sudo apt-get upgrade  
    $ sudo apt-get install -y rbenv  


調べたところ、以下のように  

    $ cd  
    $ git clone git://github.com/sstephenson/rbenv.git .rbenv  

とコマンドを打ってインストールする方法もあるらしく、  
もしパッケージからインストールできなかった場合はgitからクローンしてください。  

#### Step2 PATHの設定
インストールしただけではPATHがないので、以下のようにしてPATHを作る準備をする。  

    $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile  
    $ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile  

準備ができたら最後に以下のコマンドを実行してPATHを通してあげる  

    $ source ~/.bash_profile

きちんとインストールされているかどうかを以下のコマンドで確認する  

    $ rbenv --version


### ruby-buildのインストール
rbenvは単にrubyのバージョンを切り替える為のものなので、rubyをインストールしてくれるものが必要。  
それがruby-buildである。  

ruby-buildはrbenvのプラグインとして提供されているので、以下のコマンドを入力することで簡単にインストールすることができる。  

    $ git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build  

### rubyのインストール
上記の手順を完璧にできたら、ようやくrubyのインストールを行う。  

#### Step1 インストール可能なバージョンを確認
以下のコマンドを入力して、インストール可能なバージョンを確認する。  

    $ rbenv install -l

多くの結果が出てくるが慌てる必要は特にない。  
確認すべきは2.x.xと表示されている部分だけでいい。  

#### Step2 rubyのインストール
現時点(2017年7月3日)で最新の安定版2.4.1をインストールする。  

    $ rbenv install 2.4.1


#### Step3 インストールしたrubyの確認と切り替え
以下のコマンドでインストールしたrubyの確認ができる。

    $ rbenv versions

もしここにインストールしたrubyが表示されていなければインストールが失敗しているので、もう一度[Step2](#Step2-rubyのインストール)を行おう。  

rubyの切り替えは`global`コマンドで指定する。  

    $ rbenv global 2.4.1

インストールしたものをrbenvで指定されているから確認する。  

    $ rbenv versions

#### Step4 rubyの確認
上記のすべてを終えることができたらrubyのバージョンが変わっているかどうか確認する。  

    $ ruby -v

もしこれで2.4.1のバージョンになっていなければPATHが通っていないか、2.4.1をインストールできていない可能性がある。  
