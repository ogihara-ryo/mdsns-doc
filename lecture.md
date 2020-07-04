# 0章 はじめに

## 0-1 教材の目的

この教材では、Markdown を投稿できる SNS のような Ruby on Rails アプリケーションを、より実務的な手順で開発します。

[今回開発するアプリケーションサンプル]()

### この教材で得られる知識

多くのサンプルアプリケーション開発教材と比べて、以下のような慣習に触れることができます。

- GitHub を利用する
- 設計構想を Wiki に残す
- あとでやる必要のあるタスクを Issue に残す
- 開発は Pull Request を使って行う
- rubocop と ESLint でコーディング規約の順守チェックを行う
- rspec を使って自動テストを行う
- GitHub Actions を使って上記の2つに引っかかるコードを検出する
- GitHub Actions で自動で Heroku にデプロイする

### 想定読者

Ruby on Rails や React.js のチュートリアルや書籍を通じてサンプルアプリケーション開発を行った経験のある人を想定しています。「MVC とは何か」といったレベルの丁寧な解説は行いませんが、写経で進めていける教材にはなっています。

また、開発環境は macOS で既に Ruby on Rails や React.js の環境をローカルで構築したことのある方を想定しています。そうでない方は別途ご自分で環境構築の用意を行う必要があります。

### ストーリー

今回は、何らかの圧力で「Markdown を投稿して技術情報を共有できる Twitter のようなサービスを開発する」という仕事があなたに課せられたとして話を進めていきます。

## 0-2 各種アカウントの準備

開発を始める前に、まずは必要なサービスのアカウントを取得しておきましょう。

### GitHub

まだ [GitHub](https://github.com) のアカウントを作成していない方は作成しておきましょう。GitHub のアカウントは、今後あなたの営業資料の一部となります。GitHub のアカウントにはメールアドレスが必要です。持っていない方は [Gmail](https://www.google.com/intl/ja/gmail/about/) で取得するのが手取り早いでしょう。

### Heroku

## 

# 開発環境の構築

## Ruby

イントロダクションに書いた通り、本教材では macOS で既に rbenv で Ruby の環境が出来上がっているユーザーを想定しているので、異なる環境を使用している場合は適宜読み替えてください。

ruby-build を upgrade してインストール候補の Ruby のリストを最新化します。

```zsh
% rbenv upgrade ruby-build
```

現在の Ruby の最新バージョンは 2.7.1 であるため、rbenv でインストールしてグローバル環境に登録します。勿論、環境をある程度コントロールできる方はこの限りではありません。

```zsh
% rbenv install 2.7.1
% rbenv global 2.7.1
```

# 要件定義

## リポジトリの作成

まずは GitHub にリポジトリを作成することから始めます。Repository name だけ入力すれば充分です。リポジトリの名前は通常開発するアプリケーションの名前にしますが、今回は Markdown を投稿する SNS なので安直に `mdsns` のしておきましょうか。

(画像)

## Wiki に設計構想をまとめる

今回のアプリケーション開発に関わることは全て GitHub に残します。まずは今から何を作るのかを Wiki にまとめておきましょう。特に高級な仕様書を作成するわけではありませんが、箇条書き程度であったとしても開発開始段階ではどのような要望と設計思想を持っていたのかを記録しておくことは重要です。

(画像)

「設計構想」というページを作って、どんな機能を持ったアプリケーションを構想しているのかを雑にまとめます。

```md
- Markdown で技術情報を投稿する SNS
- Ruby on Rails / React.js
- GitHub 認証
- ユーザーのフォロー機能
- シンタックスハイライト
```

## Ruby on Rails

次は Ruby に rails をインストールします。

```zsh
% gem install rails
```

## PostgreSQL

## chromedriver

# Ruby on Rails アプリケーションの作成

いよいよアプリケーションの開発を始めます。

## rails new

任意のディレクトリで `rails new` コマンドを実行し、空の Ruby on Rails アプリケーションを作成します。

```zsh
% cd ~/development
% rails new mdsns -T
```

# rubocop

## コーディング規約とは

## 何故コーディング規約が必要なのか

## rubocop のインストール

## Pull Request


# rspec

## 自動テストとは

## 何故自動テストが必要なのか

## rspec のインストール

## Pull Request

# GitHub Actions

## CI とは

## 何故 CI が必要なのか

## GitHub Actions 構成ファイル(?)の作成

# デプロイ

## Heroku

## 

# データモデリング

## User

### rails generate model

## Post

### rails generate model

### 1:n の関連設定

## Follow

### rails generate model

### n:n で列名とモデル名が異なる場合の関連設定

### うまく関連が設定できたかテストで確認する

# GitHub 認証

## omniauth-github

## 認証プロバイダのモックを立てる

# フォロー機能の実装

## フォロイー一覧

## フォロワー一覧

## フォロー機能の実装

# 投稿機能の実装

## 

# タイムラインの実装

