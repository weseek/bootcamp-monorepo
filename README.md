# WESEEK Bootcamp monorepo

## 概要

- /frontend に node アプリケーション
- /backend に rails アプリケーション
- devcontainer の features を使い各実行環境を devcontainer の中に用意している
  - 他にも java などを自由に追加することが可能な構成になっている

### TODO

- [ ] /backend/README.md の更新

## 開発スタートアップ

開発には [Visual Studio Code Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) を利用しています。Windows の場合、事前に WSL2 と Docker Desktop のインストールが必要です。

### devcontainer の起動

1. VSCode を起動して、このプロジェクトフォルダを開く
1. `Ctrl` + `Shift` + `p` でコマンドパレットを呼び出して、`Dev Containers: Rebuild and Reopen in Container` を選択
   - 文字を途中まで入力すると項目の絞り込みができます
1. 初回は各種コンテナイメージのダウンロードとビルドのため、5 ～ 10 分待つ
