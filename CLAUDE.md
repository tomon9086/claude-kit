# claude-kit

複数のプロジェクトをまたいで再利用できる Claude 用スキル（SKILL.md）・ナレッジを一元管理するリポジトリ。

## スキル管理

スキルは `skills/<name>/SKILL.md` として定義する。
Claude が文脈から自律的に呼び出す。`user-invocable: true` にするとユーザーも名前で明示的に呼べる。

## 出力ファイルの保存

スキルや処理の実行結果を保存する場合は `output/<YYYYMMDD_HHMMSS>/` ディレクトリに格納する。
`output/` 配下のサブディレクトリは `.gitignore` で除外されているため、実行結果はリポジトリに残らない。

## 開発ガイドライン

- 新しいスキルを追加するときは [docs/development.md](docs/development.md) の手順に従う
- 運用中に得たナレッジは [docs/knowledge.md](docs/knowledge.md) に追記する
- スキルの構成や方針は [docs/spec.md](docs/spec.md) を参照する
- 直近の作業状況は [docs/todo.md](docs/todo.md) を参照する
