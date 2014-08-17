# 僕が考えた最強のレシピ運用ベストプラクティス

## vagrant box追加と起動

### vagrant boxを追加
`
$ vagrant box add centos65 https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box
`

### vagrantを起動
`
$ vagrant up
$ vagrant ssh-config --host centos65 >> ~/.ssh/config
`

## bundle install

`
$ bundle install --path vendor/bundle --binstubs vendor/bin
`

## レシピを追加

`
$ cd chef-repo
クックブックのインストールの時にcookbooksディレクトリが存在するとエラーになるので削除
$ rm -rf cookbooks
クックブックのインストール
$ ../vendor/bin/berks vendor cookbooks
`

## 仮想環境にchefをインストール

`
$ ../vendor/bin/kinfe solo prepare centos65
`
