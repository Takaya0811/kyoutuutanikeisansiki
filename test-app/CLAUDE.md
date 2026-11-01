# test-app

@~/core/product-rules.md
@~/core/foyer-caller.md

## このプロダクトについて
<!-- 使わない項目は消す。長い説明は docs/ に置き、ここには場所だけ書く -->
- 作るもの：foyer の試運転用のページ。door に頼んで作った画像を index.html に並べる
- 使う技術：HTML 1枚（index.html）。ビルドやテストのコマンドはない
- 主なフォルダ：`images/` は画像、`reports/` は資料（HTML）
- door から受け取った物の置き場所：画像は `images/` に置き、index.html の gallery に <img> で並べる

## Gotchas
<!-- 共通メモの「Gotcha」の書き方に従う。最初は空でよい -->
- **door のフォルダが未信頼だと、door の settings.json の許可が効かず、画像が0枚で返る**
  `status: ok` でも、door 内の Write や Bash が承認待ちで止まる。`permissionDenials` が空でなければ、人がその door のフォルダを Claude Code で直接開いて信頼を通してから頼み直す。
