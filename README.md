# Beeinfo

## 環境構築

### Linux環境の場合
必要なもの:  
* rbenv  
* ruby-build  

***rbenvのインストール***  
**Step1** rbenvをインストールする。  
`$sudo apt-get install -y rbenv`


調べたところ、以下のように  

`$git clone git://github.com/sstephenson/rbenv.git .rbenv`  

とコマンドを打ってインストールする方法もあるらしく、  
もしパッケージからインストールできなかった場合はgitからクローンしてください。  


`$ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile`
`$ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile`
