# Tailspin Toys クラウドファンディング開発ガイドライン

これは開発者テーマのゲーム向けクラウドファンディングプラットフォームです。バックエンドは Flask の API（DB 連携は SQLAlchemy ORM）、フロントエンドは Astro/Svelte（スタイルは Tailwind CSS）を使用します。次のガイドラインに従ってください。

## コーディング標準

### コミット前に必ず行うこと

- Python テストを実行してバックエンドの動作を確認する
- フロントエンド変更時は client ディレクトリでビルドが通ること、必要に応じて E2E テストを実行して全体の動作を確認する
- API を変更した場合は、対応するテストを更新して実行し、正しく動作することを確認する
- モデルを更新した場合、必要に応じて DB マイグレーションを含める
- 新機能を追加した場合は README を更新する
- Copilot Instructionsファイルの内容も、プロジェクト構成・スクリプト・実装方針の変更に合わせて更新する

### フォーマット要件

- Python では、関数の引数と戻り値に必ず型ヒントを付けること

### Python / Flask のパターン

- DB 連携は SQLAlchemy のモデルを使用する
- ルーティングは Flask の blueprint で構成する
- RESTful な API 設計原則に従う

### Svelte / Astro のパターン

- インタラクティブな要素は Svelte を使用する
- Svelte のリアクティブモデルに従う
- 複数箇所で使う機能は再利用可能なコンポーネントとして切り出す
- ページルーティングや静的コンテンツは Astro を使用する

### スタイル

- スタイルには Tailwind CSS のクラスを使用する
- アプリ全体を通してダークモードを維持する
- UI 要素は角丸を用いる
- アクセシブルでモダンな UI/UX 原則に従う

### GitHub Actions ワークフロー

- セキュアな実装に留意する
- `permissions` を明示的に設定する
- 実行しているタスクの目的をコメントで説明する

## スクリプト

- `scripts` フォルダに各種スクリプトが存在する
- 手作業ではなく、可能な限り既存スクリプトを利用する
- 代表的なスクリプト:
    - `scripts/setup-env.sh`: Python / Node の依存関係を一括インストール
    - `scripts/run-server-tests.sh`: `setup-env` 実行後に Python テストをすべて実行
    - `scripts/start-app.sh`: `setup-env` 実行後にバックエンド/フロントエンドのサーバーを起動

## リポジトリ構成

- `server/`: Flask バックエンド
  - `models/`: SQLAlchemy ORM モデル
  - `routes/`: リソースごとに整理した API エンドポイント
  - `tests/`: API のユニットテスト
  - `utils/`: ユーティリティ
- `client/`: Astro/Svelte フロントエンド
  - `src/components/`: 再利用可能な Svelte コンポーネント
  - `src/layouts/`: Astro のレイアウトテンプレート
  - `src/pages/`: Astro のページルート
  - `src/styles/`: CSS / Tailwind の設定
- `scripts/`: 開発/デプロイスクリプト
- `data/`: データベースファイル
- `docs/`: ドキュメント
- `README.md`: プロジェクトの概要
