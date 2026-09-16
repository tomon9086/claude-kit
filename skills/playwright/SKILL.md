---
name: playwright
description: Use this skill when the user wants to automate a browser, take screenshots of web pages, scrape web content, or interact with UI elements in a browser.
user-invocable: true
---

# Playwright Browser Automation

`@playwright/mcp` を使ってブラウザを自動操作する。

## セットアップ確認

まず MCP サーバーが設定済みかを確認する。
Claude Code の設定ファイル（`~/Library/Application Support/Claude/claude_desktop_config.json` または `~/.claude/settings.json`）に以下があるか確認:

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    }
  }
}
```

未設定の場合は上記を追加してから Claude Code を再起動するようにユーザーへ案内する。

## スクリーンショット取得

1. `browser_navigate` で対象 URL へ移動
2. `browser_screenshot` で画面を撮影
3. 画像をユーザーに提示し、確認できた内容を要約する

## Web スクレイピング

1. `browser_navigate` で対象 URL へ移動
2. 必要に応じて `browser_wait_for` でコンテンツのロードを待機
3. `browser_get_text` または `browser_snapshot` でコンテンツを取得
4. ユーザーの意図に合わせて情報を整理して返す（形式は自由）

## 共通注意事項

- セッションは原則 headless（ログイン済みセッションを前提としない）
- ログインが必要なページはユーザーに事前に確認する
- 大量のページを連続取得する場合はレート制限に配慮する
