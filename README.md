# README

## users テーブル

| Column      | type   | Options     |
| ----------- | ------ | ----------- |
| email       | string | null: false |
| password    | string | null: false |
| name        | string | null: false |
| profile     | text   | null: false |
| occupation  | text   | null: false | 
| position    | text   | null: false | 

### Association

- has_many :prototypes
- has_many :comments


## prototypes テーブル

| Column      | type       | Options     |
| ----------- | ---------- | ----------- |
| title       | string     | null: false |
| catch_copy  | string     | null: false |
| concept     | string     | null: false |
| user        | references | null: false |

### Association

- has_many :comments

## comments テーブル

| Column      | type       | Options     |
| ----------- | ---------- | ----------- |
| text        | string     | null: false |
| user        | references | null: false |
| prototype   | references | null: false |

### Association

- belongs_to :user
- belongs_to :prototypes

* ...
