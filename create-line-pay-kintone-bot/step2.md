heroku側で空のアプリを作成し、先ほど実装したアプリと紐付けます。

①まずは、herokuにログインします。

Terminalに戻って、以下のコマンドを実行します。

```shell
heroku login --interactive
``` {{copy}}

事前に作成しておいたherokuアカウント情報を入力してください。

②herokuでアプリを作成します。

`xxx`の部分はご自身のニックネームなど任意の文字列を指定してください。

英小文字、数字、-(ハイフン)のみ使用可能です。

```shell
heroku create line-pay-kintone-botxxx
```{{copy}}

③前のステップで準備したアプリ（リポジトリ）とherokuのアプリを紐づけます

```shell
heroku git:remote -a line-pay-kintone-botxxx
```{{copy}}

次のステップでは、herokuに LINE Pay 加盟店アカウント情報を設定します！
