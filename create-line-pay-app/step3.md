heroku側の設定（LINE加盟店情報を設定）

1. herokuの環境変数を設定します<br>

LINEのSandboxにより取得したアカウントで、加盟店 My Page にアクセスします。
LINE Pay 加盟店 My Page
https://pay.line.me/portal/jp/auth/login

<font color="red">加盟店IDの`@line.pay`は自動で入力されるので注意</font>

`決済連動管理` > `連動キー管理` で再度パスワードを入力すると以下画面にいきます。

![line-pay-mypage](https://raw.githubusercontent.com/maztak/katacoda-scenarios/blob/master/create-line-pay-app/img/pay_line_me_jp_center_payment_interlockKey_locale_ja_JP_isAuthenticated_true_csrfToken.png)

```shell
heroku config:set LINE_PAY_CHANNEL_ID="xxx"
```{{copy}}

```shell
heroku config:set LINE_PAY_CHANNEL_SECRET="xxx"
```{{copy}}

<font color="red">xxxの部分は各自異なります</font><br>

以下のコマンドで環境変数が正しく設定されているか確認しましょう。<br>

```shell
heroku config
```{{copy}}

これでheroku側の準備が終わりました。<br>
次のステップでいよいよ作成した LINE Pay アプリをデプロイ（Webサーバーにアップロードして実際に使えるようにする）します。