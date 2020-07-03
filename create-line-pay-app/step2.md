前のステップで準備したアプリをherokuにデプロイする準備をしましょう

1. まずは、herokuにログインします。<br>
Terminalに戻って、以下のコマンドを実行します。<br>

```shell
heroku login --interactive
```{{copy}}

2. herokuでアプリを作成します。<br>
無料で5つまで作成でき、クレジットカード登録したら作成枠が増えます。アプリの名前は一意になるようにしてください。英小文字、数字、-(ハイフン)のみ使用可能です。<br>

```shell
heroku create linepayapp-xxx
```{{copy}}

アプリが作成されたらURLが出力されるので控えておいてください。<br>
> 例）https://linepayapp-xxx.herokuapp.com

3. 前のステップで準備したアプリ（リポジトリ）とherokuのアプリを紐づけます<br>
```shell
heroku git:remote -a linepayapp-xxx
```{{copy}}

次のステップでは、〇〇をします！
