# claude-kit

複数のプロジェクトをまたいで再利用できる Claude 用スキル（SKILL.md）・ナレッジを一元管理するリポジトリ。

## ドキュメント

| ファイル | 内容 |
|----------|------|
| [docs/spec.md](docs/spec.md) | 仕様 |
| [docs/plan.md](docs/plan.md) | 実装計画 |
| [docs/todo.md](docs/todo.md) | 実装 TODO |
| [docs/knowledge.md](docs/knowledge.md) | ナレッジ |
| [docs/development.md](docs/development.md) | 開発ルール・手順 |

## スキル一覧

| スキル | 説明 |
|--------|------|
| [ping-google](skills/ping-google/SKILL.md) | google.com への ping 疎通確認 |
| [playwright](skills/playwright/SKILL.md) | Playwright MCP を使ったブラウザ自動操作・スクレイピング |

新しいスキルを追加する場合は [新規スキルの追加手順](docs/development.md#新規スキルを追加する手順) を参照してください。

## ディレクトリ構成

```
/
├── CLAUDE.md
├── README.md
├── docs/
│   ├── spec.md
│   ├── plan.md
│   ├── todo.md
│   ├── knowledge.md
│   └── development.md
├── output/           # スキル実行結果の一時保存先（.gitignore 対象）
└── skills/
    └── <skill-name>/
        └── SKILL.md
```
