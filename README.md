# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## users テーブル

| Column        | Type   | Options     |
| ------------- | ------ | ----------- |
| nickname      | string | null: false |
| email         | string | null: false |
| password      | string | null: false |
| family_name   | string | null: false |
| given_name    | string | null: false |
| family_name_fu| string | null: false |
| given_name_fu | string | null: false |
| birthday      | date   | null: false |

### Association
- has_many :items
- has_many :comments
- has_many :item_purchases

## items テーブル

| Column         | Type      | Options                      |
| -------------- | --------- | -----------                  |
| price          | integer   | null: false                  |
| category_id    | integer   | null: false                  |
| name           | string    | null: false                  |
| description    | text      | null: false                  |
| prefecture_id  | integer   | null: false                  |
| status_id      | integer   | null: false                  |
| user           | references| null: false,foreign_key: true|
| delivery_fee_id| integer   | null: false                  |
| duration_id    | integer   | null: false                  |

### Association
- belongs_to :user
- has_many :comments
- has_one :item_purchase

## comments テーブル

| Column     | Type       | Options                      |
| ---------- | ---------- | ---------------------------- |
| text       | string     | null: false                  |
| user       | references | null: false,foreign_key: true|
| item       | references | null: false,foreign_key: true|

### Association
- belongs_to :user
- belongs_to :item

## buyers テーブル

| Column        | Type      | Options                       |
| ------------- | --------- | ----------------------------- |
| postal_code   | string    | null: false                   |
| prefecture_id | integer   | null: false                   |
| municipality  | string    | null: false                   |
| address       | string    | null: false                   |
| building_name | string    |                               |
| phone_number  | string    |null: false,                   |
| item_purchase | references| null: false, foreign_key: true|

### Association
- belongs_to :item_purchase

## item_purchases テーブル

| Column     | Type      | Options                      |
| user       | references| null: false,foreign_key: true|
| item       | references| null: false,foreign_key: true|

### Association
- has_one :buyer
- belongs_to :user
- belongs_to :item