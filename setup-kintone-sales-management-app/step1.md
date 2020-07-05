kintoneに LINE Pay と連携する売上管理アプリを追加します。

[ここ](https://github.com/maztak/line-pay-v3-starter/archive/master.zip)から line-pay-v3-starter リポジトリをダウンロードし、解凍します。

①kintone開発者環境（`https://xxx.cybozu.com`）にアクセスし、`+`ボタンを押します。

![kintone_portal](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_portal.png)

②kintoneアプリストアに行くので、アプリを`テンプレートファイルを読み込んで作成`から作成します

![kintone_app_store](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_app_store.png)

`参照`ボタンを押し、先ほど解凍したフォルダの中にある`linepay_transaction.zip`を選択し、`アプリを作成`を押します。

③APIトークンの生成

作成したアプリをクリックし、さらに歯車ボタンからアプリの設定画面に行きます。
![kintone_linepay_record_list](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_linepay_record_list.png)


さらに`設定`タブをクリックし、`APIトークン`をクリック。

![kintone_app_setting](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_app_setting.png)

`生成する`をクリックしAPIトークンを生成し、アクセス権にすべてチェックを入れ`保存`を押します。

![kintone_api_token](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_api_token_generated.png)

ここで生成したトークンや表示されているIDは、後ほど使います。

以上でkintone側の準備が終わりです。