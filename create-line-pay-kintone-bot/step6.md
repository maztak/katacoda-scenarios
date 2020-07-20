

①LINE Bot 側の Webhook を設定する

LINE Developers ＞ `Messaging API設定` ＞ `Webhook設定`の項目にて以下のように Webhook　URL を設定します。

```
https://line-pay-kintone-bot-xxx.herokuapp.com/callback
```

![webhook_setting.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-kintone-bot/img/webhook_setting.png)

`検証`を押して「成功」と返ってきたら、`Webhookの利用`をオンにしておきます

<font color="red">初回は200エラーになります。検証がエラーでもWebhookをオンにできたりしますが、一度 https://line-pay-kintone-bot-xxx.herokuapp.com/callback にブラウザでアクセスしてからやり直すと成功します</font>

②Botを試す

試しにLINEアプリでBotに`linepay300`というテキストを送ってみます。

そうすると300円の決済内容の LINE Pay URL が発行されるはずです。

![line_pay_bot_demo.jpeg](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-kintone-bot/img/line_pay_bot_demo.jpeg)

最初はHerokuの起動に時間がかかるので1分くらいかかる場合があります（有料プランにすると素早く起動するようになります）。