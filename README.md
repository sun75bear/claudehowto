# はじめての Claude（紹介サイト）

Claude の契約から実務での使い方までを紹介する静的サイトです。Markdown で書き、MkDocs Material でビルドして GitHub Pages に公開します。

公開URL: （リポジトリ作成後にここへ記入）

## 仕組み

```
docs/*.md ──(編集)──▶ git push ──▶ GitHub Actions が mkdocs build ──▶ GitHub Pages で公開
```

`main` に push すると自動でビルド・公開されます。反映まで1〜2分。

## ローカルで書く

初回のみ:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

`Activate.ps1` が実行ポリシーで弾かれる場合は、先に次を実行:

```powershell
Set-ExecutionPolicy -Scope Process RemoteSigned
```

2回目以降:

```powershell
.\.venv\Scripts\Activate.ps1
mkdocs serve          # http://127.0.0.1:8000 を開く。保存すると自動で再読み込み
```

公開:

```powershell
git add .
git commit -m "変更内容"
git push
```

## ファイル構成

| パス | 役割 |
|---|---|
| `mkdocs.yml` | サイト設定・章立て（`nav`）。章を増やしたらここに追記 |
| `docs/*.md` | 本文。ファイル名は ASCII、表示名は `nav` で日本語指定 |
| `docs/assets/img/` | スクリーンショット置き場 |
| `requirements.txt` | mkdocs-material のバージョン固定 |
| `.github/workflows/deploy.yml` | 自動ビルド・公開 |

## 公開までの初回セットアップ

1. `mkdocs.yml` の `site_url` / `repo_url` の `<USER>` `<REPO>` を実際の名前に置き換える
2. GitHub でパブリックリポジトリを作成し、push する
3. **リポジトリの Settings → Pages → Build and deployment → Source を「GitHub Actions」に変更する**
   （ここを変更しないと Actions は成功しても 404 になります）
4. Actions タブでワークフローが成功したら、公開URLを開いて確認

## スクリーンショットについて

本文中に `<!-- TODO(画像): ... -->` の形でプレースホルダを置いてあります。Claude.ai にログインした状態で撮影し、`docs/assets/img/` に指定のファイル名で保存したうえで、コメントを `![説明](assets/img/xxx.png)` に置き換えてください。

## メモ

- ビルドは `mkdocs build --strict` で実行しており、リンク切れがあると失敗します
- 料金・手順は 2026年8月時点の情報です。本文の `!!! note` に日付を明記しています
- 将来 S3 に移す場合は `mkdocs build` が生成する `site/` をそのまま同期すれば動きます
