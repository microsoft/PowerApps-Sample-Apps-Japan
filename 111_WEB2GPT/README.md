# WEB2GPT (Web検索から回答作成)

> [!Note]
> AI Builder AI プロンプトとして、[GPT の機能が日本でも利用できるようになりました](https://learn.microsoft.com/ja-jp/ai-builder/availability-region)。
> 
> 日本でのAI プロンプトの利用は[地域間のデータ移動を有効化する](https://learn.microsoft.com/ja-jp/power-platform/admin/geographical-availability-copilot#enable-data-movement-across-regions)必要があります。
> 
> また、動いたよ、できたよという結果は是非、 [ギークフジワラのXアカウント](https://x.com/Geekfujiwara) までメンションしてご報告ください！！

Bing Search API でWebの検索結果を生成AI により要約して回答し、Dataverse に保存ができるPower Apps のアプリケーションです。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/2d3ffeca-578b-4f41-87f5-8b88cf195114)

> [!ポイント]
> 広く一般の公開情報に対して情報収集して要約することが可能なため、様々な分野で利用することが出来ます。

レスポンシブデザインに対応しており、スマホ縦レイアウトでは最低限の情報だけ表示されるようになります。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/9c0c2588-b6fd-43e8-970c-1dbd91a88cb0)

過去に登録されたナレッジも見たい場合は横向きのレイアウトにすると見えるようになっています。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/14069a28-7b6e-400c-82ff-80ae6b892801)


生成AI は間違いを起こすことがあるため、実際の検索結果を確認することが出来るようになっています。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/f4317e3c-e170-4b04-9e21-4a57959942fa)

作成した回答はナレッジとして保存することが出来ます。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/b446bd1d-06f6-49a8-8bf6-08be233fa41a)


# 事前準備

事前に以下を行う必要があります。

* [AI Builder が利用可能なライセンスを入手する](https://powerapps.microsoft.com/ja-jp/pricing/)
* [地域間のデータ移動を有効化する](https://learn.microsoft.com/ja-jp/power-platform/admin/geographical-availability-copilot#enable-data-movement-across-regions)
* [Azure を無料で始める](https://azure.microsoft.com/ja-jp/pricing/free-services/)

# インポート方法

## Bing Search API 

[Bing Search API](https://www.microsoft.com/en-us/bing/apis/bing-web-search-api)を準備します。

無償で利用できる枠が提供されていますのでそのプランでサインアップして試すことが出来ます。

### Bing Search API 無料枠の条件

* トランザクション上限1,000回/月
* 3回/秒 

[無料枠の条件](https://www.microsoft.com/en-us/bing/apis/pricing)

> [!Note]
> サポートが必要な本番環境での利用では有償のプランをご検討ください。

### リソースの作成方法

Bing search リソースを検索して新規作成します。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/2fe058a6-60b4-4d15-9ff2-cc5bee151765)

リソースは以下のように作成します。リソースグループ、名前は自由です。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/b3daa804-c306-41e7-ac42-df1bb9f74cfa)

作成できましたらキーを入手します。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/38d6c0e8-03e2-401c-b73d-458d8cc2ad1e)

## Power Apps ソリューション

Power Apps のソリューションは[リリース](https://github.com/geekfujiwara/WEB2GPT/releases/tag/1.0.0.0)から入手できます。

ソリューションのインポートを行います。
リリースから入手したソリューションファイルをアップロードします。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/a9234955-452d-417e-89a7-39bd87de7dd5)

次へ進みます。

インポート時にBing Search API のKeyを問われますので入力します。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/6c55326b-73cd-44da-a9f6-98e7c6d6c203)

> {!Note}
> インポート後に言語のラベルが不足している旨の警告が出ても問題ありません。
> ![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/35b1c7c8-a882-48bb-8c3c-6541ff1a0353)

マネージドソリューションをインポートした場合、マネージドソリューションのタブにソリューションが存在しています。すべてとすれば種別関係なく表示されます。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/ab0812ec-a7d7-40b5-b12b-70ff30c245b1)

WEB2GPTのSolutionに移ります。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/da51b867-5c1a-4cae-8648-5072a36ed52f)

インポート後、すべてのカスタマイズを公開してください。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/c91be7b8-95f6-4981-996b-c22d4af0b34d)

クラウドフローを有効にします。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/701ceb18-c803-43f7-b375-959c9a8b0e6d)


# アプリの利用方法

アプリを起動します。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/1d948b27-25a8-4c48-b5c8-34dfb8a429e0)


サンプルの質問として以下を入力してみます。

`Microsoft Storeの学生割引は親でも使えますか？`

> [!Note]
> 自由に質問を入力してみてください。

入力後、回答案の生成をさせてみます。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/2454dcc2-2ce4-4cbc-ab43-22403ccefa6a)


検索と生成に少々時間を要します。作成中はアプリの操作ができないように読み込み画面に切り替わります。

生成AIにより回答が生成されました。参考にしたリンクも同時に返してくれています。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/9b8b733b-658a-4eaa-ac9a-6f95f9594eda)

保存に成功すると左側のメニューに表示されます。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/5f714ec8-5109-404d-9b7f-305d5b98f06b)


> [!Note]
> 実際にはDataverseに保管されています。

生成AI は間違いを起こすことがあるため、実際の検索結果を確認することが出来るようになっています。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/f4317e3c-e170-4b04-9e21-4a57959942fa)


# 仕様説明

## AI Builder AI プロンプト

AI Builder では以下のようなAI プロンプトを作成しています。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/c8da8508-1d29-43a1-9c7b-91290eb02a7e)


## Power Automate でのBing Search

Power Automate で検索処理を設定しています。

HTTPリクエストの部分がBing Search API の部分です。

![image](https://github.com/geekfujiwara/WEB2GPT/assets/96101315/e05be8ed-2ef7-4de7-a325-bd2b51d9829a)



# リファレンス

* [Bing Custom Search API](https://learn.microsoft.com/ja-jp/bing/search-apis/bing-web-search/reference/headers)
* [Power Apps ソリューションインポート方法](https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/import-update-export-solutions)

