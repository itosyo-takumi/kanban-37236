# テーブル設計

## users テーブル

| Column               | Type       | Options                        |
| -------------------- | ---------- | ------------------------------ |
| user                 | references | null: false,foreign_key:true   |
| email                | string     | null: false                    |
| encrypted_password   | string     | null: false                    |
| password_confirmation| string     | null: false                    |


### Association
 has_many :lists 
 
 

## lists テーブル

| Column      | Type       | Options                      |
| ----------- | ---------- | ---------------------------- |
| list_id     | integer    | null: false                  |
| title       | string     | null: false                  |
| user        | references | null: false,foreign_key:true |
### Association
 
 has_many :cards

 

## cards テーブル

| Column      | Type       | Options                      |
| ----------- | ---------- | ---------------------------- |
| card_id     | integer    | null: false                  |
| title       | string     | null: false                  |
| memo        | string     | null: false                  |
| list_id     | integer    | null: false                  |

### Association

 belongs_to :lists 
 
 


