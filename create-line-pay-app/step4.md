herokuにアプリをアップロードしましよう。

1. gitの初期設定を行います<br>

```shell
git config --global user.email example@example.com
```{{copy}}

<font color="red">example@example.com部分はご自身のメールアドレスに置き換えてください</font><br>

```shell
git config --global user.name your_name
```{{copy}}

<font color="red">your_name部分はご自身の名前に置き換えてください</font><br>

2. gitでherokuにデプロイします。gitのコマンドを3つ実行します。<br>

```shell
git add .
```{{copy}}

```shell
git commit -m "first commit"
```{{copy}}

```shell
git push heroku master
```{{copy}}

3. これで LINE Pay アプリがデプロイされ使えるようになりました。

3行ほど前に`remote: https://linepay-app-xxx.herokuapp.com/ deployed to Heroku`と表示されていると思うので、このURLをクリックしてアクセスしてみましょう。<br>
`Request`ボタンを押せば、LINEアプリと連動して実際に一般決済が試せるはずです！

デプロイしたばかりだと Internal Server Error になることがあるようです。少し間を置いて再度試してみてください。