# Movidrill 動画制作ドキュメント

Movidrill で利用する**技術解説動画**の台本・制作手順を管理するフォルダです。  
**めたん**（講師役）と **ずんだもん**（生徒役）で「観ていて楽しい・身につく」動画を作るための資料をまとめています。

---

## フォルダ構成

```
docs/video/
├── README.md              # 本ファイル（概要・インデックス）
├── WORKFLOW.md            # 作業手順書（VOICEVOX + CapCut でおもしろ動画を作る）
└── scripts/               # 各コンテンツの台本
    ├── _template.md       # 台本テンプレート（新規作成時はこれをコピー）
    └── [モジュール名]/    # モジュール別台本（例: querysync/, infraplay/）
        └── *.md           # レッスンごとの台本
```

---

## ドキュメント一覧

| ファイル | 説明 |
|:--|:--|
| [WORKFLOW.md](./WORKFLOW.md) | **作業手順書** — VOICEVOX（VOICEBOX）と CapCut を使い、めたん×ずんだもんでおもしろい動画を作る手順 |
| [scripts/_template.md](./scripts/_template.md) | **台本テンプレート** — 新規レッスン動画の台本を書くときのひな形 |
| [scripts/README.md](./scripts/README.md) | **台本フォルダの説明** — 台本の置き場所・命名ルール |
| [scripts/querysync/lesson01_select-basic.md](./scripts/querysync/lesson01_select-basic.md) | **台本サンプル** — QuerySync「SELECTの基本」の台本例 |
| [scripts/](./scripts/) | **台本** — 上記以外のモジュール・レッスンごとの台本 |

---

## 動画の前提（PROJECT_PLAN との対応）

- 動画は **YouTube にアップロード** し、Movidrill の画面に埋め込んで **タイムスタンプとステップを連動** させます。
- 1本の動画あたり **3〜7ステップ**、各ステップの区切りで「ここで手を動かしてみましょう」のキューを入れます。
- 詳細は [../PROJECT_PLAN.md](../PROJECT_PLAN.md) の「6. YouTube動画の設計指針」を参照してください。

---

## 更新履歴

- 2026-03-14: 初版作成（README, WORKFLOW, 台本テンプレート）
