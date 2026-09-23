キャッシュフロー診断 v1.6.0 / 借入評価テスト版

今回の変更
- 奨学金・自動車ローン・カードローン／リボ・その他ローン・住宅ローンを分けて入力
- 借入がある場合だけ、残高と月額返済の入力欄を表示
- 金融資産の評価（①〜④）と「借入・返済コンディション」を分離
- 奨学金があるだけで若い方の総合点が下がらない設計
- カードローン／リボや返済負担が大きい場合は、借入欄で注意表示
- 住宅ローンは住宅資産との対応があるため、金融資産から差し引かず参考表示

試す前に必要な作業
1. Google Apps Scriptを開く
2. 既存のCode.gsを、このフォルダの gas/Code.gs の内容ですべて置き換えて保存
3. 「デプロイ」→「デプロイを管理」→鉛筆アイコン
4. バージョンを「新バージョン」にしてデプロイ
   ※既存の /exec URL はそのまま使えます
5. GitHubリポジトリ直下の index.html を、このフォルダの index.html に置き換える
6. GitHub Pagesの反映後、架空データで診断
7. スプレッドシート responses に1行追加されたことを確認

設定済み
- スプレッドシートID: 1tqN5fkAs86iEJ_CiqxGDwdp-0-dbOobxuVB1Ui55OpM
- シート名: responses
- テスト用トークン: test
- HTML送信先: https://script.google.com/macros/s/AKfycbwgldxZN5HQGHp9OvU6UhV6LGcqPKeolzozX7hDAQBay35HA3PMcJQOOgMji5bupyaK/exec

本番前に必須
- 同意画面の「会社名をここに」「問い合わせ先メール／電話をここに」を正式情報へ置換
- TOKEN=testを30文字以上のランダム文字列へ変更し、HTML側とGAS側を一致
- GitHub Pagesは公開ページのため、確認後は自社サーバーのアクセス制限付き領域へ移行