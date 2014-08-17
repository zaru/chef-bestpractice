# 僕が考えた最強のレシピ運用ベストプラクティス

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
