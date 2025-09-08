![image](https://github.com/user-attachments/assets/28942894-9754-4608-9b52-e852df7b4d49)

![Static Badge](https://img.shields.io/badge/https%3A%2F%2Fgithub.com%2Fyu-yaba%2Fgatareview-front)
<img src="https://img.shields.io/badge/-Docker-EEE.svg?logo=docker&style=flat">

## ガタレビュ！
新潟大学の授業レビューサイトのdocker-compose.ymlを管理するルートリポジトリです。

フロントエンドリポジトリはこちらです。
  * https://github.com/yu-yaba/gatareview-front

バックエンドリポジトリはこちらです。
  * https://github.com/yu-yaba/gatareview-back

# URL
https://www.gatareview.com

レスポンシブ対応をしています。

# このサービスの理念
## すべての新潟大学生に授業情報を、オープンに

* 忙しい学生、授業情報を取得しにくい学生の力になりたい。

* シラバスではわからない情報を共有することで、履修のミスマッチを減らしたい。


# デモ
### キーワード、学部での検索機能と並び替え機能があります。
![ガタレビュデモ1](https://github.com/yu-yaba/gatareview-front/assets/109569162/a7e937e3-acae-4fd0-9c88-c78297ca3b9c)


### レビューの登録ができます。
![ガタレビュデモ2](https://github.com/yu-yaba/gatareview-front/assets/109569162/e475a83c-60da-499b-8ca3-9725cb341a88)


# 機能
### ・ レビューの投稿
### ・ 検索機能
* キーワード検索
* 学部による検索
* 新しい順、レビュー件数順、評価が高い順で並び替え

# 技術スタック
| 領域 | 技術スタック |
| ---- | ---- |
| Frontend　| Next.js, TypeScript |
| Backend | Ruby on Rails (apiモード) |
| Database | MySQL (JawsDB) |
| Infra | Vercel Heroku  AWS S3 |
| Development | Docker |

# 開発環境のセットアップ
### フォルダ構造

```
|-- gatareview-front
|-- gatareview-back
|
|-- docker
|   |-- <DBのデータが入る。docker-compose buildすると自動作成されるので、ディレクトリを作成する必要はない。>
|
|-- docker-compose.yml
|-- .env
```

## リポジトリのクローン
1. このリポジトリをクローンする
2. フロントエンドリポジトリをcloneする
  * https://github.com/yu-yaba/gatareview-front
3. バックエンドリポジトリをcloneする
  * https://github.com/yu-yaba/gatareview-back


## .env
* docker-compose.ymlとRailsのdatabase.ymlのDBの設定値を管理するファイル
* ルートディレクトリ直下に作成する
* 任意の値を設定する
```env
MYSQL_ROOT_PASSWORD=your_password
MYSQL_DATABASE=your_database
MYSQL_PASSWORD=your_password
MYSQL_USER=your_user
MYSQL_HOST=db
```

## .env.local
* Next.jsの環境変数を設定するファイル
* ここでは開発環境でapiにリクエストを送信する際の値を設定する
* gatareview-front直下に作成する
```env
NEXT_PUBLIC_ENV=http://localhost:3001
```

### コンテナを起動
```
docker-compose up --build
```

# 開発以外の活動
* X（旧Twitter）でのSNS運用
* 大学でのビラ配り
* 履修登録相談会などのイベントへの参加

# 開発者
<a href="https://github.com/yu-yaba"><img width="50" src="https://avatars.githubusercontent.com/u/109569162?v=4" css></a>
