# QuerySync Lesson 1: 動画用画像一覧・AI生成プロンプト

台本 [lesson01_select-basic.md](./lesson01_select-basic.md) に対応する動画で使う画像の一覧と、AI画像生成用のプロンプト文をまとめたドキュメント。

---

## 動画内で必要な画像一覧

動画のどのタイミングで何の画像を使うかを抜け漏れなく列挙する。テロップ・コードはCapCutのテキストで対応可能。**図解・概念説明用**の画像をAI生成する前提で整理する。

| No. | 画像の内容 | 使用タイミング（目安） | 備考 |
|:--|:--|:--|:--|
| 1 | SELECTの全体像（一文のパーツ図解） | イントロ | 「どのテーブル・どの列・どういう条件」を一文で書くイメージ |
| 2 | 今日やる5ステップの流れ図 | イントロ | 全データ→列だけ→絞る→並べ替え→集計の5つを矢印で |
| 3 | テーブルのイメージ（行と列） | Step 1 | Excelのような表。行・列がはっきり分かる図 |
| 4 | SELECT * FROM の構文図解 | Step 1 | SELECT＝選ぶ、FROM＝どこから、*＝全部の列をラベル付きで |
| 5 | employeesテーブル全体の見本 | Step 1〜5 | id, name, department, salary, hire_date、8行の表（サンプル値） |
| 6 | * と カラム指定の対比図 | Step 2 | 左：*で全部の列／右：name, department だけの2列 |
| 7 | 「列はSELECT、行はWHERE」の図解 | Step 3 | 列を選ぶ＝SELECT、行を絞る＝WHERE をイラストで |
| 8 | WHEREで絞るイメージ | Step 3 | 8人→開発部だけ→3人に減るイメージ図 |
| 9 | ORDER BYのイメージ | Step 4 | 同じ8行が「並びだけ変わる」、給与の矢印で大小を表現 |
| 10 | GROUP BYのイメージ | Step 5 | 部署ごとにまとまり、各まとまりから平均が出る図 |
| 11 | まとめ：SELECT文パーツ一覧 | まとめ | SELECT / FROM / WHERE / ORDER BY / GROUP BY の役割を1枚で |
| 12 | めたん（講師）立ち絵・表情パターン | 全編 | 説明・うなずき・笑顔など。小窓・カットイン用 |
| 13 | ずんだもん（生徒）立ち絵・表情パターン | 全編 | 聞いてる・なるほど・喜びなど。小窓・カットイン用 |

※ 12・13は公式イラストの利用が可能ならそれを優先し、同一トーンの自作が必要な場合のみAI生成を検討する。

---

## AI画像生成用プロンプト文

以下は画像No.1〜11およびキャラクター用のプロンプト例。英語ベースで、スタイルを「教育動画向け・シンプル・視認性高め」に統一する。

---

### No.1 SELECTの全体像（一文のパーツ図解）

```
Educational diagram for a programming tutorial video. One sentence split into three parts: "which table" (FROM), "which columns" (SELECT), "what conditions" (WHERE). Clean flat design, white or light gray background, simple icons or boxes with Japanese or English labels. No realistic photos. Style: modern infographic, suitable for YouTube tutorial.
```

**日本語で依頼する場合：**  
プログラミング解説動画用の図解。一文を「どのテーブル（FROM）」「どの列（SELECT）」「どんな条件（WHERE）」の3つに分けた図。シンプルなフラットデザイン、白または薄いグレー背景、箱やアイコンで区切り。YouTubeの教育動画向け。

---

### No.2 今日やる5ステップの流れ図

```
Flowchart for SQL tutorial. Five steps in order with arrows: (1) view all data, (2) select columns only, (3) filter rows with condition, (4) sort order, (5) aggregate by group. Flat design, light background, each step in a rounded box. Labels can be in English. Style: clear educational diagram for video.
```

**日本語で依頼する場合：**  
SQL入門動画用の流れ図。5ステップを矢印でつなぐ：(1)ぜんぶ見る (2)列だけ指定 (3)条件で絞る (4)並べ替え (5)集計。角丸の箱、薄い背景、教育向けで見やすいデザイン。

---

### No.3 テーブルのイメージ（行と列）

```
Simple diagram of a database table. Rows and columns like a spreadsheet. Highlight "rows" and "columns" with different colors or labels. Minimal style, white background. For programming education video. No characters.
```

**日本語で依頼する場合：**  
データベースのテーブルを表した図。行と列がはっきり分かる表形式。「行」「列」を色やラベルで強調。シンプル、白背景、教育動画用。

---

### No.4 SELECT * FROM の構文図解

```
Educational infographic: SQL clause "SELECT * FROM table". Three parts labeled: SELECT = "choose columns", FROM = "from where", asterisk * = "all columns". Simple boxes or badges, light background. For coding tutorial video.
```

**日本語で依頼する場合：**  
SQLの「SELECT * FROM テーブル名」を説明する図。SELECT＝選んで取り出す、FROM＝どこから、*＝全部の列、を箱やバッジで表示。薄い背景、コーディング解説動画用。

---

### No.5 employeesテーブル全体の見本

```
Clean table graphic for tutorial. Table name "employees". Columns: id, name, department, salary, hire_date. Show 3-4 sample rows with placeholder data (e.g. 1, Tanaka, Development, 550000, 2020-04-01). Simple grid, white background, readable font. For programming education.
```

**日本語で依頼する場合：**  
解説用の表。「employees」テーブル。列：id, name, department, salary, hire_date。サンプルで3〜4行（例：1, 田中, 開発部, 550000, 2020-04-01）。シンプルなグリッド、白背景、読みやすいフォント。

---

### No.6 * と カラム指定の対比図

```
Split comparison diagram for SQL tutorial. Left side: "SELECT *" showing many columns (all). Right side: "SELECT name, department" showing only two columns. Same table, different result width. Flat design, light background. Educational style.
```

**日本語で依頼する場合：**  
SQL解説用の左右比較図。左：SELECT * で列がたくさん。右：SELECT name, department で2列だけ。同じテーブルで結果の幅が違うイメージ。フラット、薄い背景。

---

### No.7 「列はSELECT、行はWHERE」の図解

```
Simple educational diagram: "SELECT = which columns to show", "WHERE = which rows to keep". Two concepts side by side with icons or simple illustrations. Light background, clear labels. For database tutorial video.
```

**日本語で依頼する場合：**  
「列はSELECTで決める」「行はWHEREで決める」を説明する図。2つの概念を並べて、アイコンや簡単なイラストで表現。薄い背景、ラベルは分かりやすく。

---

### No.8 WHEREで絞るイメージ

```
Concept diagram for SQL WHERE clause. Image of many person icons or rows (e.g. 8) narrowing down to fewer (e.g. 3) with a filter or funnel. Text or label "WHERE department = 'Development'". Simple, flat, light background. For programming tutorial.
```

**日本語で依頼する場合：**  
SQLのWHEREのイメージ図。たくさんの人や行（8）が、条件で少ない数（3）に絞られていく様子。フィルターや漏斗のイメージ。「WHERE department = '開発部'」のラベル。シンプル、薄い背景。

---

### No.9 ORDER BYのイメージ

```
Diagram for SQL ORDER BY. Same number of rows (e.g. 8) but order changes: before = random order, after = sorted by salary descending (high to low). Simple arrows or numbers. Flat design, light background. For tutorial video.
```

**日本語で依頼する場合：**  
ORDER BYの説明図。行の数は同じ（8）で、並びだけが変わる。左：ばらばら、右：給与の高い順。矢印や数字で表現。フラット、薄い背景。

---

### No.10 GROUP BYのイメージ

```
Educational diagram: SQL GROUP BY and AVG. Several rows grouped by "department" (e.g. 3 groups). Each group shows an "average" value. Simple boxes or circles for groups, one result row per group. Light background. For programming tutorial.
```

**日本語で依頼する場合：**  
GROUP BYとAVGの図。複数行が「部署」でグループに分かれる（例：3グループ）。各グループから「平均」が出る。グループを箱や円で、1グループ1行の結果。薄い背景。

---

### No.11 まとめ：SELECT文パーツ一覧

```
Summary cheat sheet for SQL SELECT. One image with 5 parts: SELECT (which columns), FROM (which table), WHERE (which rows), ORDER BY (sort), GROUP BY (aggregate). Each with short icon or label. Clean, minimal, light background. For video end card or recap.
```

**日本語で依頼する場合：**  
SQLのSELECT文のまとめ図。1枚で5要素：SELECT（どの列）、FROM（どのテーブル）、WHERE（どの行）、ORDER BY（並べ替え）、GROUP BY（集計）。それぞれ短いアイコンかラベル。シンプル、薄い背景、動画のまとめ用。

---

### No.12 めたん（講師）立ち絵・表情

※ めたんはVOICEVOX公式キャラクターのため、公式素材の利用を優先すること。同一トーンの自作が必要な場合のみ以下を参考にする。

```
Anime-style character sheet, one female teacher or instructor. Friendly, calm expression. Standing pose, slightly facing viewer. Clean line art, soft colors. Suitable for educational video overlay or picture-in-picture. No text. Square or portrait format.
```

**日本語で依頼する場合：**  
アニメ調の女性講師キャラ。落ち着いた優しい表情。立ち絵、やや正面。線画はクリア、色は柔らかめ。教育動画のオーバーレイや小窓用。文字なし。正方形または縦長。

---

### No.13 ずんだもん（生徒）立ち絵・表情

※ ずんだもんはVOICEVOX公式キャラクターのため、公式素材の利用を優先すること。

```
Anime-style character sheet, one young student character (boy or androgynous). Curious, listening expression. Standing pose. Clean line art, soft colors. For educational video as "student" reaction. No text. Square or portrait format.
```

**日本語で依頼する場合：**  
アニメ調の生徒キャラ（少年または中性的）。聞いている・興味津々な表情。立ち絵。線画はクリア、色は柔らかめ。教育動画の「生徒」の反応用。文字なし。正方形または縦長。

---

### 演習キュー用バナー（共通）

動画内で「ここで手を動かしてみましょう」と表示するときのバナーや枠をAIで作る場合の例。

```
Simple banner or frame for video. Text area left blank or with placeholder "Try it yourself!". Bright but not harsh color (e.g. soft blue or green). Rounded rectangle. Suitable for overlay on tutorial video. Minimal design, no character.
```

**日本語で依頼する場合：**  
動画用のシンプルなバナー。「ここで手を動かしてみましょう」用の枠。明るめでも主張しすぎない色（薄い青や緑）。角丸長方形。オーバーレイ用、ミニマル、キャラなし。
