herokuアプリの環境変数として LINE Pay 加盟店アカウントの決済連動キー情報を設定していきます。

①herokuの環境変数を設定します<br>

LINEのSandboxにより取得したアカウントで、加盟店 My Page にアクセスします。<br>
[LINE Pay 加盟店 My Page](https://pay.line.me/portal/jp/auth/login)

<font color="red">加盟店IDの`@line.pay`は自動で入力されるので注意</font>

`決済連動管理` > `連動キー管理` で再度パスワードを入力すると以下画面にいきます。

![line-pay-mypage](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-app/img/pay_line_me_jp_center_payment_interlockKey_locale_ja_JP_isAuthenticated_true_csrfToken.png)

```shell
heroku config:set LINE_PAY_CHANNEL_ID="xxx"
```{{copy}}

```shell
heroku config:set LINE_PAY_CHANNEL_SECRET="xxx"
```{{copy}}

<font color="red">xxxの部分は各自異なります</font><br>

続いて LINE Bot に使用する環境変数を設定します。

LINE Developers で作成したチャネルの「チャネルシークレット」と「チャネルアクセストークン」を環境変数として設定します。

`LINE Developers` > `チャネル基本設定`

![channel_secret.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-app/img/channel_secret.png)

```shell
heroku config:set LINE_CHANNEL_SECRET="xxx"
```{{copy}}

`LINE Developers` > `Messaging API設定`

![channel_access_token.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-app/img/channel_access_token.png)

```shell
heroku config:set LINE_CHANNEL_SECRET="xxx"
```{{copy}}

以下のコマンドで環境変数が正しく設定されているか確認しましょう。

```shell
heroku config
```{{copy}}

これでheroku側の準備が終わりました。

次のステップでいよいよ作成した LINE Pay アプリをデプロイ（Webサーバーにアップロードして実際に使えるようにする）します。