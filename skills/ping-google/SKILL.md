---
name: ping-google
description: Use this skill when the user asks to ping google.com, check connectivity to google, or verify internet access via google.
user-invocable: true
---

google.com に ping を打って結果を報告する。

```bash
ping -c 4 google.com
```

上記コマンドを実行し、以下を簡潔に報告すること:
- 疎通の成否
- パケットロス率
- 平均 RTT (round-trip time)
