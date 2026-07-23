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
2. 次の5ファイルをProjectへ追加:
   - `PROJECT_INSTRUCTIONS.txt`
   - `UPLOAD_THESE_5_FILES/IES_v8_00_START_HERE.md`
   - `UPLOAD_THESE_5_FILES/IES_v8_01_SCENE_CATALOG.xlsx`
   - `UPLOAD_THESE_5_FILES/IES_v8_02_SCENE_CARDS.md`
   - `UPLOAD_THESE_5_FILES/IES_v8_03_TUTOR_RULES.md`
   - `UPLOAD_THESE_5_FILES/IES_v8_04_DESIGN_RATIONALE.md`
3. Project settings の instructions に `PROJECT_INSTRUCTIONS.txt` を貼る。
4. 初回チャットで短い挨拶または希望を送ると3択が出ます。

### 運用要点

- 2回目以降で保存データがある場合、3択前に最大2行表示:
  - 覚えていること
  - 今回の選定
- 引き継ぎ反映は3択中**1枠のみ**。残り2枠は新奇性／多様性優先で弱点偏重しない
- 利用者の明示訂正は推定値より優先。推定更新は自然終了後で6発話以上蓄積時のみ反映
- 明示的な終了コマンドは不要。自然な終了を検知するとレビューへ移行
- レビュー→引き継ぎ→漫画は同一ターン継続トランザクション。引き継ぎ後は即時にシーン固有プロンプトを使って1枚の漫画生成を試行し、画像出力が見えるまで完了しない。
- 画像生成は「画像ツール引数」を同一ターンでそのまま渡す。引数は `Generate one vertical Japanese manga page based on the completed roleplay.` で始まり、COUNTERPART/SETTING/TURNING POINT/PANEL/ENGLISH BUBBLES/PAGE LAYOUT/STYLE/DO NOT を scene value で埋める。

## 漫画ルール（日本語漫画表現）

- 対象は成人女性1人を固定。学習者本人は描画対象外。
- 漫画は日本語漫画文法（非対称/リズム変化のコマ配置、隣接コマで順次モーション）で描写。
- 同一コマ構図・同一構図反復を避け、静止画連結ではなく連続動作を見せる。
- 写真風／シネマチック／webtoon／モバイルガチャ風／静止画ポートレート再利用／3Dは除外。

## 検証について

- `PROJECT_INSTRUCTIONS.txt` と5ファイルの一致、`immersive-english-scenes.zip` の同梱、静的契約項目は verification で確認できます。
- 画像生成の同ターン試行自体は verification で契約テキストとフォールバック有無を検証できますが、実際に表示された画像が出たかどうかはライブE2E実行でのみ PASS です。
- 指示文字数はUI上限（実機検証時点）を超えない範囲で管理しています（実装上の目安）。

## 公式ヘルプ

- [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-using-projects-in-chatgpt)
- [File Uploads FAQ](https://help.openai.com/en/articles/8555545-file-uploads-with-chatgpt-plus)
