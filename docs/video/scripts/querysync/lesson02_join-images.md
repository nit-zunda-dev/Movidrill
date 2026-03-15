# QuerySync Lesson 2: 動画用画像一覧・AI生成プロンプト

台本 [lesson02_join.md](./lesson02_join.md) に対応する動画で使う画像の一覧と、AI画像生成用のプロンプト文をまとめたドキュメント。

---

## 動画内で必要な画像一覧

動画のどのタイミングで何の画像を使うかを抜け漏れなく列挙する。テロップ・コードはCapCutのテキストで対応可能。**図解・概念説明用**の画像をAI生成する前提で整理する。

| No. | 画像の内容 | 使用タイミング（目安） | 備考 |
|:--|:--|:--|:--|
| 1 | データが複数テーブルに分かれているイメージ | イントロ | 社員テーブルと部署テーブルが別々にある図。「つなげて見る」の必要性 |
| 2 | 今日やる4ステップの流れ図 | イントロ | テーブル確認→INNER JOIN→LEFT JOIN→複数結合の4つを矢印で |
| 3 | employees と departments の表・ER風 | Step 1 | 2つのテーブル構造。employees(department_id), departments(id, name) が分かる図 |
| 4 | つなぐ列の対応図（department_id と id） | Step 1 | 同じ値の行同士を線で結ぶイメージ。鍵（キー）の説明用 |
| 5 | INNER JOIN の構文図解 | Step 2 | FROM … INNER JOIN … ON … のパーツをラベル付きで |
| 6 | つながる行だけ残るイメージ（INNER JOIN） | Step 2 | 両テーブルでペアがある行だけが結果に残る図 |
| 7 | LEFT JOIN のイメージ | Step 3 | 左テーブルは全部残り、右はあればつながる・なければNULLの図 |
| 8 | 3テーブルをJOINするイメージ | Step 4 | employees → departments → projects が矢印でつながる図 |
| 9 | まとめ：JOINの種類と使い分け | まとめ | INNER JOIN / LEFT JOIN の違いを1枚で |
| 10 | めたん（講師）立ち絵・表情パターン | 全編 | 説明・うなずき・笑顔など。小窓・カットイン用 |
| 11 | ずんだもん（生徒）立ち絵・表情パターン | 全編 | 聞いてる・なるほど・喜びなど。小窓・カットイン用 |

※ 10・11は公式イラストの利用が可能ならそれを優先し、同一トーンの自作が必要な場合のみAI生成を検討する。

---

## AI画像生成用プロンプト文

以下は画像No.1〜9およびキャラクター用のプロンプト例。英語ベースで、スタイルを「教育動画向け・シンプル・視認性高め」に統一する。

---

### No.1 データが複数テーブルに分かれているイメージ

```
Educational diagram for SQL JOIN tutorial. Two separate tables: one "employees" (with columns like id, name, department_id), another "departments" (id, name). Show that data is split and they need to be "connected" to get full info. Clean flat design, white or light gray background, simple table shapes. Arrows or dotted line suggesting "join". No realistic photos. Style: modern infographic for YouTube tutorial.
```

**日本語で依頼する場合：**  
SQLのJOIN解説用。社員テーブルと部署テーブルが別々にある図。データが分かれていて「つなげて見る」必要があることが伝わるように。シンプルなフラット、白または薄いグレー背景。矢印や点線で「つなぐ」を表現。YouTube教育動画向け。

---

### No.2 今日やる4ステップの流れ図

```
Flowchart for SQL JOIN tutorial. Four steps in order with arrows: (1) confirm tables and key columns, (2) INNER JOIN, (3) LEFT JOIN, (4) join multiple tables. Flat design, light background, each step in a rounded box. Labels in English. Style: clear educational diagram for video.
```

**日本語で依頼する場合：**  
SQLのJOIN入門用の流れ図。4ステップを矢印で：(1)テーブル確認 (2)INNER JOIN (3)LEFT JOIN (4)複数結合。角丸の箱、薄い背景、教育向けで見やすいデザイン。

---

### No.3 employees と departments の表・ER風

```
Simple ER-style diagram for database tutorial. Two boxes: "employees" table with columns id, name, department_id, salary, hire_date; "departments" table with id, name. Optional: line or arrow from department_id to departments.id. Minimal style, white background. For programming education video. No characters.
```

**日本語で依頼する場合：**  
データベース解説用のER風図。2つの箱：employees（id, name, department_id, salary, hire_date）と departments（id, name）。必要なら department_id から departments.id へ線や矢印。シンプル、白背景、教育動画用。

---

### No.4 つなぐ列の対応図（department_id と id）

```
Educational diagram: two columns or tables connected by matching values. Label "department_id" (employees) and "id" (departments). Same values linked with lines or same color. Concept of "key" for JOIN. Flat design, light background. For SQL tutorial video.
```

**日本語で依頼する場合：**  
JOINの「鍵」の説明図。employees の department_id と departments の id が同じ値で線で結ばれているイメージ。同じ値の行をペアにすることを表現。フラット、薄い背景、SQL解説動画用。

---

### No.5 INNER JOIN の構文図解

```
Educational infographic: SQL "FROM table1 INNER JOIN table2 ON table1.col = table2.col". Parts labeled: FROM, INNER JOIN, ON, condition. Simple boxes or badges, light background. For coding tutorial video.
```

**日本語で依頼する場合：**  
SQLの「FROM … INNER JOIN … ON …」を説明する図。FROM、INNER JOIN、ON、条件を箱やバッジで表示。薄い背景、コーディング解説動画用。

---

### No.6 つながる行だけ残るイメージ（INNER JOIN）

```
Concept diagram for SQL INNER JOIN. Two tables side by side; only rows that have a matching pair in the other table are shown in the result. Unmatched rows faded or crossed out. Simple, flat, light background. For programming tutorial.
```

**日本語で依頼する場合：**  
INNER JOINのイメージ図。2つのテーブルを並べ、ペアがある行だけが結果に残り、合わない行は薄くしたり線で消したり。シンプル、薄い背景、プログラミング解説用。

---

### No.7 LEFT JOIN のイメージ

```
Concept diagram for SQL LEFT JOIN. Left table: all rows kept. Right table: matching rows connected; where no match, show empty or NULL. Visual difference from INNER JOIN. Flat design, light background. For SQL tutorial video.
```

**日本語で依頼する場合：**  
LEFT JOINの説明図。左テーブルは全行残す。右テーブルは合う行はつなぎ、合わないところは空またはNULL。INNERとの違いが分かるように。フラット、薄い背景、SQL解説動画用。

---

### No.8 3テーブルをJOINするイメージ

```
Diagram for SQL: three tables (e.g. employees, departments, projects) connected in sequence with arrows. Each connection labeled with "ON" or key columns. Simple boxes, flat design, light background. For tutorial on joining multiple tables.
```

**日本語で依頼する場合：**  
3テーブル（employees → departments → projects）が矢印で順につながる図。各つなぎに ON やキー列をラベル。シンプルな箱、フラット、複数テーブル結合の解説用。

---

### No.9 まとめ：JOINの種類と使い分け

```
Summary cheat sheet for SQL JOIN. One image: INNER JOIN (only matching rows) vs LEFT JOIN (left all, right if match). Short labels or icons. Clean, minimal, light background. For video end card or recap.
```

**日本語で依頼する場合：**  
SQLのJOINまとめ図。1枚で INNER JOIN（一致する行だけ）と LEFT JOIN（左は全部、右はあれば）の違いを短いラベルやアイコンで。シンプル、薄い背景、動画のまとめ用。

---

### No.10 めたん（講師）立ち絵・表情

※ めたんはVOICEVOX公式キャラクターのため、公式素材の利用を優先すること。同一トーンの自作が必要な場合のみ以下を参考にする。

```
Anime-style character sheet, one female teacher or instructor. Friendly, calm expression. Standing pose, slightly facing viewer. Clean line art, soft colors. Suitable for educational video overlay or picture-in-picture. No text. Square or portrait format.
```

**日本語で依頼する場合：**  
アニメ調の女性講師キャラ。落ち着いた優しい表情。立ち絵、やや正面。線画はクリア、色は柔らかめ。教育動画のオーバーレイや小窓用。文字なし。正方形または縦長。

---

### No.11 ずんだもん（生徒）立ち絵・表情

※ ずんだもんはVOICEVOX公式キャラクターのため、公式素材の利用を優先すること。

```
Anime-style character sheet, one young student character (boy or androgynous). Curious, listening expression. Standing pose. Clean line art, soft colors. For educational video as "student" reaction. No text. Square or portrait format.
```

**日本語で依頼する場合：**  
アニメ調の生徒キャラ（少年または中性的）。聞いている・興味津々な表情。立ち絵。線画はクリア、色は柔らかめ。教育動画の「生徒」の反応用。文字なし。正方形または縦長。

---

### 演習キュー用バナー（共通）

レッスン1と同様。動画内で「ここで手を動かしてみましょう」と表示するときのバナー。

```
Simple banner or frame for video. Text area left blank or with placeholder "Try it yourself!". Bright but not harsh color (e.g. soft blue or green). Rounded rectangle. Suitable for overlay on tutorial video. Minimal design, no character.
```

**日本語で依頼する場合：**  
動画用のシンプルなバナー。「ここで手を動かしてみましょう」用の枠。明るめでも主張しすぎない色（薄い青や緑）。角丸長方形。オーバーレイ用、ミニマル、キャラなし。
