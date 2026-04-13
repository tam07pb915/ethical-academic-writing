# プロンプトテンプレート集

水本（2025）のガイドに基づく，セクション別・用途別プロンプト集。

---

## 1. 日本語→英語変換

### 1.1 基本変換（第1段階）

```
以下の日本語を，意味を正確に伝える英文にしてください。
文体の美しさよりも，内容の正確さを優先してください。
新しい内容は追加しないでください。

[日本語テキスト]
```

### 1.2 文体調整（第2段階）

```
以下の英文を，学術英語の文体に調整してください。
改善点:
- 主語が長い場合は短くする
- 適切なヘッジ表現を加える（ただし過剰にしない）
- [セクション名]セクションのため，[過去形・受動態 等]を基本とする
意味は変えないでください。変更した箇所は太字にしてください。

[英文]
```

### 1.3 セクション別変換

```
以下の日本語を，英語論文の[セクション名]セクションとして自然な学術英語にしてください。

条件:
- 時制: [セクションの慣習に従う]
- 態: [受動態中心 / 能動態中心]
- ヘッジ: [適切に加える]
- 新しい内容は追加しない
- 架空の文献引用は入れない
```

### 1.4 逸脱チェック

```
この英文が，元の日本語から逸脱している箇所を箇条書きで指摘してください。

元の日本語：[日本語テキスト]
英文：[生成された英文]
```

---

## 2. 診断・チェック系

### 2.1 総合診断（5観点）

```
以下の段落について，5つの観点から総合的に点検してください。
各観点について，問題がなければ「OK」，問題があれば具体的に指摘。

(1) 時制: セクションに適した時制が一貫して使われているか
(2) 情報構造: Given-New の原則に従っているか
(3) 論理展開: 文と文のつながりに飛躍がないか
(4) 接続表現: 過不足がないか，フォーマル度は適切か
(5) パラグラフ構造: topic sentence が明確か，1パラグラフ1トピックか

セクション: [セクション名]
[段落]
```

### 2.2 弱点診断（下書き→診断）

```
次の文章の問題点を，文法・語法・論理の3カテゴリで，各3点まで指摘してください。
修正案は1案だけ。理由を短く。

[下書き]
```

### 2.3 日本語話者特有エラーの検出

```
以下の英文を，日本語話者が犯しやすい文法エラーに絞って点検してください。

特に注意すべき項目:
(1) 冠詞（a/the/無冠詞）の誤り
(2) 可算/不可算名詞の混同
(3) 不要な前置詞の付加
(4) 主述の一致
(5) 名詞の過剰な連続（noun string）

各問題について: 該当箇所，正しい表現，原因（1行）

[英文]
```

### 2.4 Reporting Verbs の点検

```
以下のIntroductionで使われている reporting verbs をすべて抽出し，一覧表にしてください。

(1) 同じ動詞が3回以上使われていないか
(2) 中立的な報告に強い動詞（proved, demonstrated等）を使っていないか
(3) 文脈に照らして不適切な動詞がないか

問題があれば指摘し，代替表現を1つずつ提案。

[本文]
```

### 2.5 Methodsの曖昧表現検出

```
以下のMethodsセクションに含まれる曖昧な表現を指摘してください。
判断基準：「別の研究者がこの記述だけで実験を再現できるか」

各指摘について:
(1) 該当箇所
(2) なぜ曖昧か
(3) どのような情報を追加すべきか（具体的な数値が不明な場合は [要追記] と表示）
```

---

## 3. セクション別執筆支援

### 3.1 Introduction構造チェック（CARSモデル）

```
以下のIntroductionを，CARSモデルの4要素で分析してください。
(1) 研究分野の重要性（Move 1）
(2) 先行研究の概観（Move 1）
(3) ギャップの指摘（Move 2）
(4) 本研究の目的（Move 3）

各要素が含まれているか，順序は適切か，ギャップは具体的かを評価。
欠けている要素があれば指摘。内容の追加は不要。

[Introduction]
```

### 3.2 参加者記述テンプレート

```
A total of [N] participants ([N] males, [N] females; M age = [X] years,
SD = [X]) took part in this study. They were [所属/属性].
Participants were recruited through [方法].
The inclusion criteria were [基準]. [N] participants were excluded
because [理由]. This study was approved by [倫理審査機関]
(approval number: [番号]). All participants provided written
informed consent prior to data collection.
```

### 3.3 Results：RQごとの構造化

```
以下の分析結果を，RQごとに整理して英語のResultsセクションとして書いてください。

条件:
- 各RQに対応する結果を小見出しで区分
- 統計値はAPA第7版の書式（イタリック，効果量を含む）
- 結果の報告に留め，深い解釈はDiscussionに回す
- 図表への言及は "As shown in Table X, ..." の形式

[分析結果の箇条書き]
```

### 3.4 Discussion構成チェック

```
以下のDiscussionを分析し，6つのムーブが含まれているか確認してください。
(1) 結果の要約  (2) 結果の解釈  (3) 先行研究との比較
(4) 含意の提示  (5) 限界の記述  (6) 今後の研究

欠けているムーブ，または順序が不自然な箇所があれば指摘。
内容の追加は不要。

[Discussion]
```

### 3.5 Abstractチェック

```
以下のAbstractについて点検してください。
(1) Background / Purpose / Methods / Results / Conclusion の5要素がすべて含まれているか
(2) 本文にない情報が混入していないか
(3) 語数は投稿規定の範囲内か

問題がある場合は指摘のみ。修正文は提示しない。

[Abstract]
```

---

## 4. 校正

### 4.1 強度調整付き校正

**最小限：** `Proofread this (minimal requirements only).`
**軽め：** `Lightly proofread this.`
**標準：** `Proofread this, improving clarity and flow.`
**踏み込み：** `Proofread this, significantly improving clarity and flow.`

### 4.2 変更箇所のみ表示

```
Proofread the following sentences and provide both the
original sentences and your suggested revisions. If they are
acceptable, you don't have to make suggestions. However,
when revisions are definitely necessary, please clearly indicate
what the original sentence was and how you recommend it should be revised.

Focus on:
- Grammar and punctuation errors
- Word choice appropriate for academic writing
- Conciseness (remove unnecessary words)
```

### 4.3 表現候補の提示

```
以下の英文の TARGET を，意味を変えずに言い換えてください。
候補を3つ。各候補について:
1) 適した場面（1行）
2) フォーマル度（高/中/低）
3) なぜこの表現が適切かの理由

TARGET: [対象表現]
CONTEXT: [前後の文を含む英文]
```

### 4.4 文体一貫性チェック

```
以下の論文原稿について，文体の一貫性を点検してください。

(1) 一人称の使用: weとIが混在していないか
(2) ヘッジの程度: 同等の確信度の主張に対して，ヘッジの強さが揃っているか

不統一な箇所を指摘し，どちらに統一すべきかを提案。

[論文原稿]
```

---

## 5. AI利用申告テンプレート

### 使用状況の判断フロー

```
AIを何に使ったか？
├─ 文法チェック・校正のみ → テンプレートA
├─ 構成相談，言い換え提案も → テンプレートB
├─ Methods等の英語化も → テンプレートC
├─ 分析コードの生成も → テンプレートD
└─ 複数ツールを併用 → テンプレートE
```

### テンプレート（英語）

**A（校正のみ）：**
> The author(s) used a generative AI tool ([TOOL]) to improve clarity and readability of the manuscript, including proofreading and wording suggestions. All content, analyses, interpretations, and final decisions remain the author(s)' responsibility.

**B（構成相談含む）：**
> The author(s) used a generative AI tool ([TOOL]) for language editing and drafting support, such as outlining, paraphrasing options, and grammar checking. The author(s) verified all statements and references and is fully responsible for the final manuscript.

**C（英語化支援含む）：**
> The author(s) used a generative AI tool ([TOOL]) to assist in converting technical procedures into natural-language descriptions and to refine wording. The author(s) ensured accuracy of all methodological descriptions and verified all factual claims and citations.

**D（コード生成含む）：**
> The author(s) used a generative AI tool ([TOOL]) for drafting support and for generating initial analysis code in R/Python. All generated code was reviewed, tested, and verified by the author(s). The author(s) is fully responsible for the accuracy of all analyses, interpretations, and the final manuscript.

**E（複数ツール）：**
> The author(s) used the following AI tools during manuscript preparation: [TOOL1] for [PURPOSE1], [TOOL2] for [PURPOSE2]. All content, analyses, and interpretations are the author(s)' own. The author(s) verified all factual claims and references and takes full responsibility for the final manuscript.

### テンプレート（日本語）

> 本稿では，文章表現の改善（明確化，言い換え，文法チェック，推敲案の提案）の範囲で生成AIを利用した。本文の主張，分析，解釈，引用・参考文献の確認，および最終稿の決定は著者が行い，その責任を負う。

---

## 6. 査読対応

### 6.1 模擬査読

```
あなたは厳格なジャーナル査読者です。以下の論文原稿を読み，査読レポートを作成してください。

- Major concerns（重大な問題）: 最大3つ
- Minor concerns（軽微な問題）: 最大5つ
- Positive aspects（評価できる点）: 最大3つ

各指摘には具体的な箇所（セクション名・段落番号）を付けてください。

[論文原稿]
```

### 6.2 査読コメントへの対応文

```
以下の査読コメントに対する回答文を英語で作成してください。

条件:
- 丁寧だが自信を持った文体
- 感謝→回答→変更箇所の明示 の順
- 変更した場合はページ番号を [要記入] として残す
- 変更しない場合は根拠を明示

査読コメント: [コメント]
対応方針（日本語で）: [同意する/部分的に同意/同意しない + 理由]
```

### 6.3 カバーレター

```
以下の情報をもとに，学術ジャーナルへの投稿用カバーレターを英語で作成してください。

条件:
- 300語以内
- 研究の新規性と意義を強調
- ジャーナルのスコープとの関連を述べる
- AI使用の申告を含める（該当する場合）

投稿先ジャーナル: [名前]
論文タイトル: [タイトル]
研究の概要（日本語）: [2-3文]
主要な知見（日本語）: [1-2文]
```

---

## 7. 作業ログ

### ログフォーマット

| 日付 | セクション | AIの用途 | 入力の種類 | 出力の扱い | 自分の確認 |
|------|-----------|---------|-----------|-----------|-----------|
| YYYY-MM-DD | [セクション名] | [用途] | [入力種別] | [採用状況] | [確認内容] |

### 詳細ログ（学位論文・競争的資金用）

```
## 変更ログ：[セクション名]（第N段落）

### YYYY-MM-DD 改善①：[改善内容]
- 使用ツール: [ツール名]
- プロンプトの要旨: [要旨]
- AIの提案: [提案内容]
- 自分の対応: [対応内容]
- 採用/不採用: [判断と理由]
```
