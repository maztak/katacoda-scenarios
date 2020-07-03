kintoneに LINE Pay と連携する売上管理アプリを追加します。

[ここ](https://github.com/maztak/line-pay-v3-starter/archive/master.zip)から line-pay-v3-starter リポジトリをダウンロードし、回答します。

①kintone開発者環境（`https://xxx.cybozu.com`）にアクセスし、kintoneポータルサイトに行きます。

![kintone_portal](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_portal.png)

②アプリの`+`ボタンからkintoneアプリストアにいきます。

![kintone_app_store](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_app_store.png)

`テンプレートファイルを読み込んで作成`から先ほど解答したフォルダの中にある`linepay売上管理.zip`を参照し、`アプリを作成`を押します。

③APIトークンの生成

作成したアプリをクリックし、アプリの設定画面に行きます。
![kintone_linepay_record_list](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_linepay_record_list.png)


設定画面のさらに`設定`タブをクリックし、`APIトークン`をクリック。

![kintone_app_setting](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_app_setting.png)

`生成する`をクリックしAPIトークンを生成します。

アクセス権にすべてチェックを入れ`保存`を推します。

![kintone_api_token](https://raw.githubusercontent.com/maztak/katacoda-scenarios/master/setup-kintone-sales-management-app/img/kintone_api_token_generated.png)

以上でkintone側の準備が終わりました。

ここで生成したトークンや表示されているIDは、後ほど使います。