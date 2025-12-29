# 投稿準備

作成した台本を投稿用にストックし、管理します。

## 使い方

```
/post                    # 台本一覧から投稿準備
/post status             # 投稿ステータス確認
/post done <id>          # 投稿完了をマーク
```

## 実行内容

1. **投稿準備**
   - 台本を投稿ストックに追加
   - プラットフォーム選択（TikTok/YouTube Shorts）
   - 投稿予定日設定

2. **ステータス管理**
   - 準備中 / 投稿済み / 分析中
   - 投稿日時の記録

3. **履歴管理**
   - 使用したネタを「使用済み」に更新
   - パフォーマンス記録（手動入力）

## 投稿ファイル形式

```json
{
  "id": "post_20241229_001",
  "scriptId": "script_xxx",
  "netaId": "neta_xxx",
  "platform": ["TikTok", "YouTube Shorts"],
  "status": "ready",
  "scheduledAt": "2024-12-30T18:00:00Z",
  "postedAt": null,
  "performance": {
    "views": null,
    "likes": null,
    "comments": null
  }
}
```

## 引数

$ARGUMENTS - サブコマンド（status, done <id>）
