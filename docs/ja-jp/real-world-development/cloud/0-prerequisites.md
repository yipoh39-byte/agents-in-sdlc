---
title: "演習 0: 前提条件"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

Copilot cloud agent の演習を始める前に、必要なものを準備します。Tailspin Toys リポジトリのコピーを作成し、[Codespace][codespaces] を起動します。Codespace で手順ファイルを編集し、cloud agent の作業をレビューします。

## ラボ用リポジトリをセットアップする

作業用のリポジトリを作成するには、[テンプレート リポジトリ][template-repository]からインスタンスを作成します。新しいインスタンスにはラボに必要なファイルがすべて含まれます。演習中はこのリポジトリを使います。

1. 新しいブラウザー ウィンドウで、[Tailspin Toys のテンプレート][tailspin-template]に移動します。
2. ラボ リポジトリのページで **Use this template** ボタンを選択し、自分用のリポジトリを作成します。次に **Create a new repository** を選択します。

    ![Use this template ボタン](../../../_images/ex0-use-template.png)

3. GitHub または Microsoft が主催するイベントでワークショップに参加している場合は、メンターの指示に従ってください。それ以外の場合は、GitHub Copilot を利用できる組織に新しいリポジトリを作成します。

    ![テンプレート リポジトリの設定](../../../_images/ex0-repository-settings.png)

4. 作成したリポジトリのパス (**organization-or-user-name/repository-name**) をメモしてください。ラボの後半で使用します。

## Codespace を作成する

次に、Codespace を使ってラボの演習を完了します。

[GitHub Codespaces][codespaces] はクラウドベースの開発環境です。ブラウザーで直接コードの作成、実行、デバッグができます。複数のプログラミング言語、拡張機能、ツールをサポートする、すべての機能を備えた IDE を利用できます。

1. 作成したリポジトリに移動します。
2. 緑色の **Code** ボタンを選択します。

    ![Code ボタン](../../../_images/ex0-code-button.png)

3. **Codespaces** タブを選択し、**+** ボタンを選択して新しい Codespace を作成します。

    ![新しい Codespace の作成](../../../_images/ex0-create-codespace.png)

Codespace の作成には数分かかりますが、すべてのサービスを手動でインストールするよりもはるかに短時間で済みます。作成中は、次に説明する GitHub Copilot の機能を確認できます。

> [!CAUTION]
> 今後の演習で Codespace に戻ります。今はブラウザーのタブで開いたままにしてください。

> [!NOTE]
> このワークショップは Codespace またはローカルの [開発コンテナー][dev-containers]で実行できるように構成されています。どちらの環境にも、スムーズに進めるために必要な前提条件がすべてインストールされています。ローカルで実行する場合は、クローンしたリポジトリを VS Code で開き、プロンプトが表示されたら **Reopen in Container** を選択します。VS Code が Codespace と同じ開発コンテナーをビルドします。

[codespaces]: https://github.com/features/codespaces
[dev-containers]: https://code.visualstudio.com/docs/devcontainers/containers

## まとめ

おめでとうございます。ラボ用リポジトリのコピーを作成し、Copilot cloud agent と一緒に作業するための Codespace の作成を開始しました。

## 次のステップ

cloud agent が従うカスタム手順を追加します。[演習 1 - カスタム手順][next-lesson]に進みます。

## リソース

- [GitHub Codespaces の概要][codespaces]
- [テンプレートからリポジトリを作成する][template-repository]
- [Codespaces のクイックスタート][codespaces-quickstart]

[tailspin-template]: https://github.com/github-samples/tailspin-toys
[template-repository]: https://docs.github.com/repositories/creating-and-managing-repositories/creating-a-template-repository
[codespaces-quickstart]: https://docs.github.com/codespaces/getting-started/quickstart
[next-lesson]: ../1-custom-instructions/
