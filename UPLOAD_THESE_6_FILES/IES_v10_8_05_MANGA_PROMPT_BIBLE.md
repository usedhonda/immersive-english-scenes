# 05 — Manga Prompt Bible / 記憶に残る日本漫画の実行規約

このファイルはEDUCATIONAL MANGA状態でだけ使う。画像生成前に全体を読み、現在チャットだけから作ったCURRENT CHAT MANGA CAPSULEを唯一の入力として、非表示のMNEMONIC STORYを先に作る。合格後だけMANGA_PAGE_PLANと最終画像プロンプトを作る。

## 1. 目的

漫画は会話記録ではない。同じシチュエーションの中で、レビューのHERO LINEを使う別エピソードを発明し、「その一言で予想外の出来事が反転した」と記憶させる。

覚える英文は1つ。英文と結び付く、会話にはなかった強い小物・動作・事件を1つ発明する。台詞を読まなくても、問題と反転が5秒で分かるようにする。

## 2. 入力の絶対条件

使用できる情報は現在チャットの表示済み内容からレビュー時に作ったCURRENT CHAT MANGA CAPSULEだけ。

- 相手名、関係、成人としての外見
- 時代、場所、世界規則
- 直前レビューに実在する完全一致のHERO LINE
- 相手名・場所・HERO LINE・新しい記憶用小物を結んだCURRENT CHAT FINGERPRINT
- 背景、人物、関係、世界規則、新事件、小物、全コマの構図・演技・動作、HERO LINE、文字、画材を完全な文にしたZERO-BASE IMAGE BLUEPRINT
- 生成後の照合だけに使う、禁止された別シーン要素。これらの固有語は画像プロンプトへ渡さない

過去データは学習履歴、好み、レベル設定だけに使い、漫画の内容へ一切使わない。画像生成時にカタログ、カード、Projectメモリ、他チャット、既定シーン、過去画像、画像ID、過去プロンプトを検索・参照しない。会話の発言、出来事、結末を漫画プロンプトへコピーしない。CAPSULEが欠けたらTutor Rules §9.3のとおり現在チャットから一度だけ再構築し、失敗時は生成しない。

## 3. 物語エンジン

同じ場所・人物・関係・世界規則を保ちながら、会話とは別の記憶用事件を発明する。コマ割りより先に、まず漫画として成立する物語を作る。

`新しい視覚的事件 → HERO LINEが必要になる溜め → HERO LINE → 予想外の反転 → 笑い・驚き・ときめき・安堵・余韻`

- 新事件: 会話にはなかった小さな事故、勘違い、発見、競争、儀式、皮肉、優しい驚き。世界規則には従う
- 溜め: HERO LINEが必要になる圧力。長い説明はしない
- HERO LINE: 学習者の改善英文を引用符で正確に指定する
- 反転: HERO LINE前後で、相手の表情／二人の距離／相手の判断／状況のうち2つ以上を目に見えて変える
- 報酬: 笑い、驚き、ときめき、安堵、余韻のうち場面に自然な1つ
- 記憶フック: 英文の意味を小物・身体動作・視覚的比喩へ変換し、前後で意味を変える

禁止: 会話の再演、あらすじ、ダイジェスト、発言順の羅列、元の問題や結末の説明、回想、事情説明、全コマの会話顔、台詞がないと変化が分からない構成。

## 4. MNEMONIC STORY GATE（非表示・最初に実行）

画像やコマ割りを考える前に、同じ人物・場所・関係・世界規則の中で、会話には存在しなかった事件を3案作る。各案は次の5点を一文ずつ決める。

1. 一目で気になる視覚的事件
2. HERO LINEを言わなければ解決しない圧力
3. HERO LINEを発した瞬間の決定的な行動
4. その一言で起きる意外で目に見える反転
5. 最後の笑い、ときめき、驚き、安堵、または余韻

各案を次の基準で内部採点する。

- 教材要素を外しても1ページ漫画として読みたい
- HERO LINEが貼り付け台詞ではなく、クライマックスの原因になっている
- 会話の問題、出来事、発言順、結末を再利用していない
- 台詞を隠しても、事件と反転が絵で分かる
- 英文の意味が小物、行動、視覚的比喩と一対一で結び付く

全項目を満たす案だけを1つ選ぶ。合格案がなければ、同じLOCKから別の3案を一度だけ作り直す。それでも合格しなければ画像ツールを呼ばない。合格した物語を非表示のMNEMONIC STORYとして固定し、その後は内容を弱めたり、会話のあらすじへ戻したりしない。

## 5. MANGA_PAGE_PLAN（非表示）

合格したMNEMONIC STORYを、初めてページへ変換する。

1. 学習上の核心
2. 完全一致のHERO LINE
3. 合格済みMNEMONIC STORYの視覚的事件、圧力、決定的行動、反転、余韻
4. HERO LINEの意味を可視化する記憶用の小物・動作
5. HERO LINE前後で変わる2項目以上
6. HERO LINEを置く決めゴマ
7. 読み順、人物の視線、吹き出し位置
8. 白黒原稿技法

ただしコマ数と吹き出し数はここで固定しない。次の可読性計算で必要な数まで減らす。

## 6. 文字サイズ優先の自動レイアウト

ページをスマホ幅390pxで全体表示した状態を基準にする。

- 画像内の文字はHERO LINEだけ。導入、圧力、反転、余韻は、表情、視線、手、距離、身体の向き、小物の状態変化だけで読める無言演出にする
- HERO LINE: 表示換算20px以上、文字高はページ幅の5.2%以上、ページ内で最も読みやすい
- 文字を収めるための縮小は禁止
- HERO LINEの文字面積と余白を最初に確保する
- 残った面積から吹き出し数とコマ数を自動決定する
- 入らなければ、効果音 → 不要なコマの順に削る
- HERO LINEは英文を変えず、句または節の境界で1〜2吹き出しへ分けてよい
- 説明枠、長文ナレーション、段落、字幕カードは禁止
- 吹き出しは重要な顔、手、小物、視線を隠さない

HERO LINE用吹き出しはページ幅の70%以上を使える決めゴマへ置く。10語を超える場合は、文字領域を先に確保し、必要なら主要な出来事を3場面まで減らす。コマ数を守るために文字を小さくしてはならない。

## 7. ページ設計

上から下、同一段内は左から右。読者が迷わないことを優先する。

- 小さな導入・反応ゴマと、大きな決めゴマに明確な大小差をつける
- 通常、斜め、台形、縦長、横長、重なり、インセット、枠外突破、枠なし、タチキリを内容に応じて使う
- 均等な2×2、全コマ同サイズ、全コマ同じ四角は禁止
- 連続は狭いガター、時間経過や沈黙は広いガターで示す
- 視線、身体の向き、動線、集中線、吹き出しで次のコマへ導く
- ロング、ミドル、アップ、極端な寄り、俯瞰、煽り、肩越し、手元を使い分ける
- 感情は表情だけでなく、距離、手、姿勢、視線、物への接触、余白で示す

構成例は選択肢であり固定テンプレートではない。

- 上の小ゴマで溜め、下半分を決めゴマ
- 中央の大ゴマを小さな反応ゴマで挟む
- 斜めゴマで緊張を高め、静かな横長ゴマへ着地
- 大きな情景ゴマへ表情や手元のインセットを重ねる
- 対立する縦長ゴマから、関係が変わる横長ゴマへ移る
- 枠外突破で登場、決断、感情の突破を見せる

連続する作品で同じレイアウトを使わない。

## 8. 日本漫画の画材表現

- 完成した縦長の日本商業白黒漫画原稿
- Gペン風の入り抜き、黒ベタ、網点、カケアミ、ハッチング、白抜き
- 集中線、スピード線、ベタフラッシュ、描き文字、効果背景、漫符は必要なものだけ
- 相手役の顔、髪、体格、衣装、種族をページ内で統一
- 学習者は匿名の肩越し、後ろ姿、手元、主観視点を使ってよい

禁止: アニメの一枚絵、セル塗り、カラーCG、ポスター、ピンナップ、ビジュアルノベル画面、ゲームカード、資料画像、UI、写実写真。

## 9. 生成前一致検査

最終プロンプトへ進む前に、以下をすべて照合する。

- 相手名、関係、成人外見、時代、場所、世界規則がCAPSULEと一致
- HERO LINEが直前レビューに完全一致
- 別シーンの固有名詞がゼロ
- 現代シーンへ竜、魔法、学園など別世界要素がゼロ
- `yes` / `はい` が画像内文字、物語、描き文字にゼロ
- 会話の発言、出来事、結末の再演がゼロ
- MNEMONIC STORYが物語ゲートの全項目に合格
- 新規text-to-image生成であり、過去画像の編集・継続・参照・再利用ではない
- プロンプト中の人物、場所、HERO LINE、小物がCURRENT CHAT FINGERPRINTと一致
- すべてが具体値であり、プレースホルダー、`same as before`、`previous`、`preserve`参照がゼロ
- ZERO-BASE IMAGE BLUEPRINTが背景から画材まで全文で入り、画像ツールが会話履歴を知らなくても制作できる
- 別シーンの固有語を、否定形や禁止例としても画像プロンプトへ書いていない
- 実際に渡す生の最終プロンプトに、`SCENE:`、`PANEL SCRIPT:`、`PAGE AND LETTERING:`、`NON-NEGOTIABLES:`の4見出しが順番どおり実在
- 引用符で囲まれた画像内文字列は、完全一致のHERO LINE 1つだけ
- タイトル文字、説明枠、ラベル、看板、学習メモ、効果音、HERO LINE以外の台詞を描かせる指示がゼロ
- 完成した生の最終プロンプト全文を、画像ツールの明示的で空でないprompt引数として渡す。promptが未指定、null、空文字、会話文脈からの自動推論になる呼び出しは禁止

不一致ならプロンプトを破棄し、CAPSULEだけから1回再構築する。再検査に失敗したら画像ツールを呼ばない。別シーンへの代替は禁止。

## 10. 最終画像プロンプト

画像ツールには会話履歴、Project、添付ファイル、CAPSULE、MANGA_PAGE_PLAN、過去プロンプト、過去画像のどれも見えない。毎回、初対面の漫画制作担当へ渡す独立した発注書をゼロから書く。次の4ブロックをこの順番で使い、角括弧をすべて具体値へ置換する。テンプレートを要約、言い換え、自由形式化せず、見出しと構造をそのまま保つ。背景、人物、関係、世界規則、新事件、全コマ、台詞、文字サイズ、画材、読後感のどれも省略せず、完成文だけを渡す。この完成文全文を画像ツールの明示的で空でないprompt引数として渡す。promptを未指定、null、空文字にしたり、会話文脈から自動推論させたりしない。画像ツールへ `this`、`current`、`same`、`above`、`previous`、`preserve`、`improved phrase` を渡さない。別シーンの人物・生物・場所・小物・作品名を禁止例としても書かない。

SCENE:
Create one brand-new portrait black-and-white Japanese manga page from text only.
The story takes place in [exact era] at [exact place, architecture, weather, lighting, and three visible background objects].
[exact name] is an adult [age range, face, hair, build, clothing, and species if relevant]. [exact name] is the anonymous learner's [exact relationship]. The learner is shown only as [exact anonymous viewpoint or partial body treatment].
The physical rules of this world are: [complete world rules stated positively].
The one-page story begins when [fully visible new incident]. [exact mnemonic prop] creates pressure by [visible cause]. The climax occurs when [exact name or learner performs exact visible action] and says "[exact HERO LINE]". Immediately afterward, [two or more visible changes in expression, distance, decision, or situation]. The final image beat is [specific humorous, romantic, surprising, relieving, or lingering payoff].

PANEL SCRIPT:
Use [resolved panel count from 3 to 6] panels, read top to bottom and left to right within a tier.
Panel 1: [panel shape and page share]; [shot and angle]; [exact character placement, gaze, hands, prop interaction, background, and silent hook].
Panel 2: [panel shape and page share]; [shot and angle]; [exact action that increases pressure, acting, gaze, and prop movement]; no text.
[Continue one complete sentence for every remaining setup or reaction panel.]
HERO PANEL: [largest panel shape, location, and 35–50% page share]; [shot and angle]; [exact body action, hand position, gaze, distance, prop, effect, and visible reversal]. Place one broad balloon with the exact text "[exact HERO LINE]".
FINAL PANEL: [shape and location]; [specific silent reaction or payoff, camera, gesture, and prop state]; no text.

PAGE AND LETTERING:
Make a finished sequential Japanese commercial manga manuscript, not a standalone illustration. Use varied panel geometry, one dominant HERO PANEL, clear gutters, expressive tapered G-pen lines, solid blacks, dot screentones, kakeami, controlled hatching, white knockout, and crisp print contrast.
The full portrait page must remain readable at 390 px smartphone width. Make the quoted HERO LINE the page's unmistakable visual and emotional focus. Draw it once, unchanged, in one or at most two broad balloons inside the HERO PANEL. Its smallest letter height must be at least 5.2% of page width, visually equivalent to at least 20 px at 390 px display width. Reserve balloon space first and remove a panel if necessary; never shrink the letters. Every other panel must communicate incident, pressure, reversal, and payoff without words, using facial acting, gaze, hands, body distance, staging, and changes to the mnemonic prop.

NON-NEGOTIABLES:
The page contains exactly the described era, place, world, [exact name], anonymous learner treatment, incident, and mnemonic prop. Every panel follows the PANEL SCRIPT. The only letters anywhere on the page are the exact quoted HERO LINE. All other panels are silent and communicate by pictures alone; they contain no captions, signs, labels, numerals, or written sound effects. Use monochrome ink and screentone only. Use an unequal manga layout with one dominant HERO PANEL.
This prompt is the complete production brief. Infer no facts from any conversation, file, previous request, prior image, or unstated context.

## 11. 学習アンカーと出力後

学習上の正本は、レビューで一度だけ表示したHERO LINEと自然な日本語訳。肯定後は非表示のMNEMONIC STORY、MANGA_PAGE_PLAN、最終画像プロンプトを作り、同じ英文や和訳をテキストで再掲せずに画像ツールを呼ぶ。画像ではHERO LINEだけを大きく際立たせ、画像の後にも英文全文や和訳を表示しない。

画像ツールの戻り値の生成タイトルと画像内容をCURRENT CHAT CAPSULEへ照合する。別の人物、場所、小物、種族、世界規則、過去画像タイトルがあれば、古い生成コンテキストの混入として不合格。参照を一切持たない新規text-to-image生成をCAPSULEだけから1回やり直す。再生成も不一致なら停止して短く報告する。

## 12. 不合格条件

- 現在シーン以外の人物、世界、小物が一つでもある
- 生成タイトルまたは画像が過去シーンを示す
- 過去画像、画像ID、過去プロンプト、Projectメモリを参照・再利用している
- HERO LINEがレビューと違う
- 390px全体表示で拡大しないと読めない
- 5秒で問題と変化を説明できない
- HERO LINEによる目に見える反転がない
- 感情的な報酬または記憶フックがない
- 会話の再演、あらすじ、説明漫画、均等グリッド
- 会話にはなかった記憶用の新事件がない
- 先に面白いMNEMONIC STORYを確定せず、レイアウトから作っている
- HERO LINEが物語の原因ではなく、後付けの字幕や飾り台詞になっている
- 教材要素を外すと物語として読めない
- レビュー前または肯定前に生成
- レビューに正確なHERO LINEと自然な日本語訳が一度だけ表示されていない

生成後の不合格を自動で別シーンに差し替えない。原因を現在シーンのLOCKに照らして報告する。

## 13. 参考

- 小学館 新人コミック大賞「まんが家養成講座」: https://shincomi.shogakukan.co.jp/training/
- CLIP STUDIO TIPS「Paneling Comics and Webtoons」: https://tips.clip-studio.com/en-us/articles/9422
- MediBang Paint「Manga Frame Layout for Beginners」: https://medibangpaint.com/en/use/2022/10/how-to-draw-frame-split/
- OpenAI「Image generation prompting guide」: https://developers.openai.com/cookbook/examples/multimodal/image-gen-models-prompting-guide
