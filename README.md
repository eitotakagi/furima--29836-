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

| Column      | Type   | Options     |
| ----------- | ------ | ----------- |
| nickname    | string | null: false |
| email       | string | null: false |
| password    | string | null: false |
| family_name | string | null: false |
| given_name  | string | null: false |

## items テーブル

<<<<<<< HEAD
<<<<<<< Updated upstream
| Column         | Type      | Options                      |
| -------------- | --------- | -----------                  |
| prince         | integer   | null: false                  |
| category_id    | integer   | null: false                  |
| name           | string    | null: false                  |
| description    | text      | null: false                  |
| area           | string    | null: false                  |
| status_id      | integer   | null: false                  |
| user           | references| null: false,foreign_key: true|
| delivery_fee_id| integer   | null: false                  |
| duration_id    | integer   | null: false                  |

=======
=======
>>>>>>> parent of 342d848... READEME2
| Column      | Type   | Options     |
| ----------- | ------ | ----------- |
| seller      | string | null: false |
| prince      | string | null: false |
| category    | string | null: false |
| name        | string | null: false |
<<<<<<< HEAD
| image       | string | null: false |
=======
>>>>>>> parent of 342d848... READEME2
| description | string | null: false |
| area        | string | null: false |
| status      | string | null: false |
| user_id     | string | null: false |
<<<<<<< HEAD
>>>>>>> Stashed changes
=======
>>>>>>> parent of 342d848... READEME2

## comments テーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| text       | string | null: false |
| user_id    | string | null: false |
| item_id    | string | null: false |

## buyers テーブル

| Column        | Type   | Options     |
| ------------- | ------ | ----------- |
| postal_code   | string | null: false |
| prefecture    | string | null: false |
| municipality  | string | null: false |
| address       | string | null: false |
| building_name | string | null: false |
