# リッチコンテンツを連動させる

## 3-1. 応答メッセージの作成

応答メッセージを作成しておくと、指定したキーワードが送信されたときに自動で好きなメッセージを応答させることができます。

これまで作成したものが自動応答するように設定していきましょう。


### Defaultの応答メッセージをオフにしておき、新しい応答メッセージを作成する

まずは Default の応答メッセージを`オフ`にしておき、`作成`をおす

![response_message_create.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/response_message_create.png)

### 応答メッセージ「サービス一覧」を作成

![response_message_service_list.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/response_message_service_list.png)

キーワードである`サービス一覧`がユーザーから送られた時にこの応答メッセージを自動で返しますので、この文言を間違えないようにしてください。

### 応答メッセージ「依頼受付」を作成

![response_message_accept.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/response_message_accept.png)

キーワードである`サービス1を依頼する`がユーザーから送られた時にこの応答メッセージを自動で返しますので、この文言を間違えないようにしてください。

以上の設定で、サービス一覧を表示→受付→サービス提供（手動）→決済という一連の流れが可能となりました。