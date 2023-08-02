# WESEEK Bootcamp backend cource with Node.js + TypeScript + Express + Prisma + MongoDB

## 各ソフトウェアのバージョン
- Node.js `18`
- MongoDB `DockerHub latest image`
- TypeScript `^5.0.4`
- Express `^4.18.2`
- Prisma `^4.15.0`

## 開発スタートアップ

開発には [Visual Studio Code Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) を利用しています。Windows の場合、事前に WSL2 と Docker Desktop のインストールが必要です。

### devcontainer の起動

1. VSCode を起動して、このプロジェクトフォルダを開く
1. `Ctrl` + `Shift` + `p` でコマンドパレットを呼び出して、`Dev Containers: Rebuild and Reopen in Container` を選択
    - 文字を途中まで入力すると項目の絞り込みができます
1. 初回は各種コンテナイメージのダウンロードとビルドのため、5～10分待つ

### プロジェクトで必要な npm のインストール

```
$ yarn
```

### 起動

1. 次のコマンドを実行
    ```
    $ yarn dev
    ```

1. ブラウザで以下の URL にアクセスできることを確認する
    - http://localhost:3000

