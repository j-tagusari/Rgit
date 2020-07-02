Rとgitの連携
===

R（Rstudio）とgitを連携させる．

# 必要なもの
 - R
 - R Studio
 - Git (Git Bash)
 - GitHubアカウント

# 手順（Rプロジェクトが既にある場合）

## GitHubで新しいレポジトリをつくる

## Git Bashでプロジェクトフォルダにリモートリポジトリをつくる

```
git init #.gitをつくる
git remote add origin https://github.com/<user.name>/<repository.name>.git #githubのリポジトリと関連付け
git add . # 全てのファイルをステージング
git commit -m "first upload" # 適当なコメントを付けてコミット
git push -u origin master # プッシュ．"-u"を付けるのがポイント．
```

## R studioでcommit

あとはRstudioの機能でcommitできる．
pushのときに-uを付け忘れると，pull/pushがグレーアウトして使えない．

## トラブルシューティング

```
fatal: remote origin already exists
> git remote rm origin
```
