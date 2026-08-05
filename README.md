# Liner Notes サイト

購入者レビューを読み込んで日用品・消耗品を比較するアフィリエイトサイト。

## デプロイ手順（GitHubアカウント作成後）

1. Rさんが新規GitHubアカウントで `<ユーザー名>.github.io` リポジトリを作成（README初期化つき・Public）
2. Settings → Collaborators で `sea-song-label` を招待
3. Claudeが招待を受諾し、このディレクトリの中身をpush：
   ```
   cd ~/Projects/liner-notes-site
   git init && git add . && git commit -m "初回公開"
   git remote add origin https://github.com/<ユーザー名>/<ユーザー名>.github.io.git
   git branch -M main && git push -u origin main
   ```
4. リポジトリ名が `<ユーザー名>.github.io` ならPagesは自動で有効化される。数分後 `https://<ユーザー名>.github.io/` で公開確認

## 運用ルール（正本：Vault `liner-notes/plan.md` の「方針転換 2026-08-05」節）

- 1記事=1テーマの比較記事。候補は `liner_notes_search.py --all` で週次生成
- 使ったことのない商品の使用感は書かない。「レビューを読み込んだ」スタンスを記事内で明示
- 全ページに【PR】表記とアフィリエイト参加の明示（景表法ステマ規制対応）
- 楽天リンクは `rel="nofollow sponsored"` を付ける
- 価格・レビュー件数には必ず取得日を添える
- 新記事追加時は `index.html` の記事一覧にも忘れず追記
