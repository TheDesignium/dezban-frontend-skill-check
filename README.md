<<<<<<< HEAD
# sample

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).


### `pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).


=======
# TODO アプリ

## 概要

Nuxt.js と TypeScript を用いてで TODO アプリを実装する。

<img src="./static/sample.png" width="80%">

## 機能一覧

- ヘッダー
  - タイトルを中央寄せで表示
- 入力フォーム
  - タスクを入力
  - 追加ボタンをクリックでタスクをリストに追加
  - 追加後、入力値をクリア
- タスクリスト
  - 箇条書きでタスクを表示
  - タスクの右に削除ボタンを配置
  - 削除ボタンクリックでタスクを削除

## 補足

- ボタンはコンポーネント化してください
- データ管理は vuex を用いても、props による受け渡しでもどちらでも構いません
- vue ファイル内の変数等は型をつけてください。
- UI に関しては自由です
- コミットの粒度やコミットメッセージはチーム開発を意識したものにしてください。
- PC/スマートフォンの両方でデザインが崩れないようにしてください(検証ツールにて確認)
- 技術的な面でわからないものがあれば[こちら](https://github.com/TheDesignium/dezban-frontend-skill-check/wiki/%E5%8F%82%E8%80%83%E8%A8%98%E4%BA%8B)に目を通してみてください。

## 技術スタック

- フレームワーク: Nuxt.js 2 系
- 言語: TypeScript
- CSS フレームワーク: TailwindCSS

## 実行手順

### 1.環境構築をする

- [こちら](#環境構築)を参考に行ってください

### 2.作業ブランチを作成

branch 名は`intern/github名/年月/todo-list`としてください。

ex) `intern/mnt3710/202401/todo-list`

```bash
$ git checkout -b ブランチ名
```

### 3.作業着手

[機能一覧](#機能一覧)を参考に todo アプリを作成してください。

### 4.PR 作成

PullRequest を作成する際は以下の項目を確認してください。

- [ ] コンポーネントファイルやイメージファイルを参照するときは@ではなく~になっているか。
- [ ] `console.log()`がコード内に残っていないか。
- [ ] `yarn lintfix`を実行し、フォーマットが整っているか。
- [ ] PR に正常に動作していることが確認できる画像、または動画を入れているか。

## 環境構築

既にインストールされているものは飛ばしてください。

また、macOS の場合の環境構築のため、windows を使っている方は参考にして適宜調べてください。

### 1. vscode のインストール

[こちら](https://chigusa-web.com/blog/vs-code-install/)から vscode のインストールをする

### 2. リポジトリをローカルに持ってくる

github 上にあるスキルチェックのテンプレートを自分の pc に持ってくる。

```bash
$ git clone https://github.com/TheDesignium/dezban-frontend-skill-check.git

$ cd dezban-frontend-skill-check
```

### 3. nvm のインストール

```bash
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

### 4. node のインストール

```bash
$ nvm install v16.14.1
```

正常にインストールされていたら以下のようにバージョンが表示される。

```bash
$ node --version
v16.19.0
$ npm --version
8.19.3
```

※ vscode 上のターミナルで作業していて、version が出てこない場合は vscode を再起動する

### 5. yarn のインストール

```bash
$ npm install -g yarn
$ yarn -v
```

### 6. localhost を立ち上げる

```bash
$ yarn
$ yarn dev
```

<img src="./static/localhost.png" width="80%">

http://localhost:3000 を開く。

## vscode の推奨拡張機能

- Vetur
- ESlint
- Prettier - Code formatter
- Tailwind CSS IntelliSense

## 想定されるエラー

### nuxt not found

package.json を確認(github 上と同じであることを確認)

github と違う内容であれば`git pull origin main`を実行

再度`yarn`を実行

`yarn dev`を実行
>>>>>>> da9048b55354194126da0a249b1d70b56a4c5d98
