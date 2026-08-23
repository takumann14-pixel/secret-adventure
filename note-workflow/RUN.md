# RUN — 毎朝の全ステージ実行手順

この環境（Claude Code）が、毎朝この手順を上から順に実行する。
外部LLM APIは不要（この環境のClaude自身が各ステージの実行者）。

## 事前
- 作業日を `DATE = 今日(JST) YYYY-MM-DD` とする。
- `note-workflow/output/{DATE}/` を作成。
- 対象ジャンル：AI活用 × 知的生産／副業（変えたい場合はこの行を書き換える）。

## ステージ実行

1. **01 リサーチ**：`01-research/prompt.md` に従い実行。
   WebSearchでnote人気/急上昇・note公式レポート・X反応を収集 →
   `01-research/scoring.md` でスコア＆耐久フィルタ → `output/{DATE}/01-research.md`。

2. **02 企画**：`02-planning/prompt.md` に従い、01の結果＋`02-planning/history.csv` から
   テーマ10本 → `output/{DATE}/02-themes.md`。1位を採用。

3. **03 執筆**：`03-writing/prompt.md` に従い、採用1本を4,000字＋有料境界設計 →
   `output/{DATE}/03-draft.md`。
   **04に渡す前に必ず字数を実測する**（空白除く本文・有料境界で分割）：
   ```bash
   python3 -c "
   import re,sys
   b=open(sys.argv[1]).read().split('---',2)[2].split('## 検品ログ')[0]
   f,p=b.split('<!-- 💰 有料境界 -->')
   f,p=len(re.sub(r'\s','',f)),len(re.sub(r'\s','',p))
   print('合計',f+p,'/ 無料',f,f'({round(f*100/(f+p))}%)')
   print('字数ゲート:','PASS' if 3600<=f+p<=4400 else 'FAIL')
   print('無料比ゲート:','PASS' if 35<=f*100/(f+p)<=45 else 'FAIL')
   " output/{DATE}/03-draft.md
   ```
   FAILなら**この時点で**増補/圧縮して直す（検品後に直すと二度手間になる）。
   増補は具体例・実体験の追加で行い、一般論の水増しはしない。

4. **04 検品**：`04-qa/prompt.md` に従い、AIっぽさ除去 → `output/{DATE}/04-final.md`。

5. **05 デザイン**：`05-design/prompt.md` に従い、表紙/告知10案 → `output/{DATE}/05-design.md`
   （必要なら `covers/` にSVGカンプ）。

6. **06 営業**：`06-sales/prompt.md` に従い、X告知30本＋予約CSV →
   `output/{DATE}/06-x-posts.md` と `06-x-posts.csv`。

## 仕上げ
- `output/{DATE}/SUMMARY.md` に「今日の1本：タイトル / 採用理由 / 想定score / やることは公開ボタンだけ」を1画面ぶんで書く。
- `git add note-workflow/output/{DATE}` して
  `chore(note): {DATE} の記事パッケージ自動生成` でコミット、指定ブランチにpush。
- 人間がやる残作業（noteに下書き貼付→公開 / X予約CSV取込）だけをSUMMARYに箇条書き。

## 品質ゲート（各ステージ後にセルフチェック）
- 01：通過テーマは耐久フィルタ3項目以上YESか？ スコアは推測だと明記したか？
- 03：本文4,000字±10%か？ 有料境界は"最も欲しい直前"か？ 無料で1個本物を渡したか？
- 04：AIっぽさチェックリスト8項目を通したか？ 文字数±5%以内で保てたか？
- 06：30本すべて切り口が違うか？ 嘘の数字を書いていないか？

どれか落ちたらそのステージだけ再実行してから次へ。
