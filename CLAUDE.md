# ATik - Claude Code Context

## プロジェクト概要

**ATik** - AI × TikTok/YouTube Shorts アフィリエイト動画制作支援ツール

ショート動画の企画→台本→素材→投稿までをClaude Codeで一気通貫で行うための支援ツールです。

### ターゲットジャンル
- **退職系**: 退職代行、転職、働き方改革、副業
- **AI系**: ChatGPT、Claude、AIツール紹介、効率化Tips

### 目標
- 毎日1本以上の投稿を効率化
- ネタ出し→台本→素材準備の時間短縮

## ATik専用コマンド

Claude Code で以下のコマンドが使用可能:

| コマンド | 説明 |
|---------|------|
| `/neta` | ネタ収集・トレンド分析 |
| `/script` | 台本生成（テンプレート活用） |
| `/post` | 投稿準備・ステータス管理 |
| `/sozai` | 素材生成指示（TTS・画像） |

### 使用例

```bash
# トレンドからネタ収集
/neta AI

# VS形式で台本生成
/script VS形式

# 投稿準備
/post

# TTS用テキスト抽出
/sozai tts
```

## ディレクトリ構造

```
ATik/
├── .claude/
│   └── commands/         # ATik専用コマンド
│       ├── neta.md       # /neta
│       ├── script.md     # /script
│       ├── post.md       # /post
│       └── sozai.md      # /sozai
├── knowledge/
│   ├── neta/            # ネタストック
│   ├── scripts/         # 台本ストック
│   ├── posts/           # 投稿管理データ
│   ├── templates/       # 台本テンプレート
│   │   ├── vs.json      # VS形式
│   │   ├── ranking.json # ランキング形式
│   │   └── aruaru.json  # あるある形式
│   └── settings/
│       └── genres.json  # ジャンル・ペルソナ設定
├── app/                 # Webダッシュボード（開発予定）
└── CLAUDE.md            # このファイル
```

## 台本テンプレート

### VS形式
2つの選択肢を比較。議論を呼びやすくエンゲージメント高め。
```
【フック】〇〇 vs △△、どっちが正解？
【本題】〇〇派 / △△派
【結論】実は...
【CTA】どっち派？コメントで教えて！
```

### ランキング形式
TOP3やベスト5。1位を最後まで引っ張る。
```
【フック】〇〇 TOP3！
【3位】→【2位】→【1位】
【CTA】他にもあったらコメントで！
```

### あるある形式
共感を呼ぶネタ。いいね・シェアされやすい。
```
【フック】〇〇あるある
【あるある1-3】
【CTA】共感したらいいね！
```

## ワークフロー

```
1. /neta でトレンド収集
   ↓
2. /script でテンプレート選んで台本生成
   ↓
3. /sozai で素材生成指示（TTS・画像プロンプト）
   ↓
4. 外部ツールで素材作成（VOICEVOX, Midjourney等）
   ↓
5. CapCut等で編集
   ↓
6. /post で投稿管理
```

## 🌸 Miyabi Framework

このプロジェクトはMiyabiフレームワークで構築されています。

### 利用可能なMiyabiコマンド

- `/create-issue` - Issue作成
- `/agent-run` - Autonomous Agent実行
- `/verify` - システム動作確認
- `/deploy` - デプロイ実行

## GitHub Issues

機能開発はIssueで管理:

- [#2 ネタストック機能](../../issues/2)
- [#3 台本テンプレート機能](../../issues/3)
- [#4 Claude Code Skills実装](../../issues/4)
- [#5 素材パイプライン機能](../../issues/5)
- [#6 投稿管理機能](../../issues/6)
- [#7 ジャンル・ペルソナ設定](../../issues/7)

---

🎬 **ATik** - AI × TikTok/YouTube Shorts 制作効率化

*このファイルは Claude Code が自動的に参照します。*
