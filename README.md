## データベース設計

### users テーブル

| Column             | Type    | Options                   |
| ------------------ | ------- | ------------------------- |
| name               | string  | null: false               |
| email              | string  | null: false, unique: true |
| encrypted_password | string  | null: false               |

#### Association

- has_one :post

### posts テーブル

| Column         | Type       | Options                        |
| -------------- | -----------| ------------------------------ |
| text           | text       | null: false                    |
| user           | references | null: false, foreign_key: true |

#### Association

- belongs_to :user