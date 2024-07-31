# 複数データソースに対応したチャットアプリ
Power Apps をインターフェイスとして、各種データソースに対して検索を行うことができるアプリです。Dataverse、SharePoint、OneDriveのほか、Azure AI Search 経由の各種データソースに対してRAGを簡単に実現することができます。

> [!NOTE]
> 作成したよ、という方はぜひ[ギークフジワラのXアカウント](https://x.com/geekfujiwara/status/1800463571169804761?s=46&t=X4PQ4pTx14WnUTLP_ysSJw)までご連絡ください！

## アプリの概要

* Azure OpenAI Searvice (GPT-4o推奨) を利用して、検索クエリの作成、検索結果の要約を行っています。
* カスタムのデータソースとしてAzure AI Search のAPIに接続して検索結果を取得する仕組みも実装されています。
* SharePoint とOneDrive への検索は権限のある範囲での検索をGraph APIを介して行います。
* Dataverse への検索は、別で作成している[ナレッジ管理アプリのテーブル、モデル駆動型アプリ](https://github.com/geekfujiwara/KBCopilot/releases/tag/KBApp)を利用しています。Dataverse Search を行い、その結果をAzure OpenAIに要約させて返答しています。


https://github.com/geekfujiwara/AzureAISearchMultiDatasourcePowerApp/assets/96101315/a373d195-2824-4405-872c-84bfc23f69ca


# 参考情報

[ブログ](https://www.geekfujiwara.com/)

[YouTubeチャンネル](https://www.youtube.com/@geekfujiwara)

[X](https://twitter.com/geekfujiwara)

# インストール方法

## ナレッジ管理アプリ

Dataverse Search の対象として利用しているナレッジ管理アプリを準備する必要があります。
ナレッジ管理アプリは様々なコンポーネントを利用しており、以下の項目をインストール及び設定する必要があります。

1. [Attachments Grid](https://pcf.gallery/attachments-grid/)
2. [環境のDataverse検索を有効にする](https://learn.microsoft.com/ja-jp/power-platform/admin/configure-relevance-search-organization)
3. [KBApp - Power Apps モデル駆動型アプリのリリース](https://github.com/geekfujiwara/KBCopilot/releases/tag/KBApp)

### Attachemnts Grid のインストールの補足情報

Attachemnts Grid はGitHub上に[ソリューション](https://github.com/BenLBartle/PCF-AttachmentsGrid/blob/master/Solution/bin/Debug/Solution.zip)が提供されています。

こちらからZip ファイルをダウンロードしてください。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/b2358ae9-1bdb-4e47-b565-47a698d96f4c)

### 環境変数用にナレッジ管理アプリのベースURLを取得 

ナレッジ管理アプリをインストールしたら、アプリのURLを取得、メモ帳などに保管しておきます。

本ソリューションをインストールする際に環境変数 KBAppURLが問われ、そのときに必要になります。

> [!NOTE]
> AppIdまでのKBAppのペースURLを取得するようにしてください。

モデル駆動型アプリを起動してappidまでのURLを入手しておきます。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/4da373b8-e2ac-488b-b2d7-e673c6553f1f)


> [!NOTE]
> 各ソリューションをインストール後、すべてのカスタマイズを公開するようにしてください。
>
> もし、Power Automate クラウドフローがオフになっている場合、オンにするようにしてください。

## ナレッジ管理アプリへのデータの追加

ナレッジ管理アプリを検索対象としたときにデータが入っていないと検索結果がないとなります(そりゃそうだ)。

そのため、ナレッジ管理アプリに何かデータを登録するようにしておいてください。

## Azure

## 必要な環境変数

以下の環境変数を用意する必要があります。

* ナレッジ管理アプリのURL
* Azure OpenAI URL
* Azure OpenAI APIキー
* Azure AI Search URL
* Azure AI Search インデックス
* Azure AI Search APIキー

### Azure OpenAI のエンドポイント及びAPI キー

チャットプレイグラウンドからコードの表示と進めると確認できます。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/6d323025-2202-4ce6-8e8b-b35a98e1fefe)


エンドポイントURLはCurlから取得できます。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/3a2bb72e-97f5-44ff-bf3d-ed974b3124de)

APIキーはこちらから取得できます。

![image](https://github.com/geekfujiwara/GPT-4oPowerApps/assets/96101315/d5ef7dc2-0b13-4855-9828-d9f44d82f9a2)


### Azure Search AI のURLとインデックス、APIキー

Azure AI Search のURLは以下より入手できます。 

![image](https://github.com/geekfujiwara/AzureAISearchMultiDatasourcePowerApp/assets/96101315/4701c180-3f2d-475a-bd72-715065a2d4f3)


Azure AI Search のインデックスは以下より入手できます。 

![image](https://github.com/geekfujiwara/AzureAISearchMultiDatasourcePowerApp/assets/96101315/41d7a4ae-aca3-437e-891b-83d246e9c64c)


Azure AI Search のAPIキーは以下より入手できます。

APIキーを生成して出力することを推奨します。

![image](https://github.com/geekfujiwara/AzureAISearchMultiDatasourcePowerApp/assets/96101315/2229f865-ae07-473f-970f-8c5b4d87ec53)

ここまでで環境変数の準備が完了です。

## 複数データソースに対応したチャットアプリソリューションのインポート

[リリース](https://github.com/geekfujiwara/AzureAISearchMultiDatasourcePowerApp/releases)より最新のマネージドソリューションを入手しインポートします。

ここまでで準備してきた情報を環境変数に入力してインポートします。

![image](https://github.com/geekfujiwara/AzureAISearchMultiDatasourcePowerApp/assets/96101315/82227723-adfd-48bd-a61e-2906058e26c6)


インポート後はカスタマイズをすべて公開します。

もしクラウドフローがオフになっている場合はオンにします。

# アプリの実行

アプリを実行できます。Enjoy!

![image](https://github.com/geekfujiwara/AzureAISearchMultiDatasourcePowerApp/assets/96101315/fd6d7578-3530-4215-8de6-4c31fbfdae6d)


以上、ご参考になれば幸いです。










