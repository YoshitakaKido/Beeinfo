# Beeinfo

## 環境構築

### Linux環境の場合
必要なもの:  
* rbenv  
* ruby-build  

### rbenvのインストール
**Step1 パッケージのインストール**  
最初にrbenvをインストールする為、以下のコマンドを実行  

    $ sudo apt-get update  
    $ sudo apt-get upgrade  
    $ sudo apt-get install -y rbenv  


調べたところ、以下のように  

    $ cd  
    $ git clone git://github.com/sstephenson/rbenv.git .rbenv  

とコマンドを打ってインストールする方法もあるらしく、  
もしパッケージからインストールできなかった場合はgitからクローンしてください。  

**Step2 PATHの設定**  
インストールしただけではPATHがないので、以下のようにしてPATHを作ってあげる。  

    $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile  
    $ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile  

PATHをとおせたら最後に以下のコマンドを実行  

    $ source ~/.bash_profile

きちんとインストールされているかどうかを以下のコマンドで確認する  

    $ rbenv --version


