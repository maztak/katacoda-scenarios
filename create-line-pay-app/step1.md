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

4. KatacodaのIDEをクリックします
![ide](https://raw.githubusercontent.com/MasatakaMiki/katacoda-scenarios/master/liff_drawing_scenario/img/s0101_ide.jpg)<br>

5. `line-pay-v3-starter`をデプロイします
![ide](https://raw.githubusercontent.com/MasatakaMiki/katacoda-scenarios/master/liff_drawing_scenario/img/s0102_ide.jpg)<br>

6. `.gitignore`ファイルを作成します<br>
`line-pay-v3-starter`上でマウスを右クリック、`New File`をクリックし、ファイル名に.gitignoreと入力します
![gitignore](https://raw.githubusercontent.com/MasatakaMiki/katacoda-scenarios/master/liff_drawing_scenario/img/s0103_gitignore.jpg)<br>

7. ファイルに下記を追加し、保存します
```
.env
# account.yml #後で確認
```{{copy}}
![gitignore](https://raw.githubusercontent.com/MasatakaMiki/katacoda-scenarios/master/liff_drawing_scenario/img/s0104_gitignore.jpg)<br>

これで、〇〇ができました。<br>
それでは、次のステップから、このアプリをherokuにデプロイ（Webサーバーにアプリをアップロードして使えるようにする）していきましょう！
