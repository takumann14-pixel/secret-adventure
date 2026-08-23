# デザイン 10パターン 2026-08-23

対象記事：**AIが書いた文章、なぜ「読む気が失せる」のか——8つの症状と、私が全部潰した置換ルール**

- note表紙：1280×670px（1.91:1）
- X告知：1200×675px（16:9）
- 共通トーン：本文が「AI臭を消す＝人間に戻す」なので、**無機質 → 人肌**の対比を全案の軸にする

---

### パターン1：大文字タイポ×余白（ミニマル）／note表紙
- コンセプト：文字だけで殴る。装飾ゼロが記事の主張と一致
- レイアウト：左寄せ、上下に大きく余白。メインコピーを2行組みで左上3分の1に配置
- 配色：`#FAFAF8`（紙白）／`#1A1A1A`（墨）
- メインコピー：**その文章、誰もいない**
- サブコピー：AIっぽさを消す8つの置換ルール
- 生成プロンプト：`Minimal Japanese editorial cover, off-white paper background, vast negative space, no illustration, subtle paper grain texture, 1280x670`

### パターン2：ビフォーアフター対比／note表紙
- コンセプト：記事の中身（Before/After置換表）をそのまま表紙にする
- レイアウト：中央縦線で二分割。左=グレーの平坦な文字組、右=黒の太い手書き寄り
- 配色：`#9CA3AF`（左・無機質）／`#111827`（右）／`#FFD93D`（矢印）
- メインコピー：**「〜ではないでしょうか」→「〜だ」**
- 生成プロンプト：`Split-screen before/after typographic layout, left side flat gray sterile text block, right side bold black confident text, yellow arrow between, editorial minimal, 1280x670`

### パターン3：数字訴求／note表紙 ★推奨
- コンセプト：「17回」という実体験の数字を主役に
- レイアウト：中央に極大数字。その下に細く説明文
- 配色：`#0F0E17`（背景）／`#FFFFFF`／`#FF6B6B`（数字）
- メインコピー：**4,000字に17回**
- サブコピー：私の原稿からAIが顔を出していた回数
- 生成プロンプト：`Dark editorial poster, giant red numeral as focal point, thin white Japanese sans-serif caption below, high contrast, minimal, 1280x670`

### パターン4：手書き風・親近感／note表紙
- コンセプト：AI臭の対極＝手の跡。赤ペン添削のメタファー
- レイアウト：印字された文章に赤ペンで取り消し線と書き込み
- 配色：`#FFFDF7`（紙）／`#333`（印字）／`#E5484D`（赤ペン）
- メインコピー：**AI原稿、赤入れ実況**
- 生成プロンプト：`Printed Japanese manuscript page with red pen proofreading marks, strikethroughs and handwritten corrections, top-down photo, warm paper, 1280x670`

### パターン5：ダーク×ゴールド（有料感）／note表紙
- コンセプト：300円でも"ちゃんとした商品"に見せる
- レイアウト：中央寄せ、細い金の罫線で囲み
- 配色：`#0F0E17`／`#C9A227`（金）／`#FFFFFF`
- メインコピー：**AI臭を消す技術**
- サブコピー：8症状 × 置換ルール全公開
- 生成プロンプト：`Premium dark editorial cover, deep navy-black, thin gold hairline frame, centered elegant Japanese typography, luxury minimal, 1280x670`

### パターン6：スクショ風UI（実用ノウハウ感）／note表紙
- コンセプト：検索ボックスに「でしょうか」と打った瞬間の画面
- レイアウト：エディタ風UIを中央に、検索ヒット17件のバッジ
- 配色：`#F5F5F7`／`#1A1A1A`／`#FF6B6B`（ヒット数）
- メインコピー：**「でしょうか」 17件**
- 生成プロンプト：`Clean text editor UI mockup, search bar with Japanese query, red match counter badge, soft shadow, flat design, 1280x670`

### パターン7：人肌の写真＋短文／note表紙
- コンセプト：人間に戻す、を文字通り視覚化
- レイアウト：手がキーボードから離れて紙にペンを取る瞬間、下部に白帯コピー
- 配色：写真＋`#FFFFFF`帯／`#1A1A1A`
- メインコピー：**書き手を、戻す**
- 生成プロンプト：`Hands moving from keyboard to paper notebook with pen, warm natural window light, shallow depth of field, muted tones, 1280x670`

### パターン8：チェックリスト見せ（中身が透ける）／note表紙
- コンセプト：有料パートのチェックリストを一部ぼかして見せる＝購買動機
- レイアウト：8項目のチェックリスト、上3つ鮮明・下5つブラー
- 配色：`#FAFAF8`／`#1A1A1A`／`#4ADE80`（チェック）
- メインコピー：**推敲チェックリスト8項目**
- 生成プロンプト：`Checklist card design, first three items crisp, remaining blurred out, green check marks, clean minimal Japanese UI, 1280x670`

### パターン9：疑問形フック／X告知用
- コンセプト：タイムラインで指を止める挑発
- レイアウト：全面ベタ塗り＋中央に大きな問い
- 配色：`#FFD93D`（地）／`#0F0E17`（文字）
- メインコピー：**まだ「いかがでしたか」で締めてる？**
- 生成プロンプト：`Bold yellow flat background, large black Japanese question text centered, high contrast social media graphic, 1200x675`

### パターン10：シリーズ用テンプレ（使い回し枠）／note表紙
- コンセプト：今後の連載で毎回使える固定フレーム。左に通し番号、右に可変タイトル
- レイアウト：左25%に濃色帯＋`#01`、右75%に白地＋タイトル。**次回以降は数字とタイトルだけ差し替え**
- 配色：`#0F0E17`（左帯）／`#FAFAF8`（右）／`#FFD93D`（番号）
- メインコピー：**#01 AI臭を消す**
- サブコピー：AIと書く技術シリーズ
- 生成プロンプト：`Editorial series cover template, left dark vertical band with large yellow issue number, right white area for Japanese title, reusable layout system, 1280x670`

---

## 使い分けの推奨

| 用途 | 採用案 | 理由 |
|------|--------|------|
| **note表紙（本命）** | パターン3 | 実体験の数字が一番強い。3秒で主題が伝わる |
| note表紙（代替） | パターン2 | 記事の中身そのものが表紙になり、内容が即伝わる |
| X告知メイン | パターン9 | ベタ塗り＋問いはタイムラインで止まりやすい |
| X告知サブ | パターン6・8 | 実用感と「中身が透ける」で保存されやすい |
| 今後の連載 | パターン10 | 2本目以降は制作コストがほぼゼロになる |

カンプ（SVG見本）：`covers/cover3.svg`、`covers/cover10.svg` を同梱。
