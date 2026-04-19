# 開発ルール

このリポジトリを運用・改善していくための手順とルールをまとめる。

---

## ドキュメント体系

| ファイル | 役割 |
|----------|------|
| `docs/spec.md` | リポジトリ・スキルの仕様定義 |
| `docs/plan.md` | フェーズ別の実装計画 |
| `docs/todo.md` | 直近の作業タスクと完了履歴 |
| `docs/knowledge.md` | 作業を通じて得たナレッジ・判断基準 |
| `docs/development.md` | このファイル。開発ルール・手順 |

### 更新のタイミング

- **spec.md**: スキルの構成や方針が変わったとき
- **plan.md**: フェーズが進んだとき、または計画を見直したとき
- **todo.md**: 作業開始・完了のたびに随時更新する
- **knowledge.md**: 新しい知見・失敗・判断基準を得たとき
- **development.md**: ルール・手順を追加・変更したとき

---

## 新規スキルを追加する手順

1. `docs/todo.md` に追加作業を記載する
2. `skills/<skill-name>/` ディレクトリを作成する
3. `docs/knowledge.md` の SKILL.md テンプレートを参考に `SKILL.md` を作成する
4. README のスキル一覧を更新する
5. 必要であれば `docs/spec.md` のカテゴリ定義を更新する
6. `docs/todo.md` の該当タスクを完了済みにする

---

## 既存スキルを改善する手順

1. 改善内容を `docs/todo.md` に記載する
2. 対象の `SKILL.md` を編集する
3. 変更の背景・理由を `docs/knowledge.md` に記録する（任意だが推奨）
4. `docs/todo.md` の該当タスクを完了済みにする

---

## ディレクトリ構成

```
/
├── README.md
├── docs/
│   ├── spec.md          # 仕様
│   ├── plan.md          # 実装計画
│   ├── todo.md          # 実装 TODO
│   ├── knowledge.md     # ナレッジ
│   └── development.md   # 開発ルール（このファイル）
└── skills/
    └── <skill-name>/
        ├── SKILL.md
        ├── examples/    # 任意
        └── templates/   # 任意
```

---

## コミットメッセージの規則

```
<type>: <概要>

type:
  feat     - 新規スキル追加、新機能
  fix      - スキル内容の修正・誤り訂正
  docs     - ドキュメントのみの変更
  refactor - スキルの構成変更（内容変更なし）
  chore    - リポジトリ管理上の雑務
```

例：
```
feat: TypeScript の型定義パターンスキルを追加
fix: Python 仮想環境スキルの手順を最新バージョンに更新
docs: development.md にコミットメッセージ規則を追記
```

---

## このドキュメントを改善するには

手順・ルールが実態と合わなくなったり、より良い方法を発見した場合は、
このファイルを直接編集し、変更内容を `docs/knowledge.md` に記録する。
