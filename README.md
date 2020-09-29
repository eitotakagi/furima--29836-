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

| Column      | Type   | Options     |
| ----------- | ------ | ----------- |
| seller      | string | null: false |
| prince      | string | null: false |
| category    | string | null: false |
| name        | string | null: false |
| description | string | null: false |
| area        | string | null: false |
| status      | string | null: false |
| user_id     | string | null: false |

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
