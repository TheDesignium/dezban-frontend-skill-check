# TODOアプリ
## 概要
Nuxt.jsとTypeScriptを用いてでTODOアプリを実装する。

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
- データ管理はvuexを用いても、propsによる受け渡しでもどちらでも構いません
- vueファイル内の変数等は型をつけてください。
- UIに関しては自由です
- コミットの粒度やコミットメッセージはチーム開発を意識したものにしてください。
- PC/スマートフォンの両方でデザインが崩れないようにしてください(検証ツールにて確認)
- 技術的な面でわからないものがあれば[こちら](https://github.com/TheDesignium/dezban/wiki/%E3%83%81%E3%83%A5%E3%83%BC%E3%83%88%E3%83%AA%E3%82%A2%E3%83%AB)に目を通してみてください。

## 技術スタック
- フレームワーク: Nuxt.js 2系
- 言語: TypeScript
- CSSフレームワーク: TailwindCSS


## 実行手順
### 1.環境構築をする
- [こちら](#環境構築)を参考に行ってください
### 2.作業ブランチを作成
branch名は`intern/github名/年月/todo-list`としてください。

ex) `intern/mnt3710/202401/todo-list`
```bash
$ git checkout -b ブランチ名
```
### 3.作業着手
[機能一覧](#機能一覧)を参考にtodoアプリを作成してください。

### 4.PR作成
PullRequestを作成する際は以下の項目を確認してください。

- [ ] コンポーネントファイルやイメージファイルを参照するときは@ではなく~になっているか。
- [ ] `console.log()`がコード内に残っていないか。
- [ ] `yarn lintfix`を実行し、フォーマットが整っているか。
- [ ] PR に正常に動作していることが確認できる画像、または動画を入れているか。


## 環境構築
既にインストールされているものは飛ばしてください。

また、macOSの場合の環境構築のため、windowsを使っている方は参考にして適宜調べてください。

### 1. vscodeのインストール
[こちら](https://chigusa-web.com/blog/vs-code-install/)からvscodeのインストールをする

### 2. リポジトリをローカルに持ってくる
github上にあるスキルチェックのテンプレートを自分のpcに持ってくる。

```bash
$ git clone https://github.com/TheDesignium/dezban-frontend-skill-check.git

$ cd dezban-frontend-skill-check
```
### 3. nvmのインストール
```bash
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

### 4. nodeのインストール
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
※ vscode上のターミナルで作業していて、versionが出てこない場合はvscodeを再起動する

### 5. yarnのインストール
```bash
$ npm install -g yarn
$ yarn -v
```

### 6. localhostを立ち上げる
```bash
$ yarn
$ yarn dev
```
<img src="./static/localhost.png" width="80%">

http://localhost:3000 を開く。

## vscodeの推奨拡張機能

- Vetur
- ESlint
- Prettier - Code formatter
- Tailwind CSS IntelliSense

## 想定されるエラー

### nuxt not found

package.jsonを確認(github上と同じであることを確認)

githubと違う内容であれば`git pull origin main`を実行

再度`yarn`を実行

`yarn dev`を実行
