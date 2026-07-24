# 没入型英会話 — Immersive English Scenes

このProjectは、英会話の実践を「会話の相手役」を通じて続けるためのライブラリです。

- 320基本シーン／1,280バリエーション
- 通常3択は実務・現実系・現代ドラマ系・非日常・発想系の3枠を必ず1枠ずつ選出
- 相手役は成人女性を中心に、1ターン1問いで会話を進行
- 会話終了後は辛口レビュー→「📌 次回への引き継ぎ」（5軸）を出力
- 2回目以降、保存データがある場合はメニュー前に最大2行だけ表示
- 学習記録は自然終了＋6発話以上後に反映。課題昇格は直近3回中2回観測で有効化

## インストール（公開配布）

配布用ZIP: [`immersive-english-scenes.zip`](immersive-english-scenes.zip)

### 手順

1. `immersive-english-scenes.zip` を展開。
2. `UPLOAD_THESE_6_FILES` 内の次の6ファイルをProject sourcesへ追加:
   - `IES_v9_00_START_HERE.md`
   - `IES_v9_01_SCENE_CATALOG.xlsx`
   - `IES_v9_02_SCENE_CARDS.md`
   - `IES_v9_03_TUTOR_RULES.md`
   - `IES_v9_04_DESIGN_RATIONALE.md`
   - `IES_v9_05_MANGA_PROMPT_BIBLE.md`
3. Project settings の instructions に `PROJECT_INSTRUCTIONS.txt` の全文を貼る。このファイルはProject sourcesへアップロードするファイルではありません。
4. 初回チャットで短い挨拶または希望を送ると3択が出ます。

### 運用要点

- 2回目以降で保存データがある場合、3択前に最大2行表示:
  - 覚えていること
  - 今回の選定
- 引き継ぎ反映は3択中**1枠のみ**。残り2枠は新奇性／多様性優先で弱点偏重しない
- 利用者の明示訂正は推定値より優先。推定更新は自然終了後で6発話以上蓄積時のみ反映
- 明示的な終了コマンドは不要。自然な終了を検知するとレビューへ移行
- 会話終了後は、相手役の締め→辛口レビュー→引き継ぎ→漫画確認までをテキストだけで出す。次の明確な「はい／yes」の後にだけ画像を生成する。
- 肯定後は追加確認をせず、`IES_v9_05_MANGA_PROMPT_BIBLE.md` に従って内部ページ設計を作り、画像ツールを呼ぶ。

## 漫画ルール（日本語漫画表現）

- 3〜6コマの縦長1ページ。英語教材のため、上から下、同一段内は左から右。
- 全コマ同じ大きさの四角形や均等な2×2グリッドを禁止し、見せ場の決めゴマを明確に大きくする。
- 通常、斜め、縦長、横長、重なり、インセット、枠外突破、枠なし、タチキリを場面の意味に応じて選ぶ。
- レビューで示した模範英文を決め台詞にし、その一言で相手の表情・距離・判断・状況が変わる短編へ再構成する。会話の羅列にはしない。
- Gペン風の線、黒ベタ、網点、カケアミ、白抜きを使う白黒漫画原稿。アニメの一枚絵、カラー、セル塗り、ポスター、ビジュアルノベルCGは除外。
- 相手役は同じ成人女性として固定。学習者は必要な場合だけ、匿名の肩越し・後ろ姿・手元・主観視点で描く。

## 検証について

- `PROJECT_INSTRUCTIONS.txt` と6ファイルの一致、`immersive-english-scenes.zip` の同梱、静的契約項目は verification で確認できます。
- 画像生成の同ターン試行自体は verification で契約テキストとフォールバック有無を検証できますが、実際に表示された画像が出たかどうかはライブE2E実行でのみ PASS です。
- 指示文字数はUI上限（実機検証時点）を超えない範囲で管理しています（実装上の目安）。

## 公式ヘルプ

- [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-using-projects-in-chatgpt)
- [File Uploads FAQ](https://help.openai.com/en/articles/8555545-file-uploads-with-chatgpt-plus)
