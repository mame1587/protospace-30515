# DB設計

## users テーブル

|  Column  |  Type  |   Options   |
|----------|--------|-------------|
|   email  | string | null: false |
| password | string | null: false |
|   name   | string | null: false |
| profile  |  text  | null: false |
|occupation|  text  | null: false |
| position |  text  | null: false |


### Association

* has_many :prototypes
* has_many :comments


## prototype テーブル

|   Column   |   Type     |   Options         |
|------------|------------|-------------------|
|    title   |   string   |     null:false    |
| catch_copy |    text    |     null:false    |
|   concept  |    text    |     null:false    |
|     user   | references | foreign_key: true |

### Association

## comments テーブル

|  Column     |    Type    |   Options                      |
|-------------|------------|--------------------------------|
|   text      |   text     | null: false                    |
|  prototype  | references | foreign_key: true              |
|   user      | references | foreign_key: true              |

### Association

- belongs_to :prototype
- belongs_to :user
