# ステップ 1: コードを保護する

Mergington High では、課外活動を管理するための小さな Web サイトが人気になりました。いくつかの活動向けの簡単な申し込みフォームから始まったものが、今では学校活動の多くで使われる場所になっています。

校長の Martinez 先生はこの成果に感心し、すべてのクラブがこの Web サイトを使い始めるべきだと職員会議で発表しました。うれしい一方で、秋の活動フェア直前に誰かのうっかり変更でシステムが壊れるのは避けたいところです。

ほかの先生たちも Web サイトの更新を手伝い始めるなら、安全策が必要です。GitHub にはリポジトリを守るための機能があります。

1. **Repository Rulesets**: 重要なブランチへの直接 push、ブランチの削除や名前変更、履歴を上書きする force push などを制限できます。
1. **`.gitignore`**: 実行時に生成される一時ファイル、秘密情報を含む設定ファイル、ほかの開発者に不要なシステムファイルなど、Git が追跡しないファイルを指定します。

> [!TIP]
> これは学校の卒業アルバムの編集プロセスに似ています。各委員会が写真や記事を集め、編集長が全体の流れを整え、最後に先生が内容を確認します。

## アクティビティ: 任意で課外活動サイトを確認する

<details>
<summary>手順を表示</summary>

[Getting Started with GitHub Copilot](https://github.com/skills/getting-started-with-github-copilot/) の演習では、この課外活動 Web サイトを開発してきました。開発環境を起動して試すには、次の手順を使えます。

> **重要:** この演習を完了するために、開発環境を開いたりアプリを実行したりする必要はありません。必要なければスキップできます。

1. 次のボタンを右クリックし、**Create Codespace** ページを新しいタブで開きます。既定の設定を使います。

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

1. 環境の準備が終わるまで少し待ちます。必要なパッケージとサービスは自動でインストールされます。

1. **GitHub Copilot** と **Python** 拡張機能がインストールされ、有効になっていることを確認します。

   <img width="300" alt="copilot extension for VS Code" src="https://github.com/user-attachments/assets/ef1ef984-17fc-4b20-a9a6-65a866def468" /><br/>
   <img width="300" alt="python extension for VS Code" src="https://github.com/user-attachments/assets/3040c0f5-1658-47e2-a439-20504a384f77" />

1. 左サイドバーで **Run and Debug** タブを選択し、**Start Debugging** アイコンを押してアプリを実行してみます。

1. **Ports** タブで Web ページのアドレスを見つけ、開いて動作を確認します。

</details>

## アクティビティ: ブランチ ruleset を追加する

クラブ登録システムを誰かが誤って壊さないよう、まずは保護を追加します。

1. 必要であれば別タブでこのリポジトリを開きます。**Settings** タブから始めます。
1. 左ナビゲーションで **Rules** を展開し、**Rulesets** を選択します。
1. **New ruleset** ドロップダウンをクリックし、**New branch ruleset** を選択します。
1. **Ruleset Name** を `Protect main`、**Enforcement status** を `Active` にします。
1. **Targets** セクションで **Add target** ドロップダウンを使い、次の 2 つを追加します。
   1. **Include default branch**
   1. **include by pattern** を選び、パターンに `main` を入力
1. **Rules** セクションで次を有効にします。
   - [x] Restrict deletions
   - [x] Require a pull request before merging
     - Required approvals: `0`
     - [x] Require review from Code Owners
   - [x] Block force pushes
1. 下までスクロールし、**Create** をクリックして ruleset を保存します。

## アクティビティ: `.gitignore` ファイルを作成する

先生たちはさまざまなツールを使うので、不要なファイルを誤ってコミットしないようにします。

1. 上部ナビゲーションで **Code** タブに戻り、`main` ブランチ上にいることを確認します。
1. ファイル一覧の上にある **Add file** ドロップダウンをクリックし、**Create new file** を選択します。
1. ファイル名に `.gitignore` と入力します。テンプレート選択は使わず、次の内容をコピーします。

   ```gitignore
   # Python backend for club management
   __pycache__/
   *.py[cod]
   *$py.class
   *.so
   .Python
   env/
   .env
   venv/
   .venv

   # Teacher IDE settings
   .vscode/
   .idea/

   # Local development & testing
   instance/
   .pytest_cache/
   .coverage
   htmlcov/

   # Staff computer files
   .DS_Store
   Thumbs.db
   ```

1. 右上の **Commit changes...** を選択します。`main` ブランチへ直接コミットできないことに注目してください。ruleset が働いています。
1. ブランチ名に `prepare-to-collaborate` と入力し、**Propose changes** をクリックします。新しい pull request を開始するページへ移動します。
1. タイトルを `Prepare to collaborate` にして **Create pull request** をクリックします。共同作業に関する変更をさらに追加するため、**まだマージしないでください**。
1. ファイルをコミットすると、Mona が作業を確認し、次のレッスンを投稿します。

> [!TIP]
> GitHub とコミュニティは、多くの状況向けの [sample `.gitignore` files](https://github.com/github/gitignore) を用意しています。

<details>
<summary>うまくいかない場合</summary><br/>

`.gitignore` を `prepare-to-collaborate` ブランチへ push していることを確認してください。ファイル名とブランチ名の両方が重要です。

</details>
