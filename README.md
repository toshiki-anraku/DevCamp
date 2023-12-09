## 概要

202312 開発合宿用 JavaScript 学習用リポジトリ

## 詳細

JavaScript の学習をするための Docker 環境を準備しています。\
app フォルダ配下に自身の学習用にディレクトリを作成し、お好きなフレームワークやライブラリの学習にお使い下さい。

## 注意点

- **app/ 配下に自分専用のディレクトリを作成下さい**
- **自分専用のブランチを作成下さい。**

## Docker コンテナ構成

- nginx
- node
- mysql
- mailhog

## ディレクトリ構成

```
├.git/
├app/               各種プロジェクト格納場所
├docker/            Dockerコンテナ構築の設定ファイル
│ ├mysql/
│ ├nginx/
│ └node/
├gitignore          Gitの追跡除外設定ファイル
├docker-compose.yml コンテナ立ち上げ時の設定ファイル
└README.md
```

## 環境構築手順

1. プロジェクトのクローン
   - `git clone git@github.com:toshiki-anraku/DevCamp.git`
1. クローンしたプロジェクトファイルへ移動
   - `cd DevCamp`
1. 自分専用ブランチの作成
   - `git branch -b {ブランチ名}`
1. 自分専用ブランチへのブランチの切り替え
   - `git checkout {ブランチ名}`
1. 自分専用ディレクトリの作成
   - `mkdir app/{ディレクトリ名}`
1. Docker コンテナの立ち上げ
   - `docker compose up -d`

## よく使うコマンド

- node コンテナ内へ入る
  - `docker exec -it dev_camp_node bash`
- main ブランチを自身のブランチに取り込む
  - `git pull origin main`
