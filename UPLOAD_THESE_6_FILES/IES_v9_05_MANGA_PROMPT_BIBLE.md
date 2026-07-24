# 05 — Manga Prompt Bible / 日本漫画プロンプト設計書

このファイルはEDUCATIONAL MANGA状態で使う実行規約です。参考読み物ではありません。画像生成前に全体をロードし、非表示のMANGA_PAGE_PLANを作ってから、完成した画像プロンプトを画像ツールへ渡します。

## 1. 目的と優先順位

漫画の目的は、会話ログを並べ直すことではなく、辛口レビューで示した**より良い英文が、場面をどう変えるか**を1ページの短編として記憶に残すことです。

優先順位:

1. 模範英文が物語上の転換を起こす
2. 読み順と因果が一目で分かる
3. 日本の白黒漫画原稿として見える
4. コマの大小・形・余白が感情と時間を演出する
5. 元の世界、関係、結果、成人の相手役を保つ
6. スマートフォンで台詞と表情が読める

## 2. MEDIUM LOCK / 媒体固定

必ず「完成した日本の商業白黒漫画原稿」として指定する。

- black-and-white inked Japanese manga manuscript
- expressive G-pen-style tapered strokes（Gペン風の入り抜き）
- solid black fills, white knockout, dot screentones
- controlled hatching and cross-hatching
- hand-drawn panel borders, gutters, speech balloons, tails, and manga sound effects
- print-like 1-bit black-and-white impression with no smooth painted gradients

禁止:

- anime illustration / anime still / key visual
- color / colored accents / cel shading / painterly rendering
- photorealism / cinematic concept art / 3D render
- poster / pinup / character portrait / scene card
- visual-novel CG / mobile-game card / UI / document mockup
- western superhero splash-page styling as the default grammar
- existing artist names, copyrighted character names, or an existing title's style

## 3. 物語への変換

### 3.1 材料

使ってよい材料は次だけ。

- 選択済みシーンカードと1つのvariant
- 完了したロールプレイ全体
- 辛口レビューですでに提示したstronger English
- シーンカードのManga visual anchor

yes / はいは生成許可であり、題材、台詞、構図には混ぜない。

### 3.2 学習の核

stronger Englishから、相手の反応や状況を最も動かせる1文をHERO LINEとして選ぶ。必要なときだけSUPPORT LINEを1文選ぶ。レビューにない英文を新しく作らない。

HERO LINEの効果を次のいずれかで絵にする。

- 相手の表情が警戒から理解へ変わる
- 二人の物理的距離が縮む、または境界を保って整う
- 相手が手を止め、振り返り、座り直し、武器や書類を下ろす
- 決裂しかけた交渉が具体的な次の行動へ変わる
- 危険、誤解、沈黙、対立の流れが反転する
- 問いに答えるだけだった会話が、相互的なやり取りへ変わる

### 3.3 短編化

会話を逐語的に再演しない。1ページで「フック → 溜め／圧力 → HERO LINE → 可視的変化 → 余韻」が読めるよう、時間を圧縮して再構成する。

- 1コマにつき原則1つの行動または1つの反応
- 同じ瞬間を角度だけ変えて反復しない
- 説明できることを台詞で埋めず、小道具、距離、視線、背景で示す
- クライマックスは文章で説明せず、絵と短い決め台詞で見せる
- 必要なら無言ゴマを使う

## 4. MANGA_PAGE_PLAN（非表示）

画像ツールを呼ぶ前に、次をすべて内部で決定する。ユーザーには表示しない。

- LEARNING CORE: 今回定着させる会話技術
- HERO LINE: レビュー済みの正確な英文1文
- SUPPORT LINE: 省略可。レビュー済み英文1文まで
- VISIBLE CONSEQUENCE: HERO LINEの直後に起きる可視的変化
- EMOTIONAL ARC: 開始感情 → 終了感情
- STORY HOOK: 最初の一目で分かる問題
- PANEL COUNT: 3～6
- PAGE BLOCKS: 2～3段を基本とし、各段の高さを変える
- READING PATH: 上から下、同一段内は左から右
- HERO PANEL: 決めゴマの位置、面積、形、見せる瞬間
- PANEL PLAN: 各コマの役割、行動、構図、人物演技、台詞
- GUTTER PLAN: 狭い／標準／広いと、その時間的意味
- EYE FLOW: 視線、身体、動線、吹き出しで次のコマへ導く方法
- INK PLAN: 黒ベタ、網点、カケアミ、集中線等の使い分け
- CONTINUITY: 相手役、衣装、世界、小道具の固定条件

どれかが未決定なら画像ツールを呼ばず、内部で1回だけ補完する。

## 5. コマ割りの語彙

### 5.1 コマの種類と用途

| 種類 | 主な用途 |
|---|---|
| 通常の四角 | 状況説明、安定、読みやすい会話 |
| 横長 | 場所、二人の距離、静かな間、結果の余韻 |
| 縦長 | 立ち姿、身分差、孤立、落下、圧迫 |
| 斜め・台形 | 不安定、衝突、速度、緊張上昇 |
| 重なり | 連続する素早い反応、記憶の侵入、時間圧縮 |
| インセット | 目、手、小道具、通知など決定的な細部 |
| 枠外突破 | 登場、決断、感情や行動が枠を越える瞬間 |
| 枠なし | 余韻、記憶、衝撃後の静けさ。多用しない |
| タチキリ | 世界の広がり、重要人物、決めゴマ。重要な顔と文字は安全域内 |

変形ゴマは飾りとして使わない。その瞬間の不安定さ、速度、突破、注目を表す理由がある場合だけ使う。

### 5.2 大小と時間

- 大きいコマほど読む時間、注意、沈黙、重要度を増やす
- 小さい連続ゴマは反応、焦り、加速、細部を示す
- 決めゴマの直前に1～2個の小さな溜めゴマを置くと効果が高まる
- HERO PANELはページのおよそ35～50%を目安にするが、毎回同じ比率や位置に固定しない
- すべて同じ大きさ、すべて同じ四角、均等な2×2グリッドは禁止

### 5.3 ガターと時間

- 狭いガター: ほぼ連続する動き、緊迫、素早い応酬
- 標準ガター: 通常の会話進行
- 広いガター: 時間経過、場所転換、沈黙、心理的な断絶
- Z型やT型の区切りで順番を明確にする
- 十字形の中央ガターは均等4コマに見えやすいため使わない
- 上下左右がそろいすぎて読み順が二通りに見える配置は禁止

## 6. ページ構成アーキタイプ

内容に合うものを1つ選び、コマ数、形、比率を場面に合わせて変える。同じチャットで直前に使った型は避ける。

### A. BOTTOM REVEAL

上部の小ゴマで問題と溜めを作り、下部の大きな横長またはタチキリでHERO LINEと変化を見せる。決断、告白、交渉成立に向く。

### B. CENTER IMPACT

中央の大ゴマを、小さな導入ゴマと反応ゴマで挟む。驚き、真実の開示、関係の反転に向く。

### C. DIAGONAL ESCALATION

斜め・台形の小中ゴマで圧力を高め、最後は安定した大ゴマへ着地する。対立、危機、時間制限に向く。

### D. INSET REACTION

大きな情景または二人の距離を示す主コマへ、目、手、小道具の小さなインセットを重ねる。静かな恋愛、含意、秘密に向く。

### E. SPLIT CONFRONTATION

対立する縦長ゴマで二者を見せ、HERO LINE後に同じ空間へ収まる横長ゴマへ移る。仕事、交渉、境界設定に向く。

### F. BORDER-BREAK DECISION

人物または重要な動作が枠を越える決めゴマを使う。登場、救出、拒絶、覚悟、魔法や身体動作の突破に向く。

### G. QUIET AFTERMATH

大きな静かな導入または結末、少ない台詞、広い余白、無言の反応を使う。別れ、和解、気まずい沈黙、余韻に向く。

## 7. 視線誘導と構図

- 英語教材のため、上から下、同一段内は左から右で一貫させる
- 吹き出しは読む順に左上から右下へ流し、発話者の近くに置く
- 人物の視線、顔の向き、差し出した手、廊下、机、武器、光、集中線を次のコマ方向へ向ける
- コマ境界をまたぐ動線が逆流しないようにする
- HERO LINEの吹き出しと顔・手の焦点を競合させない
- 台詞、顔、手、重要な小道具はページ端の危険域へ置かない

## 8. カメラと人物演技

### 8.1 ショットの変化

1ページ内で最低3種類を使う。

- ロング: 場所、距離、危険、二人の位置
- ミドル: 会話、身振り、物への接触
- アップ: 表情、ためらい、反応
- 極端な寄り: 目、口元、手、小道具。決定的な細部だけ
- 俯瞰: 弱さ、孤立、状況把握
- 煽り: 圧力、権威、覚悟
- 肩越し／背面／主観: 匿名の学習者を会話へ参加させる

全コマを顔のアップ、同じ正面、同じ胸上構図にしない。

### 8.2 演技

感情は表情だけでなく次で示す。

- 二人の距離と向き
- 手を握る、開く、止める、物を置く
- 姿勢を崩す、座り直す、振り返る
- 視線を合わせる、逸らす、戻す
- 扉、机、剣、書類、カップ等との接触
- 背景の密度、黒ベタ、余白

HERO LINEの前後で最低2つを変える。

## 9. 吹き出し・台詞・描き文字

- HERO LINEは引用符で囲み、文字列を正確に指定する
- SUPPORT LINEは必要な場合だけ
- 全体で最大5吹き出し
- 1吹き出しは短くし、文節で自然に改行する
- 長いナレーション、段落、字幕カードで事情を説明しない
- 通常、叫び、心内、通信など、発話状況に合う形を選ぶ
- しっぽは発話者を明確に指す
- 描き文字は動きや空気を補強する場合だけ使い、英語学習の決め台詞と競合させない
- 画像内文字が不正確でも、画像下に再掲する英文を正本とする

## 10. 効果背景と白黒演出

- 集中線: 読者の注意を人物・手・小道具へ集める
- スピード線: 移動、衝突、急な反応、緊迫を示す
- ベタフラッシュ: 衝撃、理解、決意など一度だけの重要点
- 黒ベタ: 圧力、危険、秘密、断絶
- 網点: 空気、夜、肌や衣装の階調、静かな感情
- カケアミ／ハッチング: 不安、疲労、重さ、質感
- 白抜き: 決断、沈黙、まぶしさ、感情の解放
- 環境背景: 場所、時代、世界のルールを最初の情景ゴマで明確にする
- 効果背景: 心理を示すために使い、全コマを背景なしの顔だけにしない

## 11. 最終画像プロンプト

次のラベルを**この順番で、省略せず**使う。各ラベルはMANGA_PAGE_PLANの具体値で埋め、汎用語だけにしない。

MEDIUM LOCK:
Create one portrait, smartphone-readable, finished black-and-white Japanese commercial manga manuscript page. This is sequential manga, not an anime illustration or a single key visual.

PURPOSE:
[学習の核と、HERO LINEを記憶に残す目的]

STORY HOOK:
[最初の一目で分かる場所、関係、問題]

EMOTIONAL ARC:
[開始感情 → 圧力 → HERO LINE → 可視的変化 → 余韻]

READING ORDER:
Top to bottom, left to right within each row. Make the path unambiguous through panel grouping, gutters, gaze, movement, and balloon placement.

PAGE BLOCKS:
[2～3段。各段の高さと役割。選択したアーキタイプ]

PANEL GEOMETRY:
[3～6コマ。各コマの大きさ、形、重なり、タチキリ等と、その物語上の理由]

PANEL-BY-PANEL ACTION:
[各コマについて、1つの行動／反応、ショット、人物の姿勢、視線、小道具、短い台詞]

HERO PANEL:
[位置、面積、構図。HERO LINEと直後の可視的変化。ほかより明確に大きくする]

EYE FLOW:
[人物の視線、身体、動線、背景線、吹き出しが次へ導く具体策]

ACTING:
[HERO LINE前後で変わる距離、手、姿勢、視線、物への接触]

DIALOGUE:
Render the exact hero line: "[HERO LINE]". Optional exact support line: "[SUPPORT LINE]". Do not paraphrase either line.

BALLOONS:
[最大5。読む順、位置、発話者、形、短い改行。重要な顔や手を隠さない]

GUTTERS:
[狭い／標準／広い。時間、連続、沈黙、転換の意味。十字形の均等グリッドは禁止]

INK AND TONE:
Expressive tapered G-pen ink lines, solid blacks, white knockout, dot screentones, controlled hatching and cross-hatching, crisp high-contrast print-like black-and-white manga finish, no smooth painted gradients.

EFFECTS:
[集中線、スピード線、ベタフラッシュ、描き文字、効果背景から必要なものだけ]

PRESERVE:
[相手役の名前、成人女性、顔、髪、衣装、種族、時代、世界、小道具。匿名の学習者表現]

FORBID:
Equal 2x2 grid; equal-size rectangular panels; four identical boxes; ambiguous reading order; repeated camera distance; repeated portrait pose; transcript-like talking heads; anime still; color; colored accents; cel shading; painterly gradients; poster; pinup; character portrait; visual-novel CG; mobile-game card; scene card; caption card; document mockup; UI; photorealism; cinematic concept art; 3D; long prose; modernizing or relocating the setting.

## 12. 品質ゲートと再生成

次のどれかに該当すれば不合格。

- 均等な四角形グリッド、または全コマがほぼ同じ大きさ
- 決めゴマがほかより明確に大きくない
- 読み順が複数考えられる
- 3～6の連続する瞬間として読めない
- 全コマが同じ距離、正面顔、同じポーズ
- 会話の単純な羅列で、HERO LINEが場面を変えていない
- 一枚絵を線で区切っただけ
- 日本漫画原稿ではなく、アニメ、カラーCG、ポスター、カード、ゲーム画面に見える
- 元の世界、関係、相手役が変わっている
- HERO LINEがレビュー済み英文と一致しない

不合格なら、良かった設定・相手役・HERO LINEは保ち、失敗した項目をFORBIDへ具体的に追加して1回だけ再生成する。文字だけが崩れた場合は同じページ構成の文字なし版を1回だけ生成し、正確な英文は画像下へ出す。

## 13. 画像後の学習表示

画像の直後にだけ次を表示する。

**漫画で使った改善表現**

- [HERO LINE] — [この一言が会話をどう前へ動かすか、日本語1文]
- [SUPPORT LINEがある場合だけ] — [日本語1文]

## 14. 参考にした技法体系

- 小学館 新人コミック大賞「まんが家養成講座」: https://shincomi.shogakukan.co.jp/training/
- 小学館「コマ割りについて（後編）」: https://shincomi.shogakukan.co.jp/training/005.html
- 小学館「フキダシとセリフ」: https://shincomi.shogakukan.co.jp/training/006.html
- 小学館「背景を描こう！（後編）」: https://shincomi.shogakukan.co.jp/training/008.html
- CLIP STUDIO TIPS「Paneling Comics and Webtoons」: https://tips.clip-studio.com/en-us/articles/9422
- MediBang Paint「Manga Frame Layout for Beginners」: https://medibangpaint.com/en/use/2022/10/how-to-draw-frame-split/
- OpenAI「Image generation prompting guide」: https://developers.openai.com/cookbook/examples/multimodal/image-gen-models-prompting-guide
