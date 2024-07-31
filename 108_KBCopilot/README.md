# KBCopilot - ナレッジ回答アプリ
Dataverse 内のデータの検索を行い、Copilot Studio の生成型の回答で要約返答することができるソリューションです。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/eb8d6e3e-0357-46e6-ae02-60d232bf44b6)



https://github.com/geekfujiwara/KBCopilot/assets/96101315/789444d1-422e-408b-bc55-94f556618714



# ソリューション

KBCopilot - ナレッジ回答Copilot は、前提として以下のPower Apps で作成されたナレッジ管理アプリをインストールする必要があります。

また、ナレッジ回答アプリはAttachments Grids というPCF (Power Apps Component Framework)を利用しています。そのため、段階的にソリューションをインストールしてください。

> [!NOTE]
> 今回利用するPCF は添付ファイルを簡単にアップロードすることができるソリューションです。
>
> ドラッグ&ドロップでファイルをアップロードすることが出来ます。
> 
> ![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/b66c079c-1165-4fa4-a9fa-c0408c69113e)
>
> アップロードはDataverse のメモ (タイムライン)に保存されます。
>
> ![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/2e26d48d-1725-4883-9694-5fd71697ec46)
> 
> このようにPCF が提供されている[PCF Gallery](https://pcf.gallery/) から様々の機能をインストールすることが出来ます。
>
> 有志での提供のため、その殆どがサポート対象外のためその点はご注意ください。

# 前提条件

* Copilot Studio スタンドアローンライセンスが必要です。
* Power Apps Premium ライセンスが必要です。
* AI Builder のクレジットが必要です。


## インストール手順

手順は以下のとおりです。各ソリューション間には依存関係があるためこの順番でインストールするようにしてください。

1. [Attachments Grid](https://pcf.gallery/attachments-grid/)
2. [環境のDataverse検索を有効にする](https://learn.microsoft.com/ja-jp/power-platform/admin/configure-relevance-search-organization)
3. [KBApp - Power Apps モデル駆動型アプリのリリース](https://github.com/geekfujiwara/KBCopilot/releases/tag/KBApp)
4. [KBCopilot - Copilot Studioで作成したナレッジ回答Copilotのリリース](https://github.com/geekfujiwara/KBCopilot/releases/tag/KBCopilot)

KBCopilot をインストールする際には環境変数 KBAppURLが問われます。

KBAppのペースURLを入力するようにしてください。

モデル駆動型アプリを起動してappidまでのURLを入手しておきます。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/4da373b8-e2ac-488b-b2d7-e673c6553f1f)


> [!NOTE]
> 各ソリューションをインストール後、すべてのカスタマイズを公開するようにしてください。
>
> もし、Power Automate クラウドフローがオフになっている場合、オンにするようにしてください。



## インストールの補足

Attachemnts Grid はGitHub上に[ソリューション](https://github.com/BenLBartle/PCF-AttachmentsGrid/blob/master/Solution/bin/Debug/Solution.zip)が提供されています。

こちらからZip ファイルをダウンロードしてください。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/b2358ae9-1bdb-4e47-b565-47a698d96f4c)



## インストール後のアプリのセットアップ

ソリューションをインストールし、まずはPower Apps ナレッジ管理 モデル駆動アプリにデータを登録します。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/aa05ca1e-a39c-452d-a218-e0edfa1a7bdb)

データを登録したら、Copilot から質問を投げかけます。



# 機能紹介

ナレッジベースに書かれていることについて質問をしてみます。
※事前にモデル駆動型アプリからなどで、Dataverse にナレッジを登録しておく必要があります。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/78d813b6-5106-4eb9-b204-cfe1f868ee3f)

ナレッジがヒットすると、Copilot に返答が行われます。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/2e8c180e-ee0e-4fba-82e5-df6b100b47ab)

引用のリンクをクリックすると、ソースを確認することが出来ます。
モデル駆動型アプリに遷移する事ができるようになってきます。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/633cfb03-680d-4b8b-902b-2104dba72bc8)

クラウドフローで検索を行っています。

ユーザーのからのメッセージからキーフレーズ抽出をAI Builder にて行います。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/83df26e0-85c7-4901-8aca-76772f2d8bdf)

検索結果はナレッジのテーブルからDataverse 検索機能を利用してTop 3 を抽出しています。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/3abd1b5e-1d08-4e00-9a2e-e74361b8ea93)

抽出した結果をCopilot Studio の生成型の生成のカスタムデータで扱える形式にして返答します。

![image](https://github.com/geekfujiwara/KBCopilot/assets/96101315/342cb7a9-09f7-4bda-ae4f-109842764e6f)

[生成型の回答にカスタム データ ソースを使用する - Microsoft Learn](https://learn.microsoft.com/ja-jp/microsoft-copilot-studio/nlu-generative-answers-custom-data)

