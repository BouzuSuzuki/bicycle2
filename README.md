# README

## アプリ名
ロードバイク 愛車紹介

## イメージ
![Bicycle](https://user-images.githubusercontent.com/65278048/85391400-140e9800-b585-11ea-9a93-753e815d0ee1.jpg)

## 本番環境
URL
http://52.197.89.227/

## テストアカウント＆ID
Nickname
test

Email
test@yahoo.ne.jp

Password
testtest

Password confirmation
testtest

## 制作背景(意図)
自転車好きは自分の自転車に何かしらのこだわりや好きなポイントがあります。
紹介できるサイトがあるといいなと思い作成しました。


## 機能一覧
一覧表示機能
ログイン機能
投稿機能
コメント機能
削除機能
検索機能


## 使用技術(開発環境)

## 課題や今後実装したい機能
画像の複数枚投稿
いいね機能

## ロードバイク 愛車紹介 DB設計
## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|nickname|string|null: false|

### Association
- has_many :tweets
- has_many :comments

## tweetsテーブル
|Column|Type|Options|
|------|----|-------|
|image|text| |
|text|text| |
|user_id|integer| null: false, foreign_key: true|

### Association
- belongs_to :user
- has_many :comments

## commentsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text| null: false|
|user_id|text|integer	null: false, foreign_key: true|
|tweet_id|integer| null: false, foreign_key: true|

### Association
- belongs_to :tweet
- belongs_to :user