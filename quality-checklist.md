# 品質チェックリスト

## 1. 倫理チェックリスト（投稿前に必ず確認）

- [ ] AIに全文を書かせていない：内容の構想と骨格は自分で作成している
- [ ] アイデアはすべて自分のものである：研究の着想，仮説，解釈は自分に帰属する
- [ ] AIの修正・提案はすべて確認している：AIの出力を無批判にコピペしていない
- [ ] 自分のレベルに見合った表現を使用している：Augmented Competenceの範囲内
- [ ] 書き手のvoiceは保たれている：「誰が書いても同じ」文章になっていない

## 2. 投稿前チェックリスト

### 内容・構成
- [ ] RQに対してResults/Discussionで回答しているか
- [ ] Introduction→Methods→Results→Discussionの論理的な流れが一貫しているか
- [ ] セクション間で内容の重複や矛盾がないか
- [ ] Abstractと本文の数値・結論が一致しているか
- [ ] Abstractに本文にない情報が入っていないか

### 文体・表記
- [ ] 英米スペリングが統一されているか
- [ ] 数字の表記が一貫しているか（文頭はスペルアウト，10未満はスペルアウト等）
- [ ] 略語は初出時にフルスペルを記載しているか
- [ ] 一人称の使用が一貫しているか（we/I混在なし）
- [ ] ヘッジの強度が同等の主張で揃っているか
- [ ] AI生成文で目立ちやすい語や定型表現が，不必要に反復していないか

### 図表・参考文献
- [ ] すべての図表が本文で言及されているか
- [ ] 図表のキャプションは自己完結的か（図表だけで内容がわかるか）
- [ ] 本文中のすべての引用がReferenceリストにあるか
- [ ] Referenceリストのすべての文献が本文中で引用されているか
- [ ] DOIが正しいか（Crossrefで検証）
- [ ] 引用スタイルが投稿先の規定に従っているか

### 投稿規定
- [ ] 語数制限を満たしているか
- [ ] フォーマット（フォント，行間，マージン等）が規定に従っているか
- [ ] AI利用の申告を含めているか（必要な場合）
- [ ] カバーレターを準備しているか
- [ ] 利益相反の申告を含めているか

## 3. 8つの失敗パターン検出チェック

| # | パターン | 兆候 | 対策 |
|---|---------|------|------|
| 1 | AI丸投げ型 | 骨格なしに「論文を書いて」と依頼 | 日本語骨格を先に作る |
| 2 | 架空引用型 | AIが生成した文献情報をそのまま使用 | DOIをCrossrefで検証 |
| 3 | テンス混在型 | AI生成部分と自作部分で時制がバラバラ | セクション単位で時制チェック |
| 4 | 過度な丁寧さ型 | may/might/could/possiblyの連発 | ヘッジの必要性を文ごとに判断 |
| 5 | 依存度エスカレーション型 | 最初は校正だけだったのに段落生成まで | 自分用ルールを最初に決める |
| 6 | 文体キメラ型 | AI生成部分だけ妙に流暢 | 全体の文体一貫性チェック |
| 7 | 無批判採用型 | AIの提案を100%採用 | 必ず候補から選ぶプロセスを入れる |
| 8 | セキュリティリスク型 | 未発表データをAIに入力 | 機密情報の入力を避ける |

## 4. ファクトチェック手順

### 文献の実在確認フロー

1. 著者名＋年＋タイトルでGoogle Scholarを検索
2. DOIをCrossref（https://search.crossref.org/）で検証
3. DOIのURLにアクセスして実在を確認
4. 本文中の引用内容と原典の内容が一致するか確認

### AIのハルシネーション4類型

| 類型 | 説明 | 危険度 |
|-----|------|-------|
| 完全捏造 | 著者名・タイトル・DOIすべて架空 | 極高 |
| 部分捏造 | 実在する著者名＋架空の論文タイトル | 高（発見しにくい） |
| 情報の歪曲 | 実在する論文の内容を不正確に要約 | 中 |
| 文脈の逸脱 | 正確だが引用の文脈が不適切 | 中 |

## 5. Methods曖昧表現チェック

| 曖昧な表現 | 改善例 |
|-----------|-------|
| Several participants were excluded. | Three participants were excluded due to incomplete responses. |
| The test was administered. | The test was administered individually in a quiet room. |
| Data were analyzed statistically. | Data were analyzed using a paired-samples t-test. |
| The software was used. | R (version 4.3.1; R Core Team, 2023) was used. |
| Participants were given enough time. | Participants were given 30 minutes. |
| A questionnaire was used. | A 20-item questionnaire using a 6-point Likert scale was used. |

## 6. AI導入の段階的アプローチ

| Phase | 内容 | リスク |
|-------|------|-------|
| Phase 1 | チェック・校正（文法，スペル） | 低 |
| Phase 2 | 表現の改善（言い換え，文体調整） | 低〜中 |
| Phase 3 | 構造・論理の支援（アウトライン，構成チェック） | 中 |
| Phase 4 | ドラフト支援（日本語→英語変換） | 中〜高（要申告） |

初めてAIを論文執筆に使う場合は Phase 1 から始め，慣れてから段階的に拡大する。

## 7. コーパスツール一覧

| ツール | 用途 | URL |
|-------|------|-----|
| AntConc | 自作コーパスの検索・分析 | https://www.laurenceanthony.net/software/antconc/ |
| Academic Phrasebank | セクション別の定型表現集 | https://www.phrasebank.manchester.ac.uk/ |
| COCA | 米英語汎用コーパス（Academicセクションあり） | https://www.english-corpora.org/coca/ |
| Google Scholar | ダブルクォーテーション検索で表現の頻度確認 | https://scholar.google.com/ |
| Crossref | DOIの検証 | https://search.crossref.org/ |
| CorpusMate | 学術英語特化コーパス | https://corpusmate.com/ |
