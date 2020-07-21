まず LINE Pay アプリを実装しましょう。

①Githubから[line-pay-v3-python-sdk-sample](https://github.com/maztak/line-pay-v3-python-sdk-sample) リポジトリをCloneします<br>

```shell
git clone https://github.com/maztak/line-pay-v3-python-sdk-sample.git
```{{copy}}

②カレントディレクトリを`line-pay-v3-python-sdk-sample`に変更します<br>

```shell
cd line-pay-v3-python-sdk-sample
```{{copy}}

③`pip`コマンドで`requirements.txt`に記載のライブラリをインストールします<br>
```shell
pip install -r requirements.txt
```{{copy}}

④kintone連携のための設定
今回はkintoneの売上管理アプリを連携させるので、`account.yml`を編集していきます。

Editorで`line-pay-v3-python-sdk-sample`ディレクトリをクリックして展開し、`account.yml`を開きます。

前のシナリオでkintoneに追加したlinepay連携アプリの情報をもとに値を変更します。
![kintone_api_token](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-app/img/kintone_api_token.png)


```account.yml
domain: kintone開発者環境のサブドメイン
apps:
    linepay: ←アプリ名
        id: kintoneアプリのID
        token: kintoneで生成したAPIトークン
```

アプリ名は今回`linepay`とあらかじめ入力しておきました。

<font color="red">過去に同名のアプリがあると（それが削除されてても）kintoneとの連動が上手く行きません。アプリをアップロード後にアプリ名を変更してもダメなようです</font>

ちなみに、kintoneアプリIDはアプリ追加ごとに連番で振られます。

これでアプリが動くために必要なものが揃いました。

⑤実際のウォレットから決済できるようにする（任意）

初期のコードでは決済してもSandboxのテストウォレットから支払われて、実際のお金は決済されません。ただし実際の決済と挙動が変わるので、自分のLINEウォレットから1円払っても良い方は`app.py`の`LINE_PAY_IS_SANDBOX`を`False`にしてください。

```app.py
# LINE Pay API
LINE_PAY_CHANNEL_ID = os.environ.get("LINE_PAY_CHANNEL_ID")
LINE_PAY_CHANNEL_SECRET = os.environ.get("LINE_PAY_CHANNEL_SECRET")
LINE_PAY_IS_SANDBOX = True  # ←ここをFalseにすると実際にお金が引き落とされる
api = LinePayApi(LINE_PAY_CHANNEL_ID,
                 LINE_PAY_CHANNEL_SECRET, is_sandbox=LINE_PAY_IS_SANDBOX)
```

⑥gitの初期設定<br>

まずは初期設定を行いましょう<br>

```shell
git config --global user.email example@example.com
```{{copy}}

<font color="red">example@example.com部分はご自身のメールアドレスに置き換えてください</font><br>

```shell
git config --global user.name your_name
```{{copy}}

<font color="red">your_name部分はご自身の名前（ニックネーム等）に置き換えてください</font><br>

⑤コミットします<br>

```shell
git add .
```{{copy}}

```shell
git commit -m "first commit"
```{{copy}}


次のステップでは、heroku側の初期設定を行います。
