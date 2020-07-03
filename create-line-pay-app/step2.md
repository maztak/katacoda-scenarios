herokuにアプリを作成します。

1. まずは、herokuにログインします。<br>
Terminalに戻って、以下のコマンドを実行します。<br>

```shell
heroku login --interactive
```{{copy}}

2. herokuでアプリを作成します。<br>
アプリの名前は一意になるようにしてください。英小文字、数字、-(ハイフン)のみ使用可能です。<br>
（無料アカウントは5つまでアプリを作成できます。クレジットカード登録したら作成枠が増えます。）

```shell
heroku create linepay-app-xxx
```{{copy}}


3. 前のステップで準備したアプリ（リポジトリ）とherokuのアプリを紐づけます<br>
```shell
heroku git:remote -a linepay-app-xxx
```{{copy}}

次のステップでは、〇〇をします！
