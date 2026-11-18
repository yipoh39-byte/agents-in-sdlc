---
title: "レッスン 12 - GitHub Pages でサイトをデプロイする"
description: "GitHub Copilot app を使って Pages ワークフローを構成し、そのプル リクエストをレビューして、公開された Space Quiz を確認します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

GitHub Pages でデプロイして、Space Quiz を一般公開しましょう。Copilot はワークフローを準備し、デプロイを案内できますが、変更をレビューしてサイトが公開されたことを確認するのはユーザーの責任です。

このレッスンでは、次の操作を行います。

- Copilot に GitHub Pages のデプロイを構成するよう依頼します。
- マージする前にワークフローとプル リクエストをレビューします。
- デプロイを確認し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、誰でも簡単に試せる方法が必要です。単一ファイルのサイトを GitHub Pages で公開すれば、サーバーやランタイム依存関係を追加せずに、公開 URL からアクセスできるようになります。

## Copilot にデプロイを準備してもらう

> [!WARNING]
> プル リクエストを作成すると、コードがコミットおよびプッシュされることがあります。このプロンプトを送る前に、承認設定と送信先のリポジトリを確認してください。**Approve all** が選択されている場合、別の確認プロンプトは表示されません。

`space-quiz` の Copilot app セッションで、次のプロンプトを送信します。

```plaintext
Prepare a GitHub Pages deployment for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages after changes reach the default branch. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and report its link and any required Pages settings or permissions. Do not merge, enable auto-merge, change Pages settings, or deploy. Stop and wait for my review.
```

## ワークフローとプル リクエストをレビューする

1. リポジトリに README がまだない場合に限り、追加されていることを確認します。
2. ワークフローのビルドおよびデプロイ手順、トリガー、権限など、プル リクエストの変更をレビューします。
3. ワークフローが未マージのプル リクエストではなく、既定のブランチからデプロイすることを確認します。
4. 必要な修正を依頼して、更新された差分をレビューします。マージを許可する前に、必須のプル リクエスト チェックがすべて成功するまで待ちます。

## マージとデプロイを許可する

> [!WARNING]
> 次のプロンプトは、レビュー済みのプル リクエストのマージ、リポジトリの Pages 設定の変更、サイトの公開をエージェントに許可します。レビューを完了し、リポジトリとプル リクエストを確認してから送信してください。承認設定によっては、追加の確認なしでこれらの操作が実行されることがあります。

`<PR_NUMBER>` をレビューしたプル リクエストの番号に置き換え、次のプロンプトを別途送信します。

```plaintext
I have reviewed pull request <PR_NUMBER> in this repository and authorize its merge and deployment. Enable GitHub Pages using GitHub Actions, merge that pull request only after required checks pass, and monitor the deployment until it succeeds. Report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![3 段階の図: マージ済みの space-quiz プル リクエスト、Build website、Upload artifact、Deploy to Pages の各ステップが成功した GitHub Actions の Deploy website 実行、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

## デプロイを確認する

1. GitHub Actions のデプロイ実行が成功するまで確認します。
2. 報告された URL を開き、Space Quiz が表示されることを確認します。

エージェントが Pages の有効化やプル リクエストのマージを実行できない場合は、提示された具体的な手順に従ってください。デプロイが成功し、公開サイトが読み込まれるまで、タスクを完了扱いにしないでください。

## まとめと次のステップ

Space Quiz が公開サイトとして利用できるようになり、エージェントの報告に頼るのではなく、デプロイを自分で確認できました。[レッスン 13: 振り返りと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
