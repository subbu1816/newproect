## 1日目の実習

### 新しいスライドを追加する

クラスで作業したように、デッキに新規スライドを追加するために新規Pull Requestを行います。

1. 新しいブランチを作成し、そのブランチにチェックアウトします。`git switch -c NEWBRANCHNAME（新規ブランチ名）`
2. `_posts`ディレクトリに新しいファイルを作成する。そのファイル名は、YYYY-MM-DD-username-description.md （年-月-日-ユーザ名-ファイル内容）のようにする。 (日付は、過去の日付でなければならず、将来の日付は表示されません。)
3. "[Activity: Edit Your File](https://githubtraining.github.io/training-manual/#/ja/06_working_locally)"にある、一緒に作成した同じ実習の指示に従います。
4. キャプションをただ追加するのではなく、イメージリストから新しいイメージを見つけ、テンプレートへの入力に使用します。 ``` \--- layout: slide \---

        IMAGEURL
        {: .center}

        CAPTION-HERE
        {: .fragment}
        ```

5. 新規ブランチに変更を保存してコミットします。

6. ローカルで作業している場合は、リモートに変更をプッシュします。`git push -u origin NEWBRANCHNAME`.
7. Pull Requestを開きます。Pull Requestの本文で、変更をレビューしてもらいたい人に、@メンションします。
8. Pull Requestがテストに合格したら、Pull Requestをマージします。

### 既存のスライドにキャプションを追加する

他のユーザのPull Requestにある既存のスライドにキャプションを追加する。

1. キャプションを追加したいPull Requestを見つけます。
2. 「files changed」をクリックして他のユーザが選択したイメージを確認し、次に「view」をクリックします。
3. キャプションを追加するために、ブラウザーまたはローカルでファイルを編集します。 （他の人がこのファイルに追加した作業は消去しないでください。）
    - ローカルで作業している場合は、ブランチにチェックアウトする必要があります。
    - ローカルのリポジトリにリモートの変更がすべて反映されていることを確認します。` git pull `
    - Pull Requestにあるブランチ名を探し、ローカルでそのブランチにチェックアウトします。`git switch BRANCHNAME`
4. 変更を保存し、ファイルをコミットします。
    - ローカルで作業している場合は、変更内容をリモートにプッシュします。` git push `
5. Pull Requestをマージしないでください。 `@`メンションでPull Requestを作成したユーザに変更を知らせます。

### `README.md`を改善する

お好みのリソースを加えて、 `README.md`を改善しましょう。

1. 新しいブランチを作成し、そのブランチにチェックアウトします。`git switch -c NEWBRANCHNAME（新規ブランチ名）`
2. 何らかの方法で、README.mdを改善します。 改善方法は、新しいリソースの追加や、既存の説明内容の明確化などです。 変更を保存してコミットします。
3. ローカルで作業している場合は、リモートに変更をプッシュします。`git push -u origin NEWBRANCHNAME（新規ブランチ名）`.
4. Pull Requestを作成します。Pull Requestの本文には、`base: main` と `compare: NEWBRANCHNAME（新規ブランチ名）`　を記載します。
5. `@` mention（メンション）を使って、変更をレビューしてもらいたい人に知らせます。
6. Pull Requestの内容がテストに合格したら、そのPull Requestをマージします。

### スライドのスタイル変更

高度なチャレンジに取り組みたい場合や、スタイル編集に自信がある場合、クラスのスライドデッキの色、フォントや他の要素を変更してみましょう。 **注：複数の参加者が試すと、マージコンフリクトが発生するおそれがあります。**

1. 新しいブランチを作成し、そのブランチにチェックアウトします。`git switch -c NEWBRANCHNAME（新規ブランチ名）`
2. 次のファイルを探します。`_sass / solarized / solarized.scss`
3. ファイルに変更を加えます。
    - 12〜19行目は、色に影響します。
    - 33〜35行目は、フォントとフォントサイズに影響します。
    - 52〜55行目は、ヘッダの色に影響します
4. ブランチに変更を保存してコミットします。
5. ブランチをリモートにプッシュします。` git push -u origin NEWBRANCHNAME（新規ブランチ名） `
6. `base: main`と`compare: NEWBRANCHNAME（新規ブランチ名）`で、Pull Requestを開きます。
7. `@` mention（メンション）を使って、変更をレビューしてもらいたい人に知らせます。
8. Pull Requestの内容がテストに合格したら、そのPull Requestをマージします。
