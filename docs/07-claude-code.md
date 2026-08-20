# 7. Claude Code へ進む

!!! abstract "このページでできるようになること"
    Claude Code が何なのかを理解し、自分のパソコンに入れて動かせるようになります。

## ここから先は「興味のある人だけ」

[6章](06-cautions.md) までで、Claude.ai を日常的に使うための説明は終わっています。ここから先は**もう一段踏み込みたい人向け**です。

## Claude Code とは

Claude.ai は、こちらが貼り付けたものだけを見て答えます。**Claude Code は、パソコンの中のファイルを Claude が自分で開いて、読んで、書き換えます。**

| | Claude.ai | Claude Code |
|---|---|---|
| ファイル | こちらが1つずつ添付する | フォルダごと渡して自分で探す |
| 変更 | 結果をコピペして自分で反映 | ファイルを直接書き換える |
| 実行 | できない | コマンドを実行して結果を確認できる |

「このフォルダの資料を全部読んで一覧表を作って」「このプログラムのバグを直して」といった、**複数のファイルにまたがる作業**が任せられるようになります。

もともとはプログラマー向けの道具ですが、大量のテキストファイルやデータの整理にも使えます。

!!! danger "Pro プランが必須です"
    **無料プランでは Claude Code は使えません。** [2章](02-signup.md) を参照して Pro に上げてから進んでください。

## 2つの使い方：どちらを選ぶか

=== "デスクトップアプリ（推奨）"

    **ターミナル（黒い画面）を使いたくない人はこちら。**

    普通のアプリと同じように、画面上のボタンとチャットで操作できます。

    1. [claude.com/download](https://claude.com/download) からインストーラーを入手
    2. インストールして起動
    3. Claude アカウントでログイン
    4. 作業したいフォルダを開いて、チャット欄に指示を書く

    やれることはほぼ同じなので、**まずはこちらで試すことをおすすめします。**

=== "ターミナル版"

    コマンド操作に抵抗がない人向け。動作が軽く、細かい制御ができます。

    以下の手順で入れます。

## ターミナル版のインストール

### Windows の場合

1. スタートメニューで「PowerShell」と検索し、**Windows PowerShell** を開きます（管理者権限は不要です）
2. 次の1行を貼り付けて `Enter`

    ```powershell
    irm https://claude.ai/install.ps1 | iex
    ```

3. インストールが終わったら、**PowerShell をいったん閉じて開き直します**（これをしないと次のコマンドが見つかりません）
4. 動作確認

    ```powershell
    claude --version
    ```

    `2.1.211 (Claude Code)` のようにバージョン番号が出れば成功です。

!!! tip "Git for Windows も入れておくと良い"
    必須ではありませんが、[Git for Windows](https://git-scm.com/downloads/win) を入れておくと Claude Code が使えるコマンドが増えます。あとから入れても構いません。

### Mac の場合

1. 「ターミナル」アプリを開きます（`command + space` で「ターミナル」と検索）
2. 次の1行を貼り付けて `Enter`

    ```bash
    curl -fsSL https://claude.ai/install.sh | bash
    ```

3. ターミナルを開き直して、動作確認

    ```bash
    claude --version
    ```

## 初回の起動とログイン

1. 作業したいフォルダに移動します

    === "Windows"

        ```powershell
        cd C:\work\myfolder
        ```

    === "Mac"

        ```bash
        cd ~/work/myfolder
        ```

2. 起動します

    ```text
    claude
    ```

3. 初回はブラウザが開くので、Claude アカウントでログインし、表示された指示に従って承認します
4. ターミナルに戻ると、入力待ちの状態になっています。ここに日本語で話しかけられます

<!-- TODO(画像): Claude Code の初回起動画面。docs/assets/img/claude-code-start.png -->

## うまくいかないとき

まず次のコマンドを実行してください。設定やインストール状態を自己診断してくれます。

```text
claude doctor
```

| 症状 | 対処 |
|---|---|
| `claude` は認識されません / command not found | ターミナルを開き直す。それでもダメなら再インストール |
| インストールが途中で失敗する | [公式のトラブルシュート](https://code.claude.com/docs/en/troubleshoot-install) を参照 |
| ログイン画面が開かない | 表示された URL を手動でブラウザに貼り付ける |
| そもそも使えないと言われる | 無料プランのままの可能性。Pro になっているか確認 |

!!! note "2026年8月時点の手順です"
    インストール方法は変わることがあります。最新は [公式のセットアップ手順](https://code.claude.com/docs/en/setup) を確認してください。

[次へ：Claude Code 実践 :material-arrow-right:](08-claude-code-practice.md){ .md-button }
