# QualityForward API Specification

## 変更履歴

[CHANGELOG.md](./CHANGLOG.md)を参照してください。

## specフォルダ構成

- [OpenAPI file management](https://redocly.com/docs/cli/file-management)

```folders.md

spec
├── components
│   ├── parameters # クエリパラメータ、パスパラメータの定義ファイルをまとめたもの
│   └── requestBodies # リクエストボディ定義ファイルをまとめたもの
|   └── responses # レスポンス定義ファイルをまとめたもの
|   └── schemas # スキーマ定義ファイルをまとめたもの
|
├── paths # 各URLのファイルをまとめたもの
|
├── images # HTMLで使用する画像
|
└── openapi.yml # APIのエンドポイントやinfoセクションまわりの情報
```
