まず LINE Pay アプリを実装しましょう。

①Githubから[line-pay-v3-starter](https://github.com/maztak/line-pay-v3-starter) リポジトリをCloneします<br>

```shell
git clone https://github.com/maztak/line-pay-v3-starter.git
```{{copy}}

②カレントディレクトリを`line-pay-v3-starter`に変更します<br>

```shell
cd line-pay-v3-starter
```{{copy}}

③`pip`コマンドで`requirements.txt`に記載のライブラリをインストールします<br>
```shell
pip install -r requirements.txt
```{{copy}}

④kintone連携のための設定
今回はkintoneの売上管理アプリを連携させるので、`account.yml`を編集していきます。

Editorで`line-pay-v3-starter`ディレクトリをクリックして展開し、`account.yml`を開きます。

前のシナリオでkintoneに追加したlinepay連携アプリの情報をもとに値を変更します。
![kintone_api_token](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/create-line-pay-app/img/kintone_api_token.png)


```account.yml
domain: 自身のkintone開発者ライセンスに付与されたサブドメイン
apps:
    linepay: ←ここはアプリ名ですが今回は linepay を予め指定してます
        id: kintone linepay 連携アプリのID
        token: kintoneで生成したAPIトークン
```

これでアプリが動くために必要なものが揃いました。<br>

⑤gitの初期設定<br>

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
