# haribow-gig-prep

HARIBOWチームメンバー向け「案件に行く前に」プレップページ。公開閲覧サイトだが対象は参加者ではなくチームメンバー。
全体ルール・案件概要は `~/projects/haribow/CLAUDE.md` および `~/projects/haribow/performance/CLAUDE.md`、
本体プロジェクトの決定記録は `~/projects/haribow/performance/member_presence/decisions/` 参照。

## 役割
本番/撮影の前にチームメンバーが目を通す1ページ：
- 立ち振る舞い（アピール・表情・意識の解説動画）
- 写真を撮られるとき・ポージング（立ち方/表情の図解まとめ）
- 振り付け確認（パート別解説動画）

## 技術スタック
- 静的HTML/CSS/JS（フレームワーク無し）、単一ファイル `index.html`
- 動画はすべてYouTube限定公開埋め込み（`haribow.dd@gmail.com`チャンネル。詳細はHARIBOW全体メモリ参照）
- ロゴ画像は `haribow-audition-second-site` のGitHub Pages URLを直接参照（1ソース、複製しない）

## 動画の追加・更新
アップロードは `~/projects/haribow/performance/member_presence/youtube_upload.py` を使う。
新しい動画を追加したら `index.html` の該当セクションにカード（`data-youtubeid`）を追記し、
`performance/member_presence/decisions/` に決定記録を残す。

## リポジトリ
- GitHub: `JunyaUnityDev/haribow-gig-prep`
- `main` ブランチ運用
- GitHub Pages: `main` ブランチ `/`（ルート）から配信
