# WESEEK Bootcamp backend cource with Ruby on Rails & PostgreSQL

WESEEK Bootcamp バックエンド編の Ruby on Rails & PostgreSQL のプロジェクトテンプレートです

## 各種ソフトウェアのバージョン

- Ruby `3.1`
- Rails `~> 7.0.5`
- PostgreSQL(docker image) `13.11-bullseye`
- pgweb(docker image) `0.14.0`

## 開発スタートアップ

開発には [Visual Studio Code Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) を利用しています。Windows の場合、事前に WSL2 と Docker Desktop のインストールが必要です。

### devcontainer の起動

1. VSCode を起動して、このプロジェクトフォルダを開く
1. `Ctrl` + `Shift` + `p` でコマンドパレットを呼び出して、`Dev Containers: Rebuild and Reopen in Container` を選択
    - 文字を途中まで入力すると項目の絞り込みができます
1. 初回は各種コンテナイメージのダウンロードとビルドのため、5～10分待つ

### プロジェクトで必要な gem のインストール

```
vscode ➜ /workspaces/bootcamp-backend-ruby-on-rails (main) $ bundle install
```

### データベースの初期セットアップ

```
vscode ➜ /workspaces/bootcamp-backend-ruby-on-rails (main) $ bin/rails db:create
vscode ➜ /workspaces/bootcamp-backend-ruby-on-rails (main) $ bin/rails db:migrate
```

### 起動

1. 次のコマンドを実行
    ```
    vscode ➜ /workspaces/bootcamp-backend-ruby-on-rails (main) $ bin/rails s
    ```

1. ブラウザで以下の URL にアクセスできることを確認する
    - http://localhost:3000

1. pgweb が閲覧できるか確認
    - http://localhost:8081

# (参考) このプロジェクトセットアップ時のログ

[setup_history.md](docs/setup_history.md)
