キャッシュフロー診断 v1.5.0 / GitHub Pages確認用

設定済み
- スプレッドシートID: 1tqN5fkAs86iEJ_CiqxGDwdp-0-dbOobxuVB1Ui55OpM
- シート名: responses
- テスト用トークン: test
- HTML送信先: https://script.google.com/macros/s/AKfycbwgldxZN5HQGHp9OvU6UhV6LGcqPKeolzozX7hDAQBay35HA3PMcJQOOgMji5bupyaK/exec

接続確認済み
- /exec URLはログインなしで到達可能
- GET応答: {"ok":true,"msg":"endpoint alive"}
- POST保存テスト成功。responsesシートへ staff=CODEX_TEST / source=github-preflight の行を1件追加済み

GitHub Pagesでの確認手順
1. GitHubリポジトリ直下の index.html を、このindex.htmlへ置き換える
2. 反映まで1〜3分待つ
3. GitHub PagesのURLを開き、架空データで診断を完了する
4. スプレッドシートの responses シートへ1行追加されたことを確認する

GASコードについて
- gas/Code.gsにはスプレッドシートIDとTOKEN=testを設定済みです
- 現在の/execデプロイで正常応答しているため、GitHubテストだけなら再デプロイは不要です
- Code.gsを変更した場合のみ、新バージョンとして再デプロイしてください

未確定・本番前に必須
- index.htmlの同意画面に「会社名をここに」「問い合わせ先メール／電話をここに」が残っています。
  実在のお客様が使う前に必ず正式情報へ置換してください。
- TOKEN=testは検証専用です。本番時は30文字以上のランダム文字列へ変更し、
  GAS側とindex.html側を同じ値にした後、GASを再デプロイしてください。
- GitHub Pagesは公開ページです。今回の確認後は自社サーバーのアクセス制限付き領域へ移してください。