heroku側で空のアプリを作成し、先ほど実装したアプリと紐付けます。

①まずは、herokuにログインします。<br>
Terminalに戻って、以下のコマンドを実行します。<br>

```shell
heroku login --interactive
``` {{copy}}

事前に作成しておいたherokuアカウント情報を入力してください。

②herokuでアプリを作成します。<br>
`xxx`の部分はご自身のニックネームなど任意の文字列を指定してください。<br>
英小文字、数字、-(ハイフン)のみ使用可能です。<br>

```shell
heroku create linepay-app-xxx
```{{copy}}

③前のステップで準備したアプリ（リポジトリ）とherokuのアプリを紐づけます<br>
```shell
heroku git:remote -a linepay-app-xxx
```{{copy}}

次のステップでは、herokuに LINE Pay 加盟店アカウント情報を設定します！
