# github-slack
- 前のセクションでは、githubにコードをあげるための準備、リポジトリの作成を行いました。
- このセクションでは、githubでの活動(githubにコードをあげる,issueを使って質問する,詳しくは後述)をslackで可視化するために、githubとslackの連携を行います。
- githubとskackの連携が完了すると、以下の写真のような状態になります。
<a href="https://gyazo.com/596478880583c727b46dbcc2e2a4ef97"><img src="https://i.gyazo.com/596478880583c727b46dbcc2e2a4ef97.gif" alt="Image from Gyazo" width="700"/></a>

# 1.github app に slack をインストールする
- まず、github に [slack app(インストールURL)](https://github.com/apps/slack)をインストールします。
[![Image from Gyazo](https://i.gyazo.com/6e3f21ef0b9ad7526de88db6cbbcad75.png)](https://gyazo.com/6e3f21ef0b9ad7526de88db6cbbcad75)
- 次に、[管理画面](https://github.com/settings/installations)でインストールが完了しているか確認して、写真の様になっていれば、インストール完了です。
[![Image from Gyazo](https://i.gyazo.com/b3a8575efb3546b49d870715cc047bf1.png)](https://gyazo.com/b3a8575efb3546b49d870715cc047bf1)

# 3. slack で github に singin する
- 次に、slackでgithubとの連携を行います。
1. `lfs7-52webs-west`で `/github signin` と入力して Enter を押してください。
[![Image from Gyazo](https://i.gyazo.com/66d1130d83b4dd802f074156b97460e2.png)](https://gyazo.com/66d1130d83b4dd802f074156b97460e2)
2. 次に、slackに以下の写真の様な返答が出てくるので、`Connect github account` を押してください。
[![Image from Gyazo](https://i.gyazo.com/fe6fe559990fa5fb1f0c7de667b51849.png)](https://gyazo.com/fe6fe559990fa5fb1f0c7de667b51849)
3. すると、こんな画面が出てくるので、 `Connect github account` を押してください。
[![Image from Gyazo](https://i.gyazo.com/c04267dea6b9ed601c3f4ef83f9a8ae4.png)](https://gyazo.com/c04267dea6b9ed601c3f4ef83f9a8ae4)
4. 今までgithubとslackを連携させとがなければ、 `Authorize Slack by GitHub` を押してください。出てこない人は、一旦無視して、進めてみてください。
5. slack に連携通知が届くはずです
6. 最後に、[ここ](https://github.com/settings/apps/authorizations)で認証がうまくいったかを確認します。下の写真の様になっていれば、認証完了です！
[![Image from Gyazo](https://i.gyazo.com/a222a67e45d61f029cfd10abb3f100a2.png)](https://gyazo.com/a222a67e45d61f029cfd10abb3f100a2)

# 4. slack で リポジトリーを subscribe する
1. slackにgithubの活動の通知を流すためには、slackで `/github subscribe {username}/{repository name}　comments` のコマンドを実行する必要があります。**(commentsはissueへの返信をslackに流すために必要です)**
2. ここでは、slackに先ほど作成した`count`のリポジトリの通知を受け取れるように、`{username}` を自分のgithubのusernameに置き換て、slackで`/github subscribe {username}/count comments` と打ってみよう
3. `{username}`、githubで確認することができます。
  - 例えば、 username が `kohey` だったら、 `kohey/hogehoge` 
4. slack に **`Subscribed to {username}/hogehoge` と表示されていればokです！**

# 5.通知がslackに届くか確認する
  - githubに戻って、`count` のリポジトリを開いて、 `①issue というタブを押して`、`② New issue を押して、内容を投稿`。
  - ①
  <a href="https://gyazo.com/e469451adf4d965c6e2524a553866b05"><img src="https://i.gyazo.com/e469451adf4d965c6e2524a553866b05.png" alt="Image from Gyazo" width="1001.5000265306903"/></a>
  - ②
  <a href="https://gyazo.com/7e3c95d1864d94e95f76483bd83c5bf6"><img src="https://i.gyazo.com/7e3c95d1864d94e95f76483bd83c5bf6.gif" alt="Image from Gyazo" width="888"/></a>
  - slackにさっき投稿した issue が表示されていれば、slackとgithubの連携の完了です。
  
