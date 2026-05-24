# ステップ 2: 共同作業の準備をする

学校の Web サイトはかなり人気になりました。職員会議で紹介したあと、Art Club の Rodriguez 先生と Chess Club の Chen 先生が、新機能のアイデアをたくさん持ってきました。

- Rodriguez 先生は写真ギャラリーを追加したい。
- Chen 先生はチェスやスポーツ活動向けのトーナメント表機能を追加したい。

協力してくれるのはうれしいことですが、コードを変更し始める前にガイドラインを整える必要があります。春休み直前に、競合する変更で登録システムが壊れるのは避けたいところです。

**Collaborators** は、リポジトリ設定を通じてプロジェクトへの書き込み権限を付与された人たちです。

- リポジトリ設定を守りながら、ほかの人にプロジェクトファイルを変更する権限を与えられます。
- 個人リポジトリの権限はシンプルです。Organization リポジトリでは read、write、maintain、admin など柔軟な権限を使えます。

共同作業を助けるために、GitHub では次の 2 つの特別なファイルを使えます。

1. **`CONTRIBUTING.md`**: 「どう手伝えばよいか」を説明するガイドです。開発環境の準備、変更提案の流れ、コーディングスタイル、困ったときの相談先などを書けます。
1. **`CODEOWNERS`**: プロジェクトの一部に責任を持つ人やチームを指定します。Pull request が作られると、GitHub が適切な人にレビューを依頼します。

## アクティビティ: 歓迎する contribution guide を作成する

明日は IT Club のミーティングです。Rodriguez 先生と Chen 先生がプロジェクトに参加しやすいよう、貢献方法を説明するドキュメントを用意しましょう。

1. 上部ナビゲーションで **Code** タブに戻り、`prepare-to-collaborate` ブランチ上にいることを確認します。
1. ルートディレクトリに `CONTRIBUTING.md` という新しいファイルを作成します。大文字小文字を区別します。
1. 歓迎メッセージを追加します。

   ```md
   # Contributing to the Mergington High Extra-Curricular Activities Website

   Thank you for your interest in helping improve our school's website!
   Whether you want to add your club's activities, fix a bug, or suggest
   new features, this guide will help you get started.
   ```

1. 先生たちがすぐ開発を始められるよう、開発手順、変更手順、コードスタイル、相談先のセクションを追加します。
1. 右上の **Commit changes...** を使い、`prepare-to-collaborate` ブランチへ直接コミットします。

## アクティビティ: コード所有者を割り当てる

ほかの人が参加しても、アーキテクチャや中核機能に関わる変更にはあなたが関われるようにします。

1. **Code** タブに戻り、`prepare-to-collaborate` ブランチ上にいることを確認します。
1. ルートディレクトリに `CODEOWNERS` という新しいファイルを作成します。大文字小文字を区別し、拡張子は付けません。
1. 次の内容を追加します。

   ```codeowners
   # Core functionality - changes here should be rare!
   /src/app.py                   @{{ login }}
   /src/backend/database.py      @{{ login }}
   /src/backend/routers/auth.py  @{{ login }}

   # The frontend will need refactored soon to be more object oriented.
   /src/static/   @{{ login }}
   ```

1. 右上の **Commit changes...** を使い、`prepare-to-collaborate` ブランチへ直接コミットします。
1. ファイルをコミットすると、Mona が作業を確認し、次のレッスンを投稿します。

## アクティビティ: 任意で最初の collaborator を追加する

写真ギャラリー機能を同僚に任せる準備ができたら、collaborator を追加できます。

> [!IMPORTANT]
> この手順は、別の GitHub アカウントを持つ人の参加が必要なため任意です。

1. **Settings** タブを選択します。
1. 左ナビゲーションで **Collaborators** を選択します。
1. **Manage access** で **Add people** をクリックします。
1. 友人または同僚の GitHub ユーザー名かメールアドレスを入力し、**Add to repository** を押します。

> [!IMPORTANT]
> 個人リポジトリには collaborator という 1 種類の共同作業ロールしかありません。より細かい権限が必要な場合は、無料の [organization](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations) を作り、[repository roles](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization) を割り当てることを検討してください。
