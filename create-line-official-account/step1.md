
# チャネルの作成

Step1 ではLINE 側の設定画面でBot を利用するためのチャネルの作成や設定を行います。


## 1-1. LINE Developers 

[LINE Developers](https://developers.line.biz/console/) にログインします


## 1-2. プロバイダーを選択

任意のプロバイダーを選択します。

プロバイダー未作成の人は画面上の「作成」ボタンを押下して新規作成してください。

- 任意の「プロバイダー名」を入力して作成
- LINEという文字列は含められません

![プロバイダー選択](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/ProviderList.png)


## 1-3. チャネルを新規作成

チャネルを作成

![チャネル作成](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/NewChannel.png)

「Messaging API」 を選択

![Messaging API](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/SelectMessagingAPI.png)

チャネル情報を入力して、「入力内容を確認する」ボタンを押下する

### チャネル情報の入力例

|  項目名  |  値  |
| :-- | :-- |
|  アプリ名  |  LDGQ相談サービス  |
|  アプリ説明  |  LDGQ相談ービス  |
|  大業種  |  個人  |
|  小業種  |  個人（その他）  |
|  メールアドレス  |  （ご自分のメールアドレス）  |
|  プライバシーポリシーURL  |  （入力不要）  |
|  サービス利用規約URL  |  （入力不要）  |


各種規約に同意してチャネルを作成する

![各種規約に同意](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/AgreeTerms.png)

情報利用に関する事項に同意する

![情報利用に関する事項に同意する](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/AgreeTerms02.png)

これで チャネルの作成が完了し、同時にLINE公式アカウントも自動作成されます。

## 1-4. 応答設定

### LINE Official Manager に行く

チャネル基本設定にあるリンクから、LINE Official Account Manager にいきます

![line_developers_channel_basic_setting](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/line_developers_channel_basic_setting.png)


### 応答設定画面を開く

LINE Official Account Manager の`設定`＞`応答設定`メニューを選択して応答設定画面を開く

![応答設定](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/go_to_response_setting.png)

応答設定を下記のように設定する

![応答設定](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/line_official_account_manager_response_setting.png)

|  項目名  |  値  |
| :-- | :-- |
|  応答モード  |  チャット  |
|  あいさつメッセージ  |  オン  |
|  応答時間  |  オン  |
|  応答方法 応答時間内  |  スマートチャット（AI応答メッセージ＋手動）  |
|  応答方法 応答時間外  |  AI応答メッセージ  |


## 1-5. 作成したアカウントを友だち追加する

LINE Official Account Manager の`ホーム`＞`友達追加`にあるQRコードで、自分のスマホLINEアプリに友達追加しておく。

![QRCode](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/line_official_account_manager_add_friend.png)

※QRコードは、LINE Developers の「Messaging API 設定」タブにもあります。

これで、LINE公式アカウントが作成できたので、LINE上で`https://linepay-app-xxx.herokuapp.com/request/nocapture`というリンクをユーザーに送ってやれば、そのまま LINE Pay による支払いをしてもらうことが可能となります。

しかしURLのベタ貼りではユーザーも不安になるので、次のステップ以降では各リッチコンテンツを使ってユーザー体験を高めていきます。