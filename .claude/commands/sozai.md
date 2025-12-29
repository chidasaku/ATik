# 素材生成指示

台本から音声・画像用の素材生成プロンプトを作成します。

## 使い方

```
/sozai                   # 台本一覧から選択
/sozai tts               # TTS用テキスト抽出
/sozai image             # 画像生成プロンプト作成
```

## 実行内容

### TTS用テキスト抽出
- 台本からナレーション部分を抽出
- 読みやすい形に整形
- VOICEVOX/ElevenLabs用に最適化

### 画像生成プロンプト
- シーンごとの画像プロンプトを生成
- Midjourney/DALL-E形式
- 縦型動画用のアスペクト比指定

## 出力形式

### TTS用
```
【シーン1】
テキスト: 〇〇 vs △△、どっちが正解？
推奨音声: 元気/疑問系
時間目安: 3秒

【シーン2】
...
```

### 画像用
```
【シーン1】
プロンプト: [professional office scene, split screen comparison, modern UI, --ar 9:16]
スタイル: モダン/ビジネス

【シーン2】
...
```

## 引数

$ARGUMENTS - 出力タイプ（tts, image）
