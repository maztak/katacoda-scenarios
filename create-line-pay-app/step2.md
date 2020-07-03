heroku側の設定

1. まずは、herokuにログインします。<br>
Terminalに戻って、以下のコマンドを実行します。<br>

```shell
heroku login --interactive
```{{copy}}

事前に作成しておいたherokuアカウント情報を入力してください。

2. herokuでアプリを作成します。<br>
アプリの名前は一意である必要があるので`xxx`の部分はご自身のニックネームなど任意の文字列を指定してください。英小文字、数字、-(ハイフン)のみ使用可能です。<br>

```shell
heroku create linepay-app-xxx
```{{copy}}

（無料アカウントは5つまでアプリを作成できます。クレジットカード登録したら作成枠が増えます。）

3. 前のステップで準備したアプリ（リポジトリ）とherokuのアプリを紐づけます<br>
```shell
heroku git:remote -a linepay-app-xxx
```{{copy}}

次のステップでは、〇〇をします！
