Herokuにアプリをデプロイしていきます

①Botが返す決済URLを自身のものに変更する

app.pyの378行目付近にある`payurl`をご自身のHerokuアプリのURLに書き換えます

```
payurl = 'https://ご自身Herokuアプリ名.herokuapp.com/request/nocapture?amount=' + amount
↓
payurl = 'https://line-pay-kintone-bot-xxx.herokuapp.com/request/nocapture?amount=' + amount
```

アプリ名（HerokuアプリのURL）はアプリを開く以下のコマンドでも確認できます

```shell
heroku open
```{{copy}}


②gitの初期設定

バージョン管理ツールgitの初期設定を行いましょう

```shell
git config --global user.email example@example.com
```{{copy}}

<font color="red">example@example.com部分はご自身のメールアドレスに置き換えてください</font>

```shell
git config --global user.name your_name
```{{copy}}

<font color="red">your_name部分はご自身の名前（ニックネーム等）に置き換えてください</font>

③変更内容をコミット

```shell
git add .
```{{copy}}

```shell
git commit -m "first commit"
```{{copy}}

④変更内容をherokuにpush

```shell
git push heroku master
```{{copy}}

これで LINE Pay アプリがデプロイされました。
