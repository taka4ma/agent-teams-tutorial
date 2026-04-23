# Claude Code Agent Teams チュートリアル

このリポジトリは、Claude Code の実験的機能である **Agent Teams** を使って、複数の観点から並列にコードレビューを行うためのチュートリアルです。

Agent Teams は、複数の Claude Code インスタンスをチームとして動かす仕組みです。1 つのコードを「可読性」「パフォーマンス」「セキュリティ」などの観点に分けてレビューさせることで、単一のセッションでは見落としやすい視点を補うことを目指します。

## 想定読者

LLM や AI ツールを触ったことはあるが、Claude Code や Agent Teams には詳しくないエンジニアを想定しています。

Claude Code の基本操作に慣れていなくても進められるように、インストール、Agent Teams の有効化、ハンズオン、プロンプト改善までを順番に扱います。

## ゴール

このチュートリアルのゴールは、読者が Agent Teams を使って、1 つのコードに対して複数の観点から並列にコードレビューを実行できるようになることです。

## 必要なもの

- Claude アカウント
- Claude Code v2.1.32 以降
- macOS、Linux、または Windows WSL2 上のターミナル
- Agent Teams を有効化する環境変数 `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`

Agent Teams は現時点では実験的機能です。セッション再開、タスク状態の反映、チーム終了処理などに制限があります。重要な作業に組み込む前に、小さなハンズオンで挙動を確認してください。

## 進め方

| STEP | タイトル | 内容 |
|------|---------|------|
| 1 | [Agent Teams とは何か](./tutorial/step1.md) | Agent Teams の仕組み、subagents との違い、向き不向きを理解する |
| 2 | [環境を準備する](./tutorial/step2.md) | Claude Code をインストールし、Agent Teams を有効化する |
| 3 | [はじめての Agent Teams：コードレビュー](./tutorial/step3.md) | サンプルコードを複数観点から並列レビューする |
| 4 | [プロンプトを工夫する](./tutorial/step4.md) | 役割定義、出力形式、進行管理の指示を改善する |
| 5 | [振り返りと次のステップ](./tutorial/step5.md) | 学んだことを整理し、自分の業務で使う前の判断軸を確認する |

はじめて読む場合は、STEP 1 から順番に進めてください。
