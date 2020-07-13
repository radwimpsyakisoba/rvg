## rvg DB設計
## usersテーブル

|Colum|Type|Options|
|-----|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :videos
- has_many :comments

## videosテーブル
|Colum|Type|Options|
|-----|----|-------|
|video|text||
|text|text||
user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- has_many :comments

## commentsテーブル
|Colum|Type|Options|
|-----|----|-------|
|text|text|null: false, false|
|user_id|integer|null: false, false, foreign_key: true|
|video_id|integer|null: false, false, foreign_key: true|
### Association
- belongs_to :tweet
- belongs_to :user
