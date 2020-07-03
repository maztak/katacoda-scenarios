herokuにデプロイしましょう


1. gitでherokuにpushします

```shell
git push heroku master
```{{copy}}

3. これで LINE Pay アプリがデプロイされ使えるようになりました。

ログの5行前に`remote: https://linepay-app-xxx.herokuapp.com/ deployed to Heroku`と表示されていると思うので、このURLにアクセスしてみましょう。<br>
`Request`ボタンを押せば、LINEアプリと連動して実際に一般決済が試せるはずです！

デプロイしたばかりだと Internal Server Error になることがあるようです。少し間を置いて再度試してみてください。