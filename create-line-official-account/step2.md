# リッチコンテンツでユーザー体験を高める

## 2-1. リッチメニューを作成する

![richmenu_demo.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/richmenu_demo.png)

メニューから「リッチメニュー」を選択する

![リッチメニュー](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/AccountManagerRichMenu_01.png)

「リッチメニュー」を新規作成する

![リッチメニュー](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/AccountManagerRichMenu_02.png)

タイトルと表示期間を入力する

- 今日の日付が表示期間に含まれるよう設定する
- 時間の欄が空だとリッチメニューを登録できないので注意

![リッチメニュー](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/AccountManagerRichMenu_03.png)

### メニューテンプレートの選択

`テンプレートを選択`を押してテンプレートを選択する（今回は1つのメニューを使います）

![go_to_select_richmenu_template.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/go_to_select_richmenu_template.png)

![リッチメニュー](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/select_template.png)

### メニュー背景画像の作成

`画像を作成`を押して、「サービス選択」メニューをつくります

![go_to_create_richmenu_image.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/go_to_create_image.png)

![create_image](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/create_image.png)

作成できたら`適用`を押します

確認画面でファイルを（ローカルに）保存するか聞かれます。どちらでもいいですが、保存しておくと作成した画像を後から簡単に再利用できます。

![create_image_apply](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/create_image_apply.png)

`適用`を押して次にいきます。


### アクションの設定

下記のように設定します。

![リッチメニュー](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/richmenu_action.png)

- ここで設定したテキストがメニュー押下時にメッセージとして自動送信される

|  A  |  値  |
| :-- | :-- |
|  タイプ  |  テキスト  |
|  テキスト  |  サービス一覧  |

`保存`を押して、作成を完了します。

## 2-2. カードタイプメッセージの作成

![service_list_demo.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/service_list_demo.png)

ユーザーにサービス一覧を提示する、カードタイプメッセージを作成します

![card_type_message_create.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/card_type_message_create.png)

タイトルを「サービス一覧」と設定し、カードタイプは「プロダクト」を選択しましょう

![card_type_message_create_1.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/card_type_message_create_1.png)

![select_card_type.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/select_card_type.png)

下記の通りに設定します。

画像は`デフォルト写真`を使ってもいいですが、今回は[こちら](https://github.com/maztak/katacoda-scenarios/raw/master/create-line-official-account/irasutoya_counselor.png)のいらすとやさんの画像をお借りしてます。

![card_type_messaga_1.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/card_type_messaga_1.png)

ちなみに`カードを追加`を押すことでサービス（商品）を増やしていくことができます。

![add_card.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/add_card.png)

これでリッチコンテンツができました。

次のステップでリッチメニューの`サービス一覧`が押された時に、作成したカードタイプメッセージが自動応答で返されるように設定していきます
