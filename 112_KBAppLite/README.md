# ナレッジ管理アプリ「KBアプリ ライト版」
Power Apps モデル駆動型アプリによって作成されたKBアプリのライト版です。
AI Builder を利用したAzure OpenAI Service にて、ナレッジの自動生成機能も含まれています。


![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/d309749e-8f3f-43e8-8f8d-df49cf0f4f86)

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/93ace82f-3703-418f-a9ca-00bd5c88850e)

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/b2da70b1-4a52-40ad-9300-dc6835acc4e7)

## ナレッジ承認
ナレッジの承認を行うことが出来ます。コマンドバーの「ナレッジ承認」からクリックするとカスタムページが起動します。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/db43c44a-c658-4307-b1ce-97a1c29ea82a)

メールアドレスで承認者を検索することが出来ます。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/8b7865b0-022b-4e00-a6f1-9247d1e39e85)


![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/eae9cbc5-73ef-4366-9c94-c98716ae3ef6)

承認フローはPower Automate で実行されます。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/6022b7ff-2c19-437a-b8bd-18a1c88fffb3)


承認通知はTeams及びOutlook になされます。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/9f334001-426f-4ad4-ae0e-b0d0c0502524)

承認すると、Power Apps では承認ボタンは押せなくなります。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/8371b4de-0887-4c1d-b0e0-f6bc33434eee)

承認タブで状況を確認できます。


## ナレッジの自動生成 (Azure OpenAI Service)
ナレッジの自動生成は、製品とナレッジのタイトルのみ入力すると自動的に内容を生成してくれる機能です。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/af4c863b-785c-44d0-b402-e72e66f25e6d)

ビューを切り替えます。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/e07493cc-0723-4051-8f57-b167f4c2cc1a)

タイトルに質問、カテゴリで製品を選択して、GPTへの質問を「はい」にして保存します。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/c62a5f5e-d51c-47c8-b7e5-24f6cc370215)


以下のフローが利用されています。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/f3f4fa51-cace-463b-92f4-6c4c0a1aebf2)


作成時、かつGPTへの質問がTrueのときのみフローが起動します。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/98489ac2-f445-45c9-8e33-0f1dbd9cc702)


結果はこのようにして回答され、保存されます。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/7465b484-6e3e-41e0-ad98-5753a4cf2504)


# 設定方法
## ソリューションのインポート方法
ソリューションのインポート方法は以下にて説明があります。Microsoft Learnの情報を参照してください。
https://learn.microsoft.com/ja-jp/power-apps/maker/data-platform/import-update-export-solutions

## Azure OpenAI Serivce の利用
Azure OpenAI Serivce の利用を行うには、エンドポイントURIとAPI-KEYを指定する必要があります。

## ご利用マニュアルのURL
説明を置きたい場合、URLを設定するようにしてください。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/b7e06a3c-addd-42fc-b247-ed847f30ab66)


ソリューション内に入っておりますのでこちらから値を設定するようにしてください。
![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/4a52713e-d611-4d4a-9591-88147a1358a9)

環境変数の値の設定方法は以下のように行ってください。
ソリューションのインポート後に概要を開き、環境変数を更新するようにしてください。

![image](https://github.com/geekfujiwara/KBAppLite/assets/96101315/ef01c616-22ed-424e-bc3b-400c9d9406a9)
