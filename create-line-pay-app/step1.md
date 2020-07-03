ここでは、LIFF v2のスターターアプリをローカルに持って来て、きちんと動く環境にするために、3つのコマンドを実行します

1. LINEのgithubから、[line-pay-v3-starter](https://github.com/maztak/line-pay-v3-starter) リポジトリをCloneします<br>
```shell
git clone https://github.com/maztak/line-pay-v3-starter.git
```{{copy}}

2. カレント・ディレクトを`line-pay-v3-starter`に変更します<br>
```shell
cd line-pay-v3-starter
```{{copy}}

3. `pip`コマンドで`requirements.txt`に記載のライブラリをインストールします<br>
```shell
pip install -r requirements.txt
```{{copy}}


これでアプリが動くために必要なものが揃いました。<br>
それでは次のステップで、このアプリをherokuにデプロイ（Webサーバーにアプリをアップロードして使えるようにする）していきましょう！
