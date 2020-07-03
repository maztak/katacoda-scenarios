ここでは、LIFF v2のスターターアプリをローカルに持って来て、きちんと動く環境にするために、3つのコマンドを実行します

1. LINEのgithubから、[line-pay-v3-starter](https://github.com/maztak/line-pay-v3-starter) リポジトリをCloneします<br>
```shell
git clone https://github.com/maztak/line-pay-v3-starter.git
```{{copy}}

2. カレントディレクトリを`line-pay-v3-starter`に変更します<br>
```shell
cd line-pay-v3-starter
```{{copy}}

3. `pip`コマンドで`requirements.txt`に記載のライブラリをインストールします<br>
```shell
pip install -r requirements.txt
```{{copy}}

4. `account.yml`を編集します。

Editorで`line-pay-v3-starter`ディレクトリをクリックして展開し、`account.yml`を開きます。

前のシナリオでkintoneに追加したlinepay連携アプリの情報をもとに値を変更します。
![kintone_api_token](https://github.com/maztak/katacoda-scenarios/blob/master/create-line-pay-app/img/kintone_api_token.png)

domain: 自身のkintone開発者ライセンスに付与されたサブドメイン
id: kintone linepay 連携アプリのID
token: kintoneで生成したAPIトークン

これでアプリが動くために必要なものが揃いました。<br>
それでは次のステップで、このアプリをherokuにデプロイ（Webサーバーにアプリをアップロードして使えるようにする）していきましょう！
