# 用語集とリンク集

## 用語集

**Claude Code**
: パソコンの中のファイルを直接読み書きし、コマンドまで実行できる Claude。このサイトの主題。Pro プラン以上が必要。

**Claude / Anthropic**
: Claude は Anthropic 社が提供する AI サービス。Anthropic はアメリカの企業。

**エージェント型**
: 一度の指示で、計画を立てて複数の手順を自分で進める働き方。Claude Code の性質。

**セッション**
: Claude との1つの作業のまとまり。それぞれ独立した文脈を持ち、同時に複数開ける。

**権限モード**
: Claude Code がどこまで自分の判断で実行してよいかの設定。Manual / Plan / Accept edits / Auto の4種。

**Plan モード**
: ファイルを変更せず、方針の提案だけをさせるモード。大きな作業の前に使う。

**差分ビュー（diff）**
: 変更前と変更後の違いを表示する画面。緑が追加、赤が削除。承認前に必ず読む。

**`CLAUDE.md`**
: 作業フォルダに置いておくと、Claude Code が毎回読んでくれる指示書。毎回の説明を省ける。

**スキル**
: 繰り返す作業を手順として登録し、`/` から呼び出せるようにしたもの。チームで共有できる。

**スラッシュコマンド**
: `/help` `/clear` `/init` のように `/` で始まる特別なコマンド。

**MCP / コネクタ**
: Claude Code を手元のファイル以外（Google Drive、Slack、GitHub など）につなぐ仕組み。

**サブエージェント**
: 大きな作業を分担させるために、Claude Code が内部で動かす別の Claude。

**使用量クレジット**
: プランの上限に達したあと、従量課金で使い続けるための仕組み。

**5時間セッション上限 / 週次上限**
: Claude の使用量の枠。2段構えになっており、チャットと Claude Code で合算される。

**ハルシネーション**
: AI が事実でないことをもっともらしく答えてしまう現象。

**コンテキスト**
: Claude が今の作業で抱えている情報のまとまり。増えすぎると精度が落ちるので `/clear` する。

**ターミナル / PowerShell**
: 文字でコマンドを打ってパソコンを操作する画面。デスクトップアプリを使うなら不要。

**Git**
: ファイルの変更履歴を管理する仕組み。Windows で Claude Code のローカル作業をするには必要。

## リンク集

### まず見るもの

- [Claude を使う（claude.ai）](https://claude.ai)
- [料金プラン](https://claude.com/pricing)
- [デスクトップアプリのダウンロード](https://claude.com/download)

### Claude Code

- [公式ドキュメント（概要）](https://code.claude.com/docs/en/overview)
- [デスクトップアプリのクイックスタート](https://code.claude.com/docs/en/desktop-quickstart)
- [ターミナル版のセットアップ](https://code.claude.com/docs/en/setup)
- [よくあるワークフロー](https://code.claude.com/docs/en/common-workflows)
- [ベストプラクティス](https://code.claude.com/docs/en/best-practices)
- [MCP のクイックスタート](https://code.claude.com/docs/en/mcp-quickstart)
- [インストールのトラブルシュート](https://code.claude.com/docs/en/troubleshoot-install)

### サポート

- [ヘルプセンター](https://support.claude.com)
- [使用量と上限について](https://support.claude.com/en/articles/11647753-how-do-usage-and-length-limits-work)

!!! tip "英語のドキュメントを読むとき"
    URL を Claude に貼り付けて「このページを日本語で要約して」と頼めば、そのまま読めます。英語であることは障害になりません。
