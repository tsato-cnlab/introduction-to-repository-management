# ステップ 4: 避けられない問題に備える

職員室でコーヒーを飲みながら、あなたは気づきます。より多くの先生がコードに関わるようになるほど、セキュリティ脆弱性が入り込む可能性も高くなります。

どれほどよく保守されたコードベースでも、いずれセキュリティ上の課題に向き合うことになります。GitHub が提供するいくつかのツールを設定し、その日に備えましょう。

1. **Dependabot**: プロジェクトが使う依存関係に含まれる脆弱性を追跡し、アラートを作成します。安全なバージョンへ更新する pull request も自動作成できます。
1. **Code Scanning**: リポジトリのコードを分析し、セキュリティ脆弱性やコーディングエラーを見つけます。GitHub Copilot Autofix を使って修正案を提案できます。
1. **Security Policy and Private vulnerability reporting**: セキュリティ研究者や利用者が、脆弱性を安全に報告するためのガイドとフォームを用意します。

> [!NOTE]
> ここではすばやく設定するための概要だけを扱います。詳しくは関連する GitHub Skills 演習や GitHub Docs を参照してください。

## アクティビティ: Dependabot でセキュリティ更新を自動化する

Dependabot を既定設定で有効にし、アラートの修正を自動的にまとめ、pull request を作成できるようにします。

1. **Settings** タブを選択します。
1. 左ナビゲーションで **Advanced Security** を選択します。
1. **Dependabot** セクションで次の設定になっていることを確認します。
   - **Dependabot alerts**: `enabled`
   - **Dependabot security updates**: `enabled`
   - **Grouped security updates**: `enabled`
1. **Dependabot version updates** を見つけ、**Enable** をクリックします。設定ファイルを作成するエディタが開きます。
1. 左のファイル一覧で **Expand file tree** をクリックし、ブランチを `prepare-to-collaborate` に変更します。ruleset により `main` へ直接変更できないことを思い出してください。
1. `package-ecosytem` を `pip` に設定し、Python requirements を Dependabot が監視できるようにします。
1. 右上の **Commit changes...** を使い、`prepare-to-collaborate` ブランチへ直接コミットします。

## アクティビティ: code scanning で危険なパターンを検出する

学校の先生たちはプロのソフトウェア開発者ではありません。潜在的に危険なことをしている場合に知らせてもらえるよう、code scanning を有効にします。さらに、GitHub Copilot が解決策の pull request を作れるようにします。

1. **Settings** タブを選択します。
1. 左ナビゲーションで **Advanced Security** を選択します。
1. **Code scanning** セクションで **Set up** をクリックし、**Default** を選択します。
1. **Enable CodeQL** をクリックし、既定設定を受け入れます。
1. **Tools** セクションの下で **Copilot Autofix** が `On` になっていることを確認します。

## アクティビティ: セキュリティ報告の安全な経路を用意する

自動化の準備ができたので、人間が脆弱性を見つけたときに安全に報告できるガイドを作成します。

1. **Settings** タブを選択します。
1. 左ナビゲーションで **Advanced Security** を選択します。
1. **Private vulnerability reporting** が `enabled` になっていることを確認します。
1. 上部ナビゲーションで **Security** タブをクリックします。
1. 左ナビゲーションで **Policy** をクリックします。
1. **Start setup** をクリックします。`SECURITY.md` を作成するエディタが開きます。
1. 左のファイル一覧で **Expand file tree** をクリックし、ブランチを `prepare-to-collaborate` に変更します。
1. テンプレートは使わず、Mergington High School の IT 部門の推奨に沿って、脆弱性の報告方法、対応タイムライン、謝辞を含む `SECURITY.md` を作成します。
1. 右上の **Commit changes...** を使い、`prepare-to-collaborate` ブランチへ直接コミットします。
1. ファイルをコミットすると、Mona が作業を確認し、次のレッスンを投稿します。
