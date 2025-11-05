# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v2025110601] - 2025/11/06

### Added

- エラーレスポンスのパターン追加（登録件数上限オーバー）
  - POST 複数テストケースの作成
  - POST 複数テスト結果入力・上書き
  - POST バグカウントの登録

### Fixed

- POST テストケースの作成
  - 不要なプロパティ（`test_model_item_uuid`）の削除

## [v2025072301] - 2025/7/23

### Added

- API追加
  - POST マルチテストサイクルの作成
  - POST マルチテストサイクルの環境作成
  - POST テストスイートバージョンの紐づけ

### Fixed

- 各APIのDescriptionの修正

## [v2025062301] - 2025/6/23

### Fixed

- GET テストフェーズ情報の取得
  - レスポンスのパラメータ削除
    - `redmine_issues_url`
- POST テストフェーズの作成、PATCH テストフェーズの更新
  - リクエストボディのパラメータ追加・修正
    - `redmine_new_issue_url`を追加
    - `redmine_issues_url`の説明文を修正

## [v2025021401] - 2025/2/14

### Fixed

- POST テストスイートの作成
  - リクエストボディのパラメータ削除
    - additional_headers_json_string
- PATCH テストスイートの更新
  - リクエストボディのパラメータ削除
    - additional_headers_json_string

## [v2025020601] - 2025/2/6

### Changed

- 自動テスト結果入力
  - auto_test_results[info_url]の説明文を修正
    - 複数URLを設定する場合は、カンマ（,）で区切って記載
  - Request samplesの修正
    - 複数URL指定のサンプルを追加

## [v2024090401] - 2024/9/4

### Added

- POST 自動テスト結果入力
  - リクエストボディのパラメータ追加
    - auto_test_suite_name
    - auto_execution_device_external_key
    - auto_execution_device_name
    - auto_test_case_name
    - auto_execution_pattern_external_key
    - auto_execution_pattern_name
  - エラーレスポンスの追加
    - auto_test_suite_external_keyが未設定
    - auto_test_cycle_nameが未設定
  - サンプルコード（CURL）修正
    - 同じ"auto_test_case_external_key"、"auto_test_case_name"でデータパターンだけ異なるパターンを追加

## [v2024072301] - 2024/7/23

### Fixed

- Enumの追加
  - テストスイートバージョンのレスポンス
    - ステータス（draft,available,unavailable,waiting_for_review）
  - テストスイートバージョンのリクエスト
    - ステータス（1,2,3,4）
  - テストケースのレスポンス
    - 優先度（A ~ J）
  - テストケースのリクエスト
    - 優先度（1 ~ 10）
  - テストフェーズのリクエスト
    - バグトラッキングシステムの設定(1,2)
  - テストサイクルのレスポンス
    - ステータス（unexecuted、in_progress、waiting_for_review、complete）
    - 対象の優先度（A ~ J）
  - テストサイクルのリクエスト
    - ステータス（1,2,3,4）
    - 対象の優先度（A ~ J）
  - テスト結果のレスポンス
    - テストサイクルのステータス（unexecuted、in_progress、waiting_for_review、complete）
    - テストサイクルの対象の優先度（A ~ J）
    - テスト結果（pass,fail,skip,cut,block,na,qa）
  - テスト結果のリクエスト
    - テスト結果（1 ~ 7）

- 項目説明文でx-www-form-urlencoded形式で表現していたものをJSON形式に修正
  - 修正前：test_result[content]
  - 修正後：test_result["content"]
  - 変更箇所
    - テストスイートの作成
    - テストスイートの更新
    - テストスイートバージョンの作成
    - テストスイートバージョンの更新
    - テストケースの作成
    - 複数テストケースの作成
    - テストケースの更新
    - テストフェーズの更新
    - テスト結果入力・上書き
    - 複数テスト結果入力・上書き

## [v2024070801] - 2024/7/8

### Fixed

- リクエストボディ定義をapplication/json形式に修正
  - POST テストスイートの作成
  - PATCH テストスイートの更新
  - POST テストスイートバージョンの作成
  - PATCH テストスイートバージョンの更新
  - POST テストケースの作成
  - PATCH テストケースの更新
  - POST テストフェーズの作成
  - PATCH テストフェーズの更新
  - POST テストサイクルの作成
  - PATCH テストサイクルの更新
  - POST テスト結果入力・上書き
  - PATCH テスト結果の更新

## [v2024070401] - 2024/7/4

### Fixed

- POST 自動テスト結果入力
  - リクエストボディ resultの説明文の修正

## [v2024070302] - 2024/7/3

### Added

- サンプルcurlコマンドの追加
  - POST 複数テストケース作成
  - POST 複数テスト結果入力・上書き
  - POST 自動テスト結果入力
- レスポンスの追加
  - 400 BadRequest

### Fixed

- リクエストボディの修正
  - POST 複数テストケース作成
  - POST 複数テスト結果入力・上書き
  - POST 自動テスト結果入力

## [v2024070301] - 2024/7/3

- 新規作成（GitHub Pages公開）
