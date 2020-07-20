まず LINE Pay アプリを実装しましょう。

①Githubから[line-pay-v3-python-kintone-bot](https://github.com/maztak/line-pay-v3-python-kintone-bot) リポジトリをCloneします<br>

```shell
git clone https://github.com/maztak/line-pay-v3-python-kintone-bot.git
```{{copy}}

②カレントディレクトリを`line-pay-v3-python-kintone-bot`に変更します<br>

```shell
cd line-pay-v3-python-kintone-bot
```{{copy}}

③`pip`コマンドで`requirements.txt`に記載のライブラリをインストールします<br>
```shell
pip install -r requirements.txt
```{{copy}}

④kintone連携のための設定
今回はkintoneの売上管理アプリを連携させるので、`account.yml`を編集していきます。

Editorで`line-pay-v3-python-kintone-bot`ディレクトリをクリックして展開し、`account.yml`を開きます。

前のシナリオでkintoneに追加したlinepay連携アプリの情報をもとに値を変更します。
![kintone_api_token](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-app/img/kintone_api_token.png)


```account.yml
domain: kintone開発者環境のサブドメインだけを記載
apps:
    linepay: ←アプリ名
        id: kintoneアプリのID
        token: kintoneで生成したAPIトークン
```

アプリ名は今回`linepay`とあらかじめ入力しておきました。

<font color="red">過去に同名のアプリがあると（それが削除されてても）kintoneとの連動が上手く行きません。</font>

ちなみに、kintoneアプリIDはアプリ追加ごとに連番で振られます。

これで決済が動くために必要なものが揃いました。

⑤実際のウォレットから決済できるようにする（任意）

初期のコードでは決済してもSandboxのテストウォレットから支払われるので実際のお金は決済されません。ただし実際の決済と挙動が変わるので、自分のLINEウォレットから払っても良い方は`app.py`の`LINE_PAY_IS_SANDBOX`を`False`にしてください（あとで返金できます）。

```app.py
# app.py
# LINE Pay API
LINE_PAY_IS_SANDBOX = True  # ←ここをFalseにすると実際にお金が引き落とされる
```

次のステップでは、heroku側の初期設定を行います。
