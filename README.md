# README

## users テーブル

- has_many :prototypes
- has_many :comments


| Column     | Type   | Options     |
| --------   | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

## prototype テーブル

- has_many :comments
- belongs_to :users


| Column     | Type       | Options     |
| --------   | ------     | ----------- |
| title      | string     | null: false |
| catch_copy | text       | null: false |
| concept    | text       | null: false |
| user       | references | null: false |

## comments テーブル

- belongs_to :users
- belongs_to :prototypes

| Column    | Type       | Options     |
| --------  | ------     | ----------- |
| text      | text       | null: false |
| user      | references | null: false |
| prototype | references | null: false |