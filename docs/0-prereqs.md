# 演習 0: 事前準備

ラボを始める前に、いくつかの準備を行います。コードを含むリポジトリのコピーを作成し、開発で使用する [Codespaces](https://github.com/features/codespaces) を起動します。

## ラボ用リポジトリの作成

このラボで使うコードのコピーは、リポジトリの[テンプレート機能](https://docs.github.com/ja/repositories/creating-and-managing-repositories/creating-a-template-repository)を使って作成します。作成したリポジトリにはラボに必要なファイルがすべて含まれ、以降の演習で利用します。

1. 新しいブラウザタブで、このラボの GitHub リポジトリにアクセスします: `https://github.com/se-copilot-workshops/agents-in-sdlc-jp`。ご自身のアカウントでサインインしてください。
2. リポジトリページの **Use this template** をクリックし、**Create a new repository** を選びます。

    ![Use this template ボタン](images/use-template.png)

> [!IMPORTANT]
> Ownerは **se-copilot-workshops** を選び、リポジトリ名にはご自身の GitHub ハンドルを使用してください。

3. Ownerに **se-copilot-workshops** を選び、リポジトリ名にご自身の GitHub ハンドルを設定します。これにより Copilotコーディングエージェントへのアクセスや、Issue を Copilot に割り当てる操作が可能になります。

    ![テンプレートの作成設定](images/repository-template-settings.png)

4. **Create repository** をクリックします。
5. 作成したリポジトリのパス（例: **se-copilot-workshops/**___GHhandle___）をメモしておいてください。後の演習で参照します。

## Codespace の作成

続いて、演習を進めるための Codespace を作成します。[GitHub Codespaces](https://github.com/features/codespaces) は、ブラウザ上でコードの作成・実行・デバッグができるクラウドベースの開発環境です。複数言語や拡張、各種ツールに対応した IDE を提供します。

1. 先ほど作成したリポジトリを開きます。
2. 緑色の **Code** ボタンをクリックします。

    ![Code ボタン](images/code-button.png)

3. **Codespaces** タブを開き、**+** ボタンを押して新規 Codespace を作成します。
   （**TIP:** 作成完了を待たず、次の手順を読み進めて構いません）

    ![新しい Codespace の作成](images/create-codespace.png)

Codespace の作成には数分かかります（それでも各種サービスを手動でインストールするよりはずっと速いです）。この待ち時間を活用して、GitHub Copilot に非同期で任せられるタスクの準備を進めましょう。

## まとめ

お疲れさまでした。ラボ用リポジトリのコピーを作成し、以降で使用する Codespace の作成も開始できました。次のレッスンの後で、再びこの環境に戻って作業を続けます。

## 次のステップ

数分の余裕があるうちに、Copilot に非同期タスクを任せる準備を進めましょう。Issue を作成し、Copilotコーディングエージェントに割り当てます。次の演習へ進むには以下をクリックしてください。
[次の演習: Copilotコーディングエージェント](./1-copilot-coding-agent.md)
