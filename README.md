# ethical-academic-writing

倫理的かつ効率的な英語論文執筆を支援する Claude スキル

## 概要

本スキルは，水本篤（関西大学）の「[生成AIを用いた倫理的・効率的な英語論文執筆](https://langtech.jp/ai-writing/)」ガイドの原則に基づき，Claude上での英語論文執筆支援に**学術的誠実性のガードレール**を組み込んだものです。

AIに「論文を書かせる」のではなく，「自分が書いた論文をAIで診断・洗練する」ための仕組みです。

## 特徴

- **倫理ガードレール**：Augmented Competence原則（水本, 2025）に基づき，ユーザーの受容能力の範囲内での支援に限定
- **AIらしさが出やすい表現への注意喚起**：delve, showcase, pivotal など，生成文で目立ちやすい語や定型表現の不必要な反復を点検
- **8つの失敗パターン検出**：AI丸投げ，架空引用，文体キメラ等を警告
- **3段階の洗練プロセス**：内容の英語化→文体調整→表現の磨き上げ
- **セクション別テンプレート**：CARSモデル（Introduction），ムーブ分析（Discussion），APA統計書式（Results）等
- **AI利用申告の自動生成**：使用状況に応じた5段階のテンプレート（英語・日本語）
- **査読対応**：模擬査読，Response to Reviewers，カバーレターの作成支援

## ファイル構成

```
ethical-academic-writing/
├── SKILL.md                          # スキル本体（日本語）
├── SKILL-en.md                       # スキル本体（English）
├── README.md
├── LICENSE
└── references/
    ├── prompts.md                    # プロンプトテンプレート集（日本語）
    ├── prompts-en.md                 # Prompt template library (English)
    ├── style-guide.md                # 文体・ムーブ・時制ガイド（日英共通）
    ├── quality-checklist.md          # 品質チェックリスト（日本語）
    └── quality-checklist-en.md       # Quality checklists (English)
```

日本語版と英語版の主な違い：日本語版は日本語話者向けの前編集（pre-editing）の具体例や句読点ルールを含みます。英語版はL1を特定せず，非英語母語話者全般に適用できる形にしています。style-guide.mdは学術英語のルール集のため日英共通です。

## 使い方

### claude.ai（Project）— 推奨

論文執筆専用のProjectを作成し，Project Instructionsに `SKILL.md` の内容を貼り付けます。`references/` の3ファイルはProject Knowledgeとしてアップロードしてください。

論文執筆の会話はこのProject内で行うことで，倫理チェックやテンプレートが自動的に適用されます。

### claude.ai（ユーザースキル）

Claudeの用途が主に論文執筆である場合は，ユーザースキルとしてインストールすることで，全会話に自動適用できます。Settings内のスキル管理からフォルダをアップロードしてください。

> **注意**：論文以外の用途（雑談，コード相談等）でも倫理チェックが反応する場合があります。多目的にClaudeを使う方はProjectへの導入を推奨します。

### Claude Code

```bash
cp -r ethical-academic-writing ~/.claude/skills/
```

Claude Code起動時にスキルが自動読み込みされます。

## 基づいている原則

本スキルは，以下の文献・ガイドの原則を中心に，Claude上で使いやすい形に再構成したものです。原典の単純転記ではなく，プロンプトテンプレートの体系化，失敗パターンの分類，AI利用申告テンプレートの構造化など，スキルとしての運用に必要な拡張を加えています。

**中心となる出典:**

- 水本篤 (2025).「AIとライティング教育—英語ライティング教育における生成AIの活用と課題—」李在鎬・青山玲二郎（編著）『AIで言語教育は終わるのか？深まる外国語の教え方と学び方』（第8章）くろしお出版
- 水本篤「[生成AIを用いた倫理的・効率的な英語論文執筆](https://langtech.jp/ai-writing/)」（Webガイド）
- 柳瀬陽介 (2023).「AIを活用して英語論文を作成する：日本語話者にとっての課題とその対策」『情報の科学と技術』73(6), 219–224. https://doi.org/10.18919/jkg.73.6_219

**関連文献:**

- Kobak, D., González-Márquez, R., Horvát, E.-Á., & Lause, J. (2025). Delving into LLM-assisted writing in biomedical publications through excess vocabulary. *Science Advances*, *11*(27), eadt3813. https://doi.org/10.1126/sciadv.adt3813
- Mizumoto, A., Yasuda, S., & Tamura, Y. (2024). Identifying ChatGPT-generated texts in EFL students' writing: Through comparative analysis of linguistic fingerprints. *Applied Corpus Linguistics*, *4*, 100106. https://doi.org/10.1016/j.acorp.2024.100106

## このスキルがやること・やらないこと

### やること

- 日本語→英語の段階的な変換・洗練支援
- 文法・語法・論理・構成の診断
- セクション別のプロンプトテンプレート提供
- 時制・ムーブ・ヘッジ等の学術英語チェック
- AI利用申告文・作業ログの生成
- 査読シミュレーション・Response to Reviewers支援

### やらないこと

- 本文の丸ごと生成（ユーザーの骨格が必要）
- 文献・引用・DOIの生成
- データの捏造・改ざんにつながる出力
- AI検出回避を目的とした書き換え（humanizer的使用）

## ライセンス / License

MIT License

## クレジット / Credits

- 原著ガイド / Original guide: 水本篤 Atsushi Mizumoto（関西大学 Kansai University）
- スキル構成 / Skill design: 田村祐 Yu Tamura（関西大学 Kansai University）

---

## English

This repository provides a Claude skill for ethical and efficient academic paper writing, based on [Atsushi Mizumoto's guide](https://langtech.jp/ai-writing/en/). Use `SKILL-en.md` with `references/prompts-en.md`, `references/style-guide.md`, and `references/quality-checklist-en.md` for the English version. See the Japanese sections above for installation instructions (the process is the same).
