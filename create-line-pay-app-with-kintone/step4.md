いよいよ LINE Pay アプリをherokuにデプロイします。内容としてはまだ中身がほぼ空のheroku側アプリに、ローカルのファイルをアップロードして上書きする作業になります。

①gitでherokuにpushします

```shell
git push heroku master
```{{copy}}

これで LINE Pay アプリがデプロイされ使えるようになりました。<br>

②ブラウザでアプリURLにアクセスしてみよう<br>

アプリのURL`https://linepay-app-xxx.herokuapp.com/`にアクセスしてみましょう。<br>

`Request`ボタンを押せば、LINEアプリと連動して実際に一般決済が試せるはずです！

デプロイしたばかりだと Internal Server Error になることがあるようです。少し間を置いて再度試してみてください。