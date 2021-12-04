# テーブル設計

## usersテーブル

| Column             | Type   | Options                   |
| ------------------ | ------ | ------------------------- |
| name               | string | null: false               |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false               |
| profile            | text   | null: false               |
| occupation         | text   | null: false               |
| position           | text   | null: false               |

## commentsテーブル

| Column             | Type       | Options                        |
| ------------------ | ---------- | ------------------------------ |
| comment            | texit      | null: false                    |
| user               | references | null: false, foreign_key: true |
| prototype          | references | null: false, foreign_key: true |

## prototypeaテーブル

| Column             | Type        | Options                        |
| ------------------ | ----------- | ------------------------------ |
| title              | string      | null: false                    |
| catch_copy         | text        | null: false                    |
| concept            | text        | null: false                    |
| user               | references  | null: false, foreign_key: true |
