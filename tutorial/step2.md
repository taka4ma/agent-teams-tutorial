# STEP 2 環境を準備する

## この章で学ぶこと

STEP 1では Agent Teams が何者かを理解しました。次は実際に動かすための準備をします。

**この章では、Claude Code のインストールから Agent Teams の有効化まで、手を動かして環境を整えます。** この章の手順を終えると、ターミナルで `claude` と入力して Claude Code が起動し、Agent Teams が使える状態になります。

---

## 必要なもの

作業を始める前に、以下が揃っているか確認します。

**Claude Code を利用できるアカウント**が必要です。Claude Code は Claude Pro、Max、Team、Enterprise、または Anthropic Console アカウントで利用できます。無料の Claude.ai プランでは Claude Code は利用できません。

**ターミナル**は macOS や Linux のターミナル、Windows であれば WSL2 上のターミナルが使えます。

---

## Claude Code をインストールする

このチュートリアルでは Native Install を使います。macOS・Linux・WSL では以下のコマンドを実行します。

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Native Install ではバックグラウンドで自動更新されるため、常に最新版を使い続けられます。

インストールが完了したら、バージョンを確認します。

```bash
claude --version
```

Agent Teams を使うには Claude Code v2.1.32 以降が必要です。表示されたバージョンが `2.1.32` 以上であることを確認してください。

---

## Claude Code にログインする

インストールできたら、Claude のアカウントに接続します。

```bash
claude
```

初回起動時にはブラウザが開き、Claude のアカウントでの認証を求められます。ログインして認証を完了すると、ターミナルの Claude Code セッションが使えるようになります。

認証が完了すると、ターミナルに Claude Code の入力プロンプトが表示されます。`/exit` と入力すれば終了できます。

---

## Agent Teams を有効化する

Agent Teams は現時点では実験的機能であり、デフォルトでは無効になっています。使うためには環境変数で明示的に有効化する必要があります。

有効化する方法は2つあります。

**方法1：シェルで環境変数を設定する**

現在のシェルセッションだけで有効化したい場合は、次のようにします。

```bash
export CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1
```

**方法2：Claude Code の設定ファイルに書く**

`~/.claude/settings.json`（ユーザー全体に適用）やプロジェクト内の `.claude/settings.json`（そのプロジェクトだけに適用）に `env` フィールドとして書いておくこともできます。

```json
{
  "env": {
    "CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS": "1"
  }
}
```

このチュートリアルでは環境変数への設定（方法1）を使います。永続化したい場合や特定のプロジェクトだけで使いたい場合は方法2を使うと便利です。

## 次のステップ

環境が整いました。次は Agent Teams を実際に動かします。

STEP 3では、用意したサンプルコードを「可読性」「パフォーマンス」「セキュリティ」の3つの観点から並列にレビューさせるハンズオンをやります。

[STEP 3に進む →](./step3.md)
