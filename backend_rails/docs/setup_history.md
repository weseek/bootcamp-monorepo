# プロジェクトテンプレート構築時のログ

1. 空のプロジェクトディレクトリから、VSCode を開いて devcontainer のセットアップ
    - Add Devcontainer Configuration Files -> Ruby on Rails & Postgres -> empty enter -> 3.1-bullseye
1. `.editorconfig` ファイルを追加
1. `devcontainer.json` を編集
    - `customizations` 配下のセットアップ。必要な `extensions` を列挙
1.  `docker-compose.yml` に `pgweb` を追加
1. VSCode のコマンドパレットから `Dev Containers: Rebuild and Reopen in Container` を実行
1. 起動することを確認 (以降 devcontainers の中での作業)
1. Gemfile を作成
    ```
    bundle init
    ```
1. Gemfile を編集
    ```
    gem "rails", "~> 7.0.5"
    ```
1. bundle install をして `bundle exec rails` が実行できるように
    ```
    bundle install
    ```
1. rails new を実行
    ```
    bundle exec rails new . --database postgresql --skip-hotwire
    ```
1. Gemfile に下記の gem を追加
    ```
    # group :development, :test 配下に
    gem 'annotate'
    gem 'annotate_gem', require: false
    
    gem 'pry-byebug'
    gem 'pry-rails'
    gem 'pry'
    
    gem 'rubocop'
    gem 'rubocop-performance'
    gem 'rubocop-rails'
    ```
1. プロジェクトトップページのための必要なファイルを追加 (Rails デフォルトの root ページだと分かりづらいかもしれないのでカスタムした)
    - app/controllers/root_controller.rb
    - app/views/root/index.html.erb
1. config/routes.rb を編集
    ```
    root "root#index"
    ```
