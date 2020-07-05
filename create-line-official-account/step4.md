# サービス提供時の注意

例えばユーザーと手動でメッセージをやり取りする場合はチャット画面にいき`手動チャットに切り替え`を押すことで、そのユーザーだけ自動応答やAI応答をオフにし、手動でチャットをすることができます。

![go_to_chat_page.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/go_to_chat_page.png)

![change_to_manual_chat.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/change_to_manual_chat.png)

![send_manual_message.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/send_manual_message.png)

ただしサービス提供が終わるなどしてユーザーに決済をしてもらいたい場合、手動チャットの状態でリッチメニューの「決済」ボタンを押されても自動応答が反応しません。

そのため決済のタイミングになったら再度`AI応答メッセージに切り替え`を押して、自動応答を有効化する必要があります（つまり手動チャットでは各リッチコンテンツを送信することができないのです（泣））

![change_ai_response_message.png](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-official-account/images/change_ai_response_message.png)

以上で、LINE公式アカウントと LINE Pay を使った最小限のサービス提供が可能になりました。

実際にユーザーにお金を支払って貰う場合は [LINE Pay 加盟店申請](https://pay.line.me/portal/jp/business/contact)が必要ですが、個人事業主であれば申請可能ですので、この機会にトライしてみてはいかがでしょう？