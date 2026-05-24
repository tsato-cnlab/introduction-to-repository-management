# ステップ 3: 健全な成長を支える

多くの協力者が参加し始めたことで、校長の Martinez 先生から「この Web サイトは学校の重要な基盤になりつつあります。先生たちが増えても健全に育つよう、整理されたルールを追加できますか」と相談されました。

課外活動 Web サイトが成長するにつれて、技術的な保護や contribution guide だけでは足りません。健全で建設的なコミュニケーションも促す必要があります。

代表的な方法を 2 つ見てみましょう。

1. **Code of Conduct**: コミュニティメンバーがどのように関わるべきかの期待値を定める文書です。
1. **Issue Templates**: 問題報告や機能提案に構造を与えます。必要な情報を集めやすくなり、バグ修正や新機能検討が進めやすくなります。

## アクティビティ: Code of Conduct で期待値を示す

成長する先生チームのために、まずはコミュニティガイドラインを整えます。

> [!TIP]
> [Contributor Covenant](https://www.contributor-covenant.org/) は、多くのプロジェクトで使われている行動規範です。

1. **Code** タブに戻り、`prepare-to-collaborate` ブランチ上にいることを確認します。
1. ルートディレクトリに `CODE_OF_CONDUCT.md` という新しいファイルを作成します。
1. Mergington High School 向けの pledge、standards、responsibilities、scope、enforcement、attribution を含む内容を追加します。元の Contributor Covenant を参考にし、学校コミュニティに合う表現にします。
1. 右上の **Commit changes...** を使い、`prepare-to-collaborate` ブランチへ直接コミットします。

## アクティビティ: Issue template で伝えやすくする

次に、ほかの先生がバグ報告や機能リクエストを標準化された形で送れるよう、テンプレートを作成します。

> [!TIP]
> Issue 作成時の体験をよりわかりやすくする [issue forms](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms) の public preview も検討できます。

1. **Settings** タブを選択します。
1. **Features** セクションで **Issues** が有効になっていることを確認します。
1. **Set up templates** ボタンをクリックし、issue templates editor に入ります。
1. **Add template** ドロップダウンをクリックし、**Bug report** を選択します。
1. **Preview and edit** をクリックし、鉛筆アイコンで編集できる状態にします。
1. 任意で、学生や先生向けに簡単にするため、Desktop と Smartphone の詳細セクションを削除します。
1. 同じ手順で **Feature request** テンプレートも追加します。
1. 準備ができたら右上の **Propose changes** をクリックします。説明を入力し、ブランチを `add-issue-templates` にして **Commit changes** をクリックします。自動作成された pull request は無視してかまいません。
1. ファイルをコミットすると、Mona が作業を確認し、次のレッスンを投稿します。

> [!TIP]
> いま 2 つのブランチで並行作業していることに気づきましたか。複数人で共同作業するときも、まさにこのような状態になります。
