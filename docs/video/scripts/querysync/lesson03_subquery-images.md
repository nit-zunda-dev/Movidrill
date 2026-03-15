# QuerySync Lesson 3: 動画用画像一覧・AI生成プロンプト

台本 [lesson03_subquery.md](./lesson03_subquery.md) に対応する動画で使う画像の一覧と、AI画像生成用のプロンプト文をまとめたドキュメント。

---

## 動画内で必要な画像一覧

動画のどのタイミングで何の画像を使うかを抜け漏れなく列挙する。テロップ・コードはCapCutのテキストで対応可能。**図解・概念説明用**の画像をAI生成する前提で整理する。

| No. | 画像の内容 | 使用タイミング（目安） | 備考 |
|:--|:--|:--|:--|
| 1 | SELECTの中にSELECTが入っているイメージ | イントロ | 外側のSELECTと内側の( SELECT )が入れ子になっている図 |
| 2 | 今日やる4ステップの流れ図 | イントロ | サブクエリのイメージ→WHEREでスカラー→INとサブクエリ→FROMのサブクエリを矢印で |
| 3 | 外側のSELECTと内側のSELECTの図解 | Step 1 | WHERE の値のところに (SELECT ...) がはまっている構文図 |
| 4 | employeesテーブル見本 | Step 1〜2 | id, name, department_id, salary, hire_date の表（サンプル値） |
| 5 | WHERE と スカラーサブクエリの構文図解 | Step 2 | WHERE 列 > (SELECT AVG(...) ...) のパーツをラベル付きで |
| 6 | departments と employees の関係 | Step 3 | 部署テーブルと社員テーブル、id / department_id の対応が分かる図 |
| 7 | IN (SELECT ...) のイメージ図 | Step 3 | 複数行の結果が IN のなかに入り「どれかと一致」で絞る図 |
| 8 | FROM (SELECT ...) のイメージ・派生テーブル | Step 4 | サブクエリの結果が表になり、その上に外側のSELECTがかかる図 |
| 9 | まとめ：サブクエリの種類と書き場所 | まとめ | WHERE（スカラー・IN）と FROM（派生テーブル）を1枚で |
| 10 | めたん（講師）立ち絵・表情パターン | 全編 | 説明・うなずき・笑顔など。小窓・カットイン用 |
| 11 | ずんだもん（生徒）立ち絵・表情パターン | 全編 | 聞いてる・なるほど・喜びなど。小窓・カットイン用 |

※ 10・11は公式イラストの利用が可能ならそれを優先し、同一トーンの自作が必要な場合のみAI生成を検討する。

---

## AI画像生成用プロンプト文

以下は画像No.1〜9およびキャラクター用のプロンプト例。英語ベースで、スタイルを「教育動画向け・シンプル・視認性高め」に統一する。

---

### No.1 SELECTの中にSELECTが入っているイメージ

```
Educational diagram for SQL tutorial. Concept of subquery: one SELECT statement with another SELECT inside parentheses, like "SELECT ... WHERE col > ( SELECT ... )". Show outer query and inner query with labels or boxes. Clean flat design, white or light gray background. No realistic photos. Style: modern infographic for YouTube programming tutorial.
```

**日本語で依頼する場合：**  
SQL解説用の図。サブクエリのイメージ：SELECT のなかにかっこでくくった別の SELECT が入っている様子。「SELECT … WHERE col > ( SELECT … )」のような形。外側のクエリと内側のクエリを箱やラベルで。シンプルなフラット、白または薄いグレー背景。YouTubeプログラミング解説向け。

---

### No.2 今日やる4ステップの流れ図

```
Flowchart for SQL subquery tutorial. Four steps in order with arrows: (1) image of subquery (SELECT inside SELECT), (2) WHERE with scalar subquery, (3) IN with subquery, (4) FROM with subquery (derived table). Flat design, light background, each step in a rounded box. Labels in English. Style: clear educational diagram for video.
```

**日本語で依頼する場合：**  
SQLサブクエリ入門用の流れ図。4ステップを矢印で：(1)サブクエリのイメージ (2)WHEREでスカラー (3)INとサブクエリ (4)FROMのサブクエリ。角丸の箱、薄い背景、教育向けで見やすいデザイン。

---

### No.3 外側のSELECTと内側のSELECTの図解

```
Educational infographic: SQL subquery in WHERE clause. "WHERE salary > ( SELECT AVG(salary) FROM employees )". Label outer SELECT and inner SELECT (in parentheses). Show that inner query runs first and returns one value. Simple boxes or brackets, light background. For coding tutorial video.
```

**日本語で依頼する場合：**  
WHERE句にサブクエリが入っている図。「WHERE salary > ( SELECT AVG(salary) FROM employees )」をパーツに分け、外側のSELECTと内側のSELECT（かっこ内）をラベルで表示。内側が先に実行されてひとつの値になることを示す。シンプルな箱や括弧、薄い背景、コーディング解説動画用。

---

### No.4 employeesテーブル見本

```
Clean table graphic for tutorial. Table name "employees". Columns: id, name, department_id, salary, hire_date. Show 3-4 sample rows with placeholder data. Simple grid, white background, readable font. For programming education. Same style as lesson01/02 employees table.
```

**日本語で依頼する場合：**  
解説用の表。「employees」テーブル。列：id, name, department_id, salary, hire_date。サンプルで3〜4行。シンプルなグリッド、白背景、読みやすいフォント。レッスン1・2の employees と同一トーンで。

---

### No.5 WHERE と スカラーサブクエリの構文図解

```
Educational diagram: SQL WHERE with scalar subquery. "WHERE column > ( SELECT AVG(column) FROM table )". Parts labeled: WHERE, column, comparison operator, parentheses, subquery returning one value. Flat design, light background. For SQL tutorial video.
```

**日本語で依頼する場合：**  
WHERE句とスカラーサブクエリの構文図。「WHERE 列 > ( SELECT AVG(列) FROM テーブル )」を分解し、WHERE・列・比較演算子・かっこ・1つの値を返すサブクエリをラベルで。フラット、薄い背景、SQL解説動画用。

---

### No.6 departments と employees の関係

```
Simple diagram for database tutorial. Two tables: "departments" (id, name) and "employees" (id, name, department_id, ...). Show link from employees.department_id to departments.id. Minimal style, white background. For subquery tutorial when using IN (SELECT id FROM departments WHERE ...).
```

**日本語で依頼する場合：**  
データベース解説用の図。2つのテーブル：departments（id, name）と employees（id, name, department_id, ...）。employees.department_id と departments.id の対応が分かる線や矢印。シンプル、白背景、サブクエリで IN (SELECT id FROM departments WHERE ...) を使う説明用。

---

### No.7 IN (SELECT ...) のイメージ図

```
Concept diagram for SQL: WHERE column IN ( SELECT column FROM table ). Multiple rows from subquery form a list; outer query keeps rows whose column value matches any value in that list. Funnel or set diagram. Flat design, light background. For programming tutorial.
```

**日本語で依頼する場合：**  
SQLの「WHERE 列 IN ( SELECT 列 FROM テーブル )」のイメージ図。サブクエリの複数行がリストになり、外側のクエリはそのどれかと一致する行だけ残す。漏斗や集合の図で表現。フラット、薄い背景、プログラミング解説用。

---

### No.8 FROM (SELECT ...) のイメージ・派生テーブル

```
Educational diagram: SQL derived table. FROM ( SELECT ... ) AS alias. Subquery result shown as a small table; outer query uses it as a "table". Label "derived table" or "AS alias". Flat design, light background. For tutorial on FROM subquery.
```

**日本語で依頼する場合：**  
SQLの派生テーブルの図。FROM ( SELECT … ) AS 別名。サブクエリの結果を小さな表として描き、外側のクエリがそれを「表」として使う様子。「派生テーブル」や「AS 別名」のラベル。フラット、薄い背景、FROM句のサブクエリ解説用。

---

### No.9 まとめ：サブクエリの種類と書き場所

```
Summary cheat sheet for SQL subquery. One image: WHERE with scalar (one value), WHERE with IN (multiple rows), FROM (SELECT ...) AS alias (derived table). Short labels or icons for each. Clean, minimal, light background. For video end card or recap.
```

**日本語で依頼する場合：**  
SQLサブクエリのまとめ図。1枚で：WHEREでスカラー（1つの値）、WHEREでIN（複数行）、FROM (SELECT …) AS 別名（派生テーブル）。それぞれ短いラベルやアイコン。シンプル、薄い背景、動画のまとめ用。

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

レッスン1・2と同様。動画内で「ここで手を動かしてみましょう」と表示するときのバナー。

```
Simple banner or frame for video. Text area left blank or with placeholder "Try it yourself!". Bright but not harsh color (e.g. soft blue or green). Rounded rectangle. Suitable for overlay on tutorial video. Minimal design, no character.
```

**日本語で依頼する場合：**  
動画用のシンプルなバナー。「ここで手を動かしてみましょう」用の枠。明るめでも主張しすぎない色（薄い青や緑）。角丸長方形。オーバーレイ用、ミニマル、キャラなし。
