# 0章 はじめに

## 0-1 教材の目的

### この教材で得られる知識

### 想定読者

### ストーリー

## 0-2 各種アカウントの準備

### GitHub

### Heroku

## 0-3 開発環境の構築

### Ruby

### Ruby on Rails

### PostgreSQL

### chromedriver

### GitHub ssh 接続

### heroku cli

# 1章 開発の始まり

## 1-1 リポジトリの作成

## 1-2 要件定義

### Wiki の作成

### 設計構想の記述

## 1-3 Ruby on Rails アプリケーションの作成

### rails new

### rails server

### push

## 1-4 データベースの作成

### rails db:create

### rails db:migrate

## 1-5 トップページの作成

### branch の作成

### ルーティングの追加

### Controller の作成

### View の作成

### Pull Request

## 1-6 デプロイ

### heroku login

### heroku create

### push


# 2章 品質保証と開発効率向上のための準備

## 2-1 rubocop

### コーディング規約とは

### 何故コーディング規約が必要なのか

### rubocop のインストール

### .rubocop.yml の作成

### 既存コードの修正

### Pull Request

## 2-2 rspec

### 自動テストとは

### 何故自動テストが必要なのか

### rspec のインストール

### rails generate rspec:install

### トップページのテスト

### rubocop

### Pull Request

## 2-3 GitHub Actions

### CI/CD とは

### 何故 CI/CD が必要なのか

### GitHub Actions

### Workflow の作成

## 2-4 その他便利な Gem のインストール

### pry

### better-errors

## 2-5 Classless CSS

### 未定 (water.css, new.css, MVP.css, Sakura)

# 3章 データモデリング

## 3-1 User

### rails generate model

### rails db:migrate

## 3-2 Post

### rails generate model

### rails db:migrate

### 1:n の関連設定

## 3-3 Follow

### rails generate model

### rails db:migrate

### 列名とモデル名が異なる場合の関連付け

### 関連付けのテスト


# 4章 GitHub 認証

## 4-1 OAuth Apps の作成

## 4-2 アプリケーションに認可用の情報を登録する

### omniauth-github のインストール

### credentials の登録

### OmniAuth プロバイダーの設定

## 4-3 GitHub からのコールバックを受け取る

### 認証用リンクの設置

### コールバック用のルーティング

### コールバック用の Controller 作成

### コールバック時のパラメーター確認

## 4-4 認証機能実装

### コールバックを受けたら User を作成する

### 認証情報を session に保存する

### ログアウト

## 4-5 認証のテスト

### 認証プロバイダのモックを立てる

### テストコード


# 5章 プロフィールページの実装

## 5-1 シードデータの作成

### db/seeds.rb の作成

### rails db:seed

## 5-2 id を使わない URL に対応する

### ルーティング

### ProfilesController の作成

### User の取得

## 5-3 プロフィールの表示

### GitHub から取得した情報の表示

### テスト


# 6章 フォロー機能の実装

## 6-1 フォロイー一覧

### ルーティング

### FolloweesController の作成

### フォロイー一覧表示

### テスト

## 6-2 フォロワー一覧

### ルーティング

### FollowersController の作成

### フォロワー一覧表示

### テスト

## 6-3 フォロー機能の実装

### ルーティング

### FollowsController の作成

### フォローボタンの設置

### 非同期通信によるボタン状態の変更


# 7章 アプリケーションを形にする

## 7-1 投稿機能の実装

### ルーティング

### PostsController の作成

### 投稿フォームの実装

### テスト

## 7-2 タイムラインの実装

### トップページへの表示

### プロフィールページ

### テスト

## 7-3 リファクタリング

### パーシャルテンプレート

## 7-4 投稿の Markdown -> HTML 変換

### redcarpet

## 7-5 シンタックスハイライト

### coderay

## 7-6 今後の改善提案

### 投稿の削除

### ページネーション

### スタイリング
